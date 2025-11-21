---
name: scamper
description: Apply 7 systematic creativity lenses (Substitute, Combine, Adapt, Modify, Put to other use, Eliminate, Reverse) to generate fresh ideas and innovative solutions
---

# SCAMPER

Transform problems and ideas by systematically applying seven different creative operations.

## Instructions

When using SCAMPER:

1. **Work through each lens deliberately** - Apply all seven operations even when some feel less relevant, since the uncomfortable ones often yield the most surprising ideas: Substitute (replace elements with alternatives), Combine (merge multiple elements together), Adapt (borrow from other contexts), Modify (change attributes or scale), Put to other use (repurpose for different contexts), Eliminate (remove elements to simplify), and Reverse (flip it around or do the opposite).

2. **Generate possibilities for each operation** - For Substitute, ask what components could be swapped out, what different materials or processes could work, or who else could do this instead. For Combine, consider what could blend together, whether purposes could merge, or if adjacent processes could unite. For Adapt, look at what similar solutions exist in other domains, how different industries solve comparable problems, or what patterns from nature or games could apply. For Modify, explore making it bigger or smaller, changing shape or form, altering frequency or timing, or shifting who has control. For Put to other use, identify what else this could do, who else could use it, or whether side effects could become the main purpose. For Eliminate, question what could be removed entirely, what's truly needed, or what the core essence is. For Reverse, imagine doing the opposite, reversing order or sequence, or swapping who does what between user and system.

3. **Combine operations and capture everything** - After exploring each lens individually, try combining them to ask questions like "What if we eliminated X and combined Y with Z?" Record every idea even when it seems impractical, since wild ideas often contain seeds of practical solutions, and revisit the process with specific elements when stuck.

## Examples

### Product feature development

"We're rethinking how users share documents in our collaboration tool.

**Substitute**: Instead of email-based sharing, what if we used QR codes that expire after scanning, or blockchain-based access tokens?

**Combine**: What if sharing and permission setting were the same single action, eliminating the two-step process?

**Adapt**: Dropbox uses simple link sharing - could we adapt their model but add our document versioning on top?

**Modify**: What if shares automatically expired after 24 hours unless explicitly extended, creating urgency and reducing stale permissions?

**Put to other use**: Our share logs are for auditing, but what if users could use them as a collaboration timeline showing document evolution?

**Eliminate**: What if there was no sharing UI at all, just a button that generates a simple link with smart defaults?

**Reverse**: Instead of owners granting access, what if recipients requested it and owners approved from a queue?

That last reversal is interesting - it flips the power dynamic and might reduce permission sprawl while giving owners better context about why someone needs access."

### Technical architecture

"Rethinking our application's caching strategy.

**Substitute**: What if we used CDN edge caching globally instead of centralized Redis, or replaced the cache entirely with a faster database?

**Combine**: What if cache and database were unified into a single system that handles both persistence and speed?

**Adapt**: Browsers have sophisticated caching with headers and invalidation - could we use HTTP caching semantics for our internal services?

**Modify**: What if cache lifetime was infinite by default with smart invalidation triggered by mutations, rather than time-based expiry?

**Put to other use**: Cache misses reveal user needs - could we use that pattern to drive intelligent preloading strategies?

**Eliminate**: What if we removed caching entirely and instead optimized our database queries and added better indexes?

**Reverse**: Instead of our application caching database results, what if the database itself cached frequently-accessed queries?

The Eliminate lens is forcing us to question whether we have a caching problem or a database optimization problem - maybe we're solving the wrong thing."

### Team process improvement

"Our code review process is slow and becoming a bottleneck.

**Substitute**: What if we used automated code quality tools instead of manual review for style issues, or peer programming instead of async reviews?

**Combine**: What if code review and deployment approval were the same step, or reviews happened during standups as a team?

**Adapt**: How do open source projects handle reviews at scale? Could we adapt their maintainer model or review rotation?

**Modify**: What if instead of reviewing entire pull requests, we reviewed smaller commits continuously throughout the day?

**Put to other use**: Review comments contain valuable learning - could we turn them into a searchable knowledge base for common patterns?

**Eliminate**: What if we eliminated review for certain types of changes like documentation or tests, or removed the requirement that seniors review everything?

**Reverse**: What if authors requested specific reviewers to look at specific parts, rather than assigning whole PRs to someone?

Combining Eliminate and Modify: what if we removed review requirements for small changes under 50 lines and did rapid 5-minute reviews for everything else?"

## When to use this skill

- When you're stuck generating creative alternatives to a problem
- Before committing to the first solution that comes to mind
- When brainstorming new features or redesigning existing systems
- To challenge conventional approaches that may be limiting options
- When you notice yourself following habitual patterns without questioning them
- Before telling the user "here's the solution" without exploring alternatives first
- To generate diverse options for comparison rather than presenting a single path
