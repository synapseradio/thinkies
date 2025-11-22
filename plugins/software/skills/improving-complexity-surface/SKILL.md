---
name: complexity-surface
description: Identify where complexity lives and distinguish essential from accidental complexity to avoid harmful simplification
---

# Complexity Surface

Understand which complexity is inherent to the problem and which is introduced by our solutions, because removing essential complexity breaks systems while tolerating accidental complexity wastes cognitive resources.

## Instructions

When I encounter code that feels complex, I analyze whether that complexity is essential or accidental before suggesting changes.

1. **Inventory all complexity** - I systematically identify every source of complexity in the code under examination, including conditional logic, state management, error handling, data transformations, and abstraction layers, because I cannot evaluate what I haven't acknowledged.

2. **Trace complexity to its source** - For each complexity I find, I ask whether it exists because the problem domain requires it or because our implementation choices introduced it, following the thread back to see if it reflects business rules, real-world constraints, or simply our approach to solving the problem.

3. **Identify essential complexity** - I mark complexity as essential when removing it would eliminate required functionality, violate domain constraints, or lose important distinctions that exist in the problem space, recognizing that some problems are legitimately complex and simplifying the code would only hide this reality.

4. **Identify accidental complexity** - I mark complexity as accidental when it stems from implementation choices like framework limitations, historical decisions, premature abstraction, or unnecessary indirection, noting that this complexity could theoretically be reduced without changing what the system does.

5. **Examine complexity surfaces** - I look at where complexity is exposed versus where it's hidden, distinguishing between complexity that's appropriately abstracted away, complexity that must be visible at boundaries because it reflects real choices users or systems make, and complexity that leaks through poor abstractions revealing implementation details that shouldn't matter.

6. **Test proposed simplifications** - Before recommending any simplification, I verify whether it would preserve all essential properties by asking what we would lose, whether that loss matters to the domain, and whether we're truly reducing complexity or just moving it elsewhere or hiding it.

7. **Map the cost-benefit** - I evaluate whether each complexity earns its keep by considering the cognitive load it imposes against the value it provides, recognizing that essential complexity has high value despite its cost, while accidental complexity has cost without proportional value.

## Examples

### Over-engineered abstraction hiding domain reality

I'm examining a payment processing system that uses a deeply abstract `TransactionProcessor` interface with methods like `process(data: GenericPayload): Result`. Following the implementation, I discover it handles credit cards, bank transfers, and digital wallets, but the abstraction forces all three into a generic shape, hiding that these payment methods have fundamentally different failure modes, timing characteristics, and refund semantics. The complexity of payment domain rules is essential - credit cards can be charged immediately but reversed later, bank transfers are slow but final, digital wallets require balance checks. The abstraction is accidental complexity that makes the code look simple while actually making it harder to handle each payment type correctly. I recommend making the essential complexity explicit with distinct types for each payment method, accepting that the code will look more complex because the domain actually is complex.

### Appropriate handling of essential complexity

I'm reviewing a calendar scheduling system with intricate logic for handling recurring events, time zones, and daylight saving transitions. The code has many conditional branches checking whether events recur, whether they cross DST boundaries, and how to resolve conflicts. This feels complex, but tracing it to the source reveals each branch maps to a real constraint: events can recur on different patterns, time zones have political boundaries that change, DST transitions happen at different times in different places. This is essential complexity reflecting the genuine difficulty of time-based scheduling. The current implementation makes this complexity explicit and testable rather than hiding it. Simplifying it would mean either losing functionality or pushing the complexity into runtime bugs. I recommend keeping the explicit complexity but improving its organization through careful decomposition into well-named functions that make the domain logic readable.

### Accidental complexity from historical decisions

I'm analyzing an API client that wraps every method call in three layers: a retry wrapper, a caching wrapper, and a logging wrapper. Each wrapper exists for a valid reason, but together they create accidental complexity through ceremony. Examining the implementation reveals that the wrappers were added at different times and could be unified into a single request pipeline with configurable behavior. The essential complexity is that network calls can fail, responses should be cached under certain conditions, and operations need observability. The accidental complexity is having three separate abstraction layers that duplicate concerns like error handling. I trace through adding a new endpoint and confirm that developers must remember to apply all three wrappers in the correct order. I recommend consolidating into a single configurable request handler that maintains all the essential behavior while eliminating the accidental ceremony.

## When to use this skill

- I catch myself suggesting simplification without first identifying which complexity is domain-required versus implementation-introduced
- I'm about to recommend removing code that looks complicated without verifying whether that complication maps to real-world complexity
- I notice I'm favoring abstractions that make code look simple over code that makes essential complexity explicit and understandable
- I'm treating all complexity as bad and something to eliminate rather than distinguishing between necessary and unnecessary complexity
- I find myself recommending patterns from my training data without analyzing whether they fit the essential complexity of this specific problem
- I'm about to suggest "just" doing something simpler without mapping what would be lost or where the complexity would move
- I realize I cannot explain which parts of the complexity are inherent to the problem versus artifacts of how we chose to solve it

## Related Skills

- `abstraction-ladder` - Move between levels of abstraction to find where complexity is appropriately hidden versus inappropriately leaked
- `dependency-graph` - Understand how complexity propagates through coupled components
- `codebase-cartography` - Map the system to identify where complexity concentrates and why
- `blast-radius` - Evaluate the impact of simplification by understanding what depends on current complexity
