---
name: branch
description: Generate multiple distinct paths or possibilities from a single idea when you need alternatives, want to avoid tunnel vision, or explore different approaches to a problem
---

# Branch

Create multiple distinct continuations or possibilities from a single starting point.

## Instructions

When branching:

1. **Identify your starting point** - State the current idea, approach, or assumption clearly enough that you can see where it might diverge, noting the specific decision point or constraint that could be altered.

2. **Generate distinct branches** - Create 3-5 meaningfully different directions by asking what completely different approach could work here, considering opposite strategies rather than variations on the same theme, and ensuring each branch represents a fundamentally different path rather than minor adjustments.

3. **Make each branch concrete** - Specify what would actually be different in practice for each option, describe how it would work operationally, identify the unique trade-offs it creates, and resist the urge to eliminate branches prematurely.

4. **Map the divergence structure** - Note where exactly the paths split from each other, identify what decision or assumption causes each fork, and consider whether branches could recombine later or must remain distinct.

## Examples

### Error handling strategy

"**Starting point**: We need better error handling

**Distinct branches**:
1. **Defensive**: Validate at every boundary, fail fast and visibly
   - Catches problems immediately
   - More code, louder failures
   - Best for catching bugs early

2. **Recovery-focused**: Design for graceful degradation
   - Maintains partial functionality
   - Harder to debug root causes
   - Best for user experience

3. **Prevention**: Redesign to make errors impossible
   - Uses type system, constraints
   - Requires more upfront work
   - Best for long-term reliability

4. **Observable**: Let errors happen, detect and alert
   - Minimal code changes
   - Requires good monitoring
   - Best for understanding real patterns

**Key insight**: Each branch optimizes for different values - speed of detection, user experience, code simplicity, or learning."

### User research insight

"**Starting point**: 'Users want more features'

**Questioning branches**:
1. **Opposite**: Users actually want fewer, better features
   - Feature bloat is the problem
   - Would simplify instead of adding

2. **Communication gap**: Users want features but can't name them
   - Articulation problem, not want problem
   - Would require observational research

3. **Proxy request**: Users think they want features but really want outcomes
   - Features are their attempt at solutions
   - Would focus on problems, not requests

4. **Segmentation**: Different user types want opposing things
   - No single answer satisfies everyone
   - Would require product differentiation

**Key insight**: Each branch suggests a completely different research approach and product strategy."

### Data processing architecture

"**Starting point**: Need to process incoming data

**Implementation branches**:
1. **Batch**: Process everything at scheduled intervals
   - Simple, predictable load
   - Higher latency acceptable
   - Good for reports, analytics

2. **Stream**: Process items as they arrive
   - Real-time results
   - Complex failure handling
   - Good for user-facing features

3. **Hybrid**: Stream critical items, batch the rest
   - Balances latency and complexity
   - Requires classification logic
   - Good for mixed requirements

4. **Push-down**: Clients pre-process before sending
   - Distributes load
   - Requires client capability
   - Good for resource constraints

**Key insight**: Architecture choice depends on latency requirements, failure tolerance, and resource distribution."

## When to use this skill

- When you notice yourself locked into a single approach without having considered alternatives
- Before committing to a major architectural or design decision
- When you feel tunnel vision setting in and realize adjacent thinking has replaced genuine exploration
- If asked to compare options but only one path currently exists in your analysis
- When creating contingency plans requires understanding what fundamentally different strategies exist
- Before presenting recommendations, to verify you explored meaningfully different directions rather than variations on one theme
- When you catch yourself optimizing a solution before confirming it's the right approach to pursue

## Related Skills

**alternatives** - For generating multiple explanations of the same evidence. Use alternatives when analyzing why something happened or what caused observed patterns. branch generates different paths forward from a single point, while alternatives generates different interpretations of what already happened.