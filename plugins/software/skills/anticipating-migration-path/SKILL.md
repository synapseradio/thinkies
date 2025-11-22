---
name: migration-path
description: Design safe migration strategies for breaking changes - planning how to evolve systems without breaking users
---

# Migration Path

Plan how to safely transition from current to new state when making breaking changes, ensuring users can migrate without disruption.

## Instructions

When I need to make a breaking change, I design a migration path that allows the system to evolve while protecting existing users from sudden failures.

1. **Identify what breaks** - I precisely define the contract change by documenting what currently works that will stop working, whether that's an API signature, data format, configuration structure, or behavioral assumption, so I understand exactly what I'm asking users to change.

2. **Find all affected users** - I search the codebase for every location that depends on the current behavior, distinguishing between internal callers I can update directly and external consumers I can only influence through communication, which determines how much control I have over the migration.

3. **Design the transition state** - I create a period where both old and new approaches work simultaneously, using techniques like API versioning, feature flags, adapter layers, or dual-write patterns, allowing users to migrate at their own pace rather than forcing a flag day.

4. **Create the migration steps** - I define the ordered sequence users will follow to move from old to new, breaking it into small safe steps with clear validation points, ensuring each step can be verified before proceeding and rolled back if problems appear.

5. **Plan communication** - I determine who needs to know about the change and when, drafting deprecation warnings, migration guides, and timeline announcements that give users sufficient notice and clear instructions, recognizing that breaking changes are as much about communication as code.

6. **Define rollback strategy** - I establish how to undo the migration if critical issues emerge, ensuring the transition state supports reverting to old behavior and that I can safely back out at each step, because migrations sometimes reveal problems testing didn't catch.

7. **Establish success criteria** - I define how I'll know the migration is complete, setting metrics for adoption rate, error rate changes, and when it's safe to remove the old code path, so I don't prematurely break users who haven't migrated yet.

## Examples

### Migrating an API endpoint structure

I need to change `/api/users/:id` to return a nested user object instead of a flat structure. The current `{ id, name, email }` needs to become `{ id, profile: { name, email }, metadata: { ... } }` for consistency with other endpoints. I search the codebase and find 23 internal components calling this endpoint plus unknown external API consumers. I design a transition using API versioning: create `/api/v2/users/:id` with the new structure while keeping v1 unchanged, add a response header to v1 saying "Deprecated: migrate to /api/v2/users/:id by 2024-06-01", update internal callers one service at a time with PRs that can be independently reviewed and deployed, and provide a migration guide showing the exact field mappings. My rollback strategy is that v1 continues working indefinitely until adoption metrics show 100% of traffic on v2. Success means no v1 requests for 30 days, then I can remove the old endpoint.

### Migrating database schema with required field

I need to add a required `tenant_id` field to the `documents` table in a multi-tenant system currently identified by session context. Breaking the change immediately would cause all queries without `tenant_id` to fail. I design a multi-phase migration: Phase 1 adds `tenant_id` as nullable and backfills existing rows using audit logs to determine ownership, Phase 2 updates application code to always set `tenant_id` on new records and include it in queries, Phase 3 validates that all records have `tenant_id` populated and no queries omit it, Phase 4 adds the NOT NULL constraint and unique indexes. Each phase deploys separately with verification before proceeding. I create a feature flag to control whether queries require `tenant_id`, allowing instant rollback by disabling the flag. My communication plan includes database migration guides for the ops team and code change requirements for developers. Success criteria is 7 days of production traffic with 100% of queries including `tenant_id` before making it required.

### Migrating shared library interface

I maintain an internal `Logger` utility used by 50+ services. The current `log(level, message)` interface needs to become `log(level, message, context)` to support structured logging and tracing. Updating all callers simultaneously is impossible due to separate deployment schedules. I design a migration using the adapter pattern: create `LoggerV2` with the new interface, update `Logger` to detect calls with context and delegate to `LoggerV2`, make the old interface still work by passing empty context, and emit deprecation warnings when the old interface is used. I write a codemod script to automatically migrate calling code from old to new interface, test it on 5 services, then publish migration instructions with the automated tool and manual examples. My communication plan includes posting in the engineering Slack channel, updating the internal docs, and sending weekly reports showing migration progress by service. The rollback strategy is that old code continues working indefinitely until migration completes. Success means deprecation warnings drop to zero, then I can remove the adapter layer and old interface.

## When to use this skill

- I catch myself proposing to rename, remove, or restructure public APIs without mentioning how existing users will handle the change
- I'm suggesting database schema changes without addressing how existing data migrates or how queries continue working during the transition
- I notice I'm recommending breaking changes to shared libraries or utilities without considering the deployment dependencies of all consumers
- I'm planning refactoring that changes interfaces or contracts without designing how both old and new can coexist during migration
- I find myself saying "just update all the callers" without recognizing some callers may be external, in different repositories, or on different deployment schedules
- I'm proposing changes without defining what "migration complete" means or how we'll know when it's safe to remove old code
- I realize I haven't thought about what happens if the migration reveals problems and we need to roll back
- I'm making assumptions about how quickly users can migrate without considering their deployment constraints or the communication required

## Related Skills

- `blast-radius` - Understand scope of impact before designing migration strategy
- `failure-modes` - Anticipate what can go wrong during migration execution
- `codebase-cartography` - Map the system to find all affected areas
- `dependency-graph` - Trace all consumers of the interface being changed
- `trace-flow` - Understand current behavior before changing it
