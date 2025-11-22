---
name: abstraction-level
description: Choose appropriate abstraction levels by evaluating coupling vs flexibility - when to generalize, when to keep concrete
---

# Abstraction Level

Choose the right level of abstraction by evaluating the cost of coupling against the cost of duplication.

## Instructions

When I consider introducing or avoiding an abstraction, I evaluate whether generalization serves the code or just serves an aesthetic preference for DRY.

1. **Assess the duplication cost** - I examine whether the duplicated code is actually causing problems like bugs from inconsistent updates, or whether it's just visually similar, since duplication that doesn't hurt is often cheaper than premature abstraction.

2. **Analyze change patterns** - I review the history and likely future of the similar code to see if these pieces change together for the same reasons or independently for different reasons, as code that changes together belongs together while code that changes separately should stay separate even if it looks similar.

3. **Evaluate coupling cost** - I consider what the proposed abstraction would couple together, asking whether these things should share a fate or whether coupling them will make future changes harder by forcing me to either complicate the abstraction or break it apart later.

4. **Test the abstraction's clarity** - I try to name the abstraction and explain what concept it represents, since if I can only describe it as "the common parts of X and Y" rather than as a meaningful domain concept, it's probably not a real abstraction yet.

5. **Compare refactoring paths** - I weigh whether it's easier to extract an abstraction from concrete duplicated code when the pattern becomes clear, or to dismantle a wrong abstraction that's been built into the system, recognizing that the second path is usually much more expensive.

6. **Recognize false similarity** - I look for ways the similar code might diverge, considering whether apparent duplication is actually two different concepts that happen to look alike right now but will evolve differently as requirements change.

7. **Wait for the rule of three** - I resist abstracting on the second instance and instead wait for the third occurrence to reveal the true pattern, as the first instance is a case, the second is coincidence, and the third confirms the pattern worth abstracting.

## Examples

### Keeping domain validation separate

I'm reviewing an API where two endpoints both validate email addresses, and I'm tempted to extract a shared `validateEmail()` function. However, examining the domains reveals that one endpoint validates user registration emails (which must not already exist and should have strict format requirements) while the other validates contact form emails (which just need basic format checking and can be duplicated). Looking at the change history, user validation has been updated three times for security requirements while contact validation hasn't changed in months. These are similar operations serving different purposes that will evolve independently. Keeping the validation logic separate in each endpoint means changes to registration security don't risk breaking the contact form, and each can be understood in its own context. The superficial similarity would create coupling where none should exist.

### Extracting an overdue abstraction

I notice three API endpoints that each implement retry logic for external service calls with identical exponential backoff algorithms, error handling, and logging. Each implementation has fifteen lines of code duplicated almost exactly, and I've seen bugs where one was updated but the others weren't, creating inconsistent behavior. The change history shows these three have been updated together every time retry behavior needed adjustment. I can name the abstraction clearly as `retryWithBackoff()` and it represents a genuine domain concept rather than just "shared code." Extracting this abstraction actually reduces coupling rather than creating it, because currently these endpoints are implicitly coupled through their duplicated implementation, but the coupling is invisible and fragile. The abstraction makes the shared behavior explicit and ensures consistency, while each endpoint remains free to compose it differently or pass different parameters.

### Avoiding premature framework building

I'm working on the first background job in a new system and I'm tempted to build a generic job framework with base classes, lifecycle hooks, error handling strategies, and retry mechanisms to handle future jobs elegantly. However, there's currently only one job type and no clarity on what the next ones will need. Building the framework now means making assumptions about what flexibility will be valuable, and those assumptions are likely wrong since they're based on imagination rather than actual requirements. Instead, I implement this single job concretely with straightforward error handling and logging specific to its needs. When the second job arrives, I resist the urge to abstract and note the differences. By the third job, the actual patterns have emerged, I can see which parts truly vary and which are genuinely common, and I can extract abstractions that serve real needs rather than hypothetical ones. The concrete implementations are easy to refactor once the pattern is clear, while a premature framework would be fighting me the whole time.

## When to use this skill

- I catch myself suggesting an abstraction reflexively because two things look similar without evaluating whether they should actually be coupled
- I'm about to recommend extracting shared code without checking whether the similar pieces change together or independently
- I notice I'm justifying an abstraction with "we might need flexibility for..." without concrete evidence that the flexibility will be valuable
- I'm proposing to keep code duplicated without articulating why the duplication cost is acceptable
- I find myself unable to name an abstraction except as "the common parts of X and Y"
- I'm about to create a base class, utility function, or shared module without confirming that the third similar case exists
- I realize I'm optimizing for code appearance or aesthetic preferences rather than for actual maintenance cost and change patterns

## Related Skills

- `trade-space` - Evaluate competing design options when choosing abstraction level
- `complexity-surface` - Assess whether abstraction reduces or increases overall complexity
- `dependency-graph` - Understand what the proposed abstraction would couple together
