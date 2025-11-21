---
name: tree-explore
description: Systematically explore topics through hierarchical branching paths with controlled depth, useful for thorough research, complex problem exploration, or understanding all aspects of a subject
---

# Tree Explore

Map topics through systematic branching with controlled depth.

## Instructions

When exploring hierarchically:

1. **Define the root** - State your main topic or question clearly and completely, which anchors all subsequent exploration.

2. **Identify first-level branches** - List 2-4 major aspects or sub-questions that are distinct and meaningful, marking which warrant deeper investigation.

3. **Control depth deliberately** - Handle shallow branches by acknowledging key points before proceeding, expand deep branches into sub-branches for thorough exploration, and document each depth decision with explicit reasoning.

4. **Maintain navigational awareness** - Track your current position in the tree, return explicitly to parent topics before switching branches, and use clear markers to show movement between sections.

5. **Ensure systematic coverage** - Visit each branch at minimum depth, complete one branch fully before moving to siblings, and note any unexplored areas for potential return.

6. **Synthesize at each level** - Identify patterns across sibling branches, understand relationships between components, and extract insights from comparing branches.

## Examples

### System architecture

"**Root**: How does this authentication system work?

**Branch structure**:
```
├── Component organization
│   ├── API gateway [shallow - standard proxy pattern]
│   ├── Auth service [deep - custom logic]
│   │   ├── Token validation flow
│   │   ├── Permission resolution
│   │   └── Session lifecycle
│   └── Data persistence [shallow - PostgreSQL conventions]
├── Request flow
│   ├── Initial authentication [deep - critical path]
│   │   ├── Credential validation
│   │   ├── Token generation
│   │   └── Response formation
│   ├── Token refresh [medium - important but clear]
│   └── Logout [shallow - straightforward]
└── Security implementation
    ├── Encryption strategy
    └── Attack mitigation
```

**Synthesis**: The complexity centers on the auth service, specifically token handling. Gateway and database follow standard patterns. Focusing investigation on token validation and refresh logic."

### Product investigation

"**Root**: Why has feature adoption plateaued at 35%?

**First-level branches**:
1. Discovery (users don't know it exists)
2. Access (users can't find or enable it)
3. Value perception (users don't see the point)
4. Usability (users try but struggle)

**Exploring branch 2 (Access)**:
- Navigation path: [shallow] Present in settings menu, fourth item
- Enablement: [deep - potentially problematic]
  - Requires three-step setup process
  - Second step fails silently for 12% of users
  - Error logging shows timeout on validation API
  - [Finding]: Network latency blocking setup completion

Returning to root. Branch 2 revealed blocking issue. Checking branch 4 (Usability) to see if similar patterns exist for users who complete setup..."

### Learning new domain

"**Root**: Understanding functional reactive programming

**Branch structure**:
1. Core concepts
   - Streams and observables [deep - foundation]
   - Operators and composition [deep - essential patterns]
   - Subscription management [medium - practical concern]
2. Comparison to alternatives
   - vs callbacks [shallow - familiar territory]
   - vs promises [shallow - understand differences]
   - vs async/await [shallow - when to use each]
3. Common patterns
   - Data fetching [medium - frequent use case]
   - UI events [medium - frequent use case]
   - Error handling [deep - critical for production]

**Synthesis**: Mastering observables and operators provides foundation. Error handling deserves focused study - mistakes here create hard-to-debug issues. Comparison to promises clarifies when this approach adds value versus added complexity."

## When to use this skill

- When you need to ensure comprehensive coverage of a topic without missing major aspects
- When exploring a system or problem with multiple interconnected components that need organized investigation
- When you notice yourself jumping between topics without completing any single thread of exploration
- When the cost of overlooking something is high enough to justify systematic rather than intuitive exploration
- When you need to document or communicate the full scope of what you've investigated
- When learning a new domain where you lack intuition about what matters most
- When investigating problems with multiple potential causes that each deserve consideration

## Related Skills

**decompose** - For breaking complex problems into structural components. Use decompose when organizing work or understanding system organization. tree-explore focuses on investigative exploration with depth control, while decompose focuses on creating a workable breakdown for analysis or action.