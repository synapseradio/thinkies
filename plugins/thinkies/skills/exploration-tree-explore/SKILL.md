---
name: tree-explore
description: Systematically explore topics through hierarchical branching paths with controlled depth, useful for thorough research, complex problem exploration, or understanding all aspects of a subject
---

# Tree Explore

Explore topics through systematic branching with deliberate depth control.

## Instructions

When exploring as a tree:

1. **Establish the root**: What's the main topic or question?
   - Keep this clear and focused
   - This anchors all exploration

2. **Branch deliberately**:
   - First level: 2-4 major aspects or questions
   - For each branch, identify 2-3 sub-branches
   - Mark which branches deserve deep dives

3. **Control depth**:
   - Shallow branches: Note exists, move on
   - Deep branches: Fully explore sub-branches
   - Mark why some get more attention

4. **Maintain context**:
   - Always know which branch you're on
   - Explicitly return to parent before switching branches
   - "Returning to [parent topic]..."

5. **Systematic coverage**:
   - Visit every branch at least briefly
   - Note unexplored areas for potential return
   - Complete one branch before moving to siblings

6. **Synthesize at each level**:
   - What patterns emerge across branches?
   - How do sibling branches relate?

## Examples

### Exploring a system architecture:
```
Root: How does this authentication system work?
├── Branch 1: Component structure
│   ├── API gateway layer [shallow - well documented]
│   ├── Auth service [DEEP DIVE - complex logic here]
│   │   ├── Token validation
│   │   ├── Permission checking
│   │   └── Session management
│   └── Database layer [shallow - standard setup]
├── Branch 2: Data flow
│   ├── Login sequence [DEEP DIVE - critical path]
│   ├── Refresh flow
│   └── Logout handling
└── Branch 3: Security measures
    ├── Encryption approach
    └── Attack prevention
```

### Investigating a problem:
"Root question: Why are users abandoning the checkout flow?

First level branches:
1. Technical issues (errors, performance)
2. UX friction points (confusion, too many steps)
3. Trust/security concerns (payment fears)

Taking branch 1 deeper:
- Performance sub-branch: Load times are fine
- Error sub-branch: [DEEP DIVE] Finding JavaScript errors on mobile...
  - iOS specific issues
  - Payment validation failing silently
  - [Key finding]: Error messages not showing

Returning to root, taking branch 2..."

## When to use this skill

- Need systematic, thorough exploration
- Complex topics requiring structured investigation
- Research tasks where completeness matters
- Understanding system architectures
- Debugging with multiple possible causes
- Learning new domains methodically
- Documenting comprehensive understanding