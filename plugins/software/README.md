# Software

Systematic reasoning frameworks for working with code. These skills help Claude understand unfamiliar systems, make sound design decisions, validate correctness, and change code safely.

## What's Included

Ten specialized skills organized into five categories: understanding code structure, making design choices, validating changes, improving quality, and anticipating consequences.

## The Skills

### Understanding
How do I make sense of this code?

- **codebase-cartography** - Map unfamiliar codebases by identifying landmarks, boundaries, and flows
- **trace-flow** - Follow data and control flow through execution paths
- **dependency-graph** - Map coupling, boundaries, and architectural layers

### Deciding
Which approach should I choose?

- **trade-space** - Map design trade-offs across multiple dimensions
- **abstraction-level** - Choose appropriate abstraction by evaluating coupling vs flexibility

### Validating
Is this change safe and correct?

- **blast-radius** - Map impact radius of code changes across the system
- **edge-finder** - Systematically discover edge cases through boundary analysis

### Improving
Where is the complexity, and what should I do about it?

- **complexity-surface** - Identify where complexity lives and distinguish essential from accidental

### Anticipating
What could go wrong, and how do I migrate safely?

- **failure-modes** - Systematically enumerate how code can fail
- **migration-path** - Design safe migration strategies for breaking changes

## When to Use These Skills

**Exploring unfamiliar code**
Start with `codebase-cartography` to build a map, then use `trace-flow` to follow key paths, and `dependency-graph` to understand coupling.

**Making breaking changes**
Use `blast-radius` to find what will be affected, `migration-path` to design the transition, and `failure-modes` to identify risks.

**Choosing between approaches**
Apply `trade-space` to map the dimensions you're trading off, `abstraction-level` to evaluate whether abstraction helps, and `complexity-surface` to understand complexity implications.

**Validating correctness**
Run `edge-finder` to discover boundary cases, `failure-modes` to enumerate failure scenarios, and `trace-flow` to verify behavior with specific inputs.

**Refactoring safely**
Start with `dependency-graph` to understand current coupling, use `blast-radius` to map change impact, and `complexity-surface` to distinguish essential from accidental complexity.

## Examples

### Understanding a New Codebase
```
Task: "Add a feature to this API service"

1. codebase-cartography - Map the overall structure
2. trace-flow - Follow a similar feature through the system
3. dependency-graph - Understand what depends on what

Result: Grounded understanding before proposing changes
```

### Proposing a Breaking Change
```
Task: "Rename this function for clarity"

1. blast-radius - Find all callers and usage sites
2. migration-path - Design the transition strategy
3. failure-modes - Identify what could break during migration

Result: Safe migration plan rather than risky direct change
```

### Evaluating Alternatives
```
Task: "Should we cache this data or compute it fresh?"

1. trade-space - Map trade-offs (latency vs freshness vs complexity)
2. failure-modes - Enumerate cache-related failure scenarios
3. complexity-surface - Evaluate accidental complexity introduced

Result: Decision grounded in actual trade-offs
```

### Validating Implementation
```
Task: "This validation logic handles all cases"

1. edge-finder - Systematically explore boundary cases
2. failure-modes - Enumerate failure scenarios
3. trace-flow - Verify behavior with edge case inputs

Result: Discovery of unconsidered cases before production
```

---

**Version:** 1.0.0
**Author:** synapseradio

*Ground your reasoning. Verify your claims. Change code safely.*
