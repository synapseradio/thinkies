---
name: decompose
description: Break overwhelming problems into manageable components for systematic analysis, useful for large projects, complex systems, or any situation where the whole feels too big to grasp
---

# Decompose

Break complex problems into smaller, manageable pieces that can be understood and solved independently.

## Instructions

When decomposing:

1. **Define the whole**: What's the full scope of what you're dealing with?
   - State the problem completely
   - Note what makes it feel overwhelming

2. **Identify natural boundaries**:
   - Functional boundaries (what different parts do)
   - Temporal boundaries (what happens when)
   - Spatial boundaries (where things happen)
   - Logical boundaries (independent concepts)
   - Data boundaries (what information flows where)

3. **Create components**:
   - Each piece should be understandable alone
   - Minimize dependencies between pieces
   - Make interfaces between components explicit
   - Aim for 3-7 components at each level

4. **Check completeness**:
   - Do components cover everything?
   - Any gaps between components?
   - Any unwanted overlaps?

5. **Decompose recursively**:
   - Take complex components
   - Break them down further
   - Stop when pieces are manageable

6. **Map relationships**:
   - How do components interact?
   - What depends on what?
   - What can be parallel vs sequential?

7. **Identify the core**:
   - Which component is most critical?
   - What's the minimum viable subset?
   - Where should you start?

## Examples

### Decomposing a system migration:
"**Overwhelming problem**: Migrate legacy system to new architecture

**Functional decomposition**:
1. **Data layer**: Database schema, data migration, integrity
2. **Business logic**: Core algorithms, rules, workflows
3. **Integration layer**: APIs, external services, webhooks
4. **User interface**: Pages, components, interactions
5. **Infrastructure**: Servers, deployment, monitoring

**Temporal decomposition of data layer**:
- Phase 1: Schema design and mapping
- Phase 2: Migration script development
- Phase 3: Test with sample data
- Phase 4: Full migration with rollback plan

**Risk-based decomposition**:
- Critical path: User authentication (breaks everything if wrong)
- High risk: Payment processing (money involved)
- Medium risk: Reporting (important but not critical)
- Low risk: Admin tools (internal only)

**Starting point**: Critical path + minimum data to test it"

### Decomposing a debugging problem:
"**Overwhelming problem**: App crashes randomly in production

**Symptom decomposition**:
- When: Time patterns, frequency
- Where: Which endpoints, which servers
- Who: User types, geographic distribution
- What: Error messages, stack traces

**System layer decomposition**:
- Frontend (JavaScript errors?)
- API layer (request handling?)
- Business logic (processing errors?)
- Database (query failures?)
- Infrastructure (resource exhaustion?)

**Hypothesis decomposition**:
For each layer, check:
- Logs at that layer
- Error patterns
- Recent changes
- Resource usage

**Simplification**: Can we reproduce with:
- Single user?
- Minimal data?
- One feature disabled?
- Locally vs production?"

### Decomposing a feature request:
"**Complex request**: Add real-time collaboration

**User journey decomposition**:
1. Joining a session
2. Seeing others' cursors
3. Editing simultaneously
4. Handling conflicts
5. Leaving session

**Technical component decomposition**:
- WebSocket connection management
- Operation transformation
- Conflict resolution
- State synchronization
- Persistence layer

**Each component breaks down**:
WebSocket management:
- Connection establishment
- Authentication
- Reconnection logic
- Message queuing
- Error handling

**MVP decomposition**: Start with seeing others' cursors - simplest real-time feature"

## When to use this skill

- Project planning
- System design
- Complex debugging
- Large refactoring
- Learning new systems
- Writing documentation
- Task estimation
- Team work distribution