---
name: trade-space
description: Map design trade-offs across dimensions (simple/flexible, fast/safe, etc.) when choosing between approaches
---

# Trade-Space

Systematically map what each approach optimizes for and what it sacrifices to make informed design choices.

## Instructions

When I face a design decision, I map the trade-space by identifying the fundamental tensions between competing qualities and understanding what each option gains and loses.

1. **Identify relevant dimensions** - I determine which qualities actually matter for this specific decision, such as simplicity versus flexibility, performance versus safety, or explicitness versus conciseness, rather than evaluating every possible dimension that might apply to any decision.

2. **Map each option's position** - I plot where each candidate approach falls on the dimensions that matter, recognizing that an approach optimized for performance will necessarily sacrifice safety checks, or that maximizing flexibility adds complexity, making the costs and benefits explicit.

3. **Recognize fundamental tensions** - I identify which dimensions are in opposition such that improving one necessarily degrades another, understanding that these aren't weaknesses to eliminate but inherent constraints that define the boundaries of what's possible.

4. **Weight by context** - I consider which dimensions matter most for this specific situation by examining the problem domain, team capabilities, and system requirements, as a dimension that's critical in one context may be irrelevant in another.

5. **Surface hidden costs** - I look beyond the obvious trade-offs to find second-order effects, asking what happens when the system evolves, when requirements change, or when new team members encounter the code, as these delayed costs often exceed the immediate ones.

6. **Test the map** - I validate my understanding by explaining why certain combinations are impossible or why specific approaches succeed in some contexts but fail in others, ensuring I've identified real constraints rather than assumed limitations.

7. **Choose with eyes open** - I select an approach based on which trade-offs align with the actual priorities, documenting what I'm optimizing for and what I'm deliberately sacrificing so future changes can be made with the same understanding.

## Examples

### Choosing error handling strategy

I'm deciding how to handle errors in a new API service. I identify that the relevant dimensions are explicitness (whether errors are visible in type signatures), ergonomics (how much ceremony is required), and control flow (how errors propagate). Mapping the options, I see that exceptions are ergonomic with clean success paths but hide failure modes in the type system, Result types make errors explicit and composable but add ceremony to every operation, and error codes are simple but easy to ignore and lose context. The tension is that making errors explicit in types requires more syntax, while implicit propagation (exceptions) reduces type safety. Given this is a new service where understanding all failure modes matters more than development speed, and the team is experienced with functional patterns, I choose Result types. I'm deliberately trading ergonomics for explicitness because in this context, the cost of unhandled errors exceeds the cost of additional syntax, and I document this so we don't undo it later for "convenience" without reconsidering the original reasoning.

### Choosing state management approach

I'm implementing a feature that needs to share data across multiple React components. I map the dimensions: coupling (how much components know about each other), boilerplate (setup and maintenance cost), debugging (how easy to trace state changes), and scope (how broadly the state is accessible). Prop drilling creates tight parent-child coupling with no boilerplate but becomes unmaintainable beyond two levels. React Context decouples components with minimal setup but makes it hard to track what triggered updates and exposes state to entire subtrees. Redux fully decouples with excellent debugging but requires significant boilerplate and makes state global. The fundamental tension is that reducing coupling increases indirection, making state flow harder to trace. Looking at context, this feature is isolated to one section of the app, used by five components at varying depths, and needs to be understood by junior developers. I choose Context because the moderate coupling is acceptable for this scope, the minimal boilerplate matters more than perfect debugging in a non-critical feature, and the simpler mental model fits the team's experience level. I'm trading some debugging clarity for reduced complexity, which aligns with this feature being low-risk and the team being small.

### Choosing data structure representation

I'm modeling a collection of users where I need to look them up by ID and iterate through all of them. The dimensions are access speed (lookup performance), iteration order (predictability), memory overhead (space cost), and mutation safety (how errors manifest). An array gives ordered iteration and low memory overhead but makes lookup O(n) and index-based access fragile to reordering. A Map provides O(1) lookup and maintains insertion order but uses more memory and makes index-based access impossible. A normalized structure (Map of entities plus array of IDs) optimizes both but doubles the maintenance burden and creates consistency risks. The tension is that optimizing lookup speed requires giving up array simplicity, while maintaining multiple representations risks desynchronization. Examining context, users are looked up frequently in event handlers, the collection has hundreds of items, iteration order doesn't matter for the features using it, and this is a mature part of the codebase unlikely to change frequently. I choose a Map because the O(1) lookup directly solves the performance issue I'm observing, the memory overhead is negligible for hundreds of items, and the lack of ordering isn't used by current features. I'm trading ordered access and some memory for lookup performance, which fits the actual usage patterns rather than optimizing for theoretical future needs.

## When to use this skill

- I'm recommending an approach based on a single criterion like "performance" or "simplicity" without acknowledging what it sacrifices
- I'm presenting multiple options but only listing features rather than explaining what each optimizes for and what it costs
- I'm defaulting to patterns from my training data or "best practices" without examining whether their trade-offs fit this specific context
- I'm deep in implementation details or syntax debates before establishing what qualities actually matter for this decision
- I'm surprised when a solution I proposed has significant downsides that should have been predictable from the trade-offs
- I'm treating design choices as objectively right or wrong rather than as different positions in a trade-space with context-dependent value
- I catch myself saying something is "better" without specifying what dimension it's better on and what it's worse on

## Related Skills

- `abstraction-level` - Choose the right level of abstraction after understanding the simplicity/flexibility trade-off
- `blast-radius` - Evaluate the scope dimension of trade-offs by understanding change impact
