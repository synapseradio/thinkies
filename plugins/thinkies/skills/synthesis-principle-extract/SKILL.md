---
name: principle-extract
description: Distill fundamental truths from complex information and specific examples, useful for moving from observations to understanding, creating guidelines from experience, or finding what's really true beneath the details
---

# Principle Extract

Identify the fundamental truths and generalizable rules that underlie specific observations or examples.

## Instructions

When extracting principles:

1. **Start with specifics** - Gather concrete examples with real outcomes and conditions, focusing on what actually happened rather than theories.

2. **Ask why it's true** - Determine what made this work or fail, what conditions were necessary, what would make it false, and what the underlying mechanism is.

3. **Generalize carefully** - Remove context-specific details while keeping what's essential, then test whether it applies elsewhere and predicts new situations.

4. **State the principle** - Express it clearly and actionably, avoid vague language, include boundaries of applicability, and explain the underlying reason.

5. **Test the principle** - Verify it explains all your examples, predicts things you haven't seen, and check for counter-examples or whether it's actually several principles.

6. **Check the level** - Assess whether it's too specific with unnecessary details, too broad and loses meaning, or at the right level of abstraction.

## Examples

### Extracting from debugging experience:
"**Specific case**: We had a bug that only appeared in production. Turned out to be a timing issue that didn't show up in development because our test data was small.

**Why this happened**:
- Development had different conditions than production
- The difference was invisible until it caused a failure
- We assumed similarity when environments were actually different

**Generalizing**:
- Not just about data size
- Not just about production vs development
- About hidden differences in conditions

**Principle**: Systems behave differently under different conditions. When debugging, look for environmental differences first, especially those invisible in normal operation.

**Boundary**: Applies when behavior changes across environments. Doesn't apply to pure logic bugs that appear everywhere.

**Deeper principle**: Test against reality, not assumptions about similarity. What you think is 'the same' often isn't.

**Actionable form**: When something works in one place and fails in another, map the differences in conditions before diving into code. The failure is telling you about an assumption you didn't know you had."

### Extracting from code reviews:
"**Observation**: Pull requests with better descriptions get better feedback and merge faster.

**Looking deeper**:
- Better descriptions = reviewer understands context
- Understanding context = can give useful feedback
- Useful feedback = fewer revision cycles
- Fewer cycles = faster merge

**Extracting principle**: Communication quality early in a process reduces total time spent. The time spent explaining upfront is recovered many times in reduced back-and-forth.

**Testing the principle**:
- Applies to: design docs, bug reports, feature requests
- Predicts: Good user stories reduce development time
- Counter-case: Over-documentation can also slow things down

**Refined principle**: Invest communication effort at decision points where others need to act on your information. Clarity at handoff points multiplies efficiency.

**Why it's true**: Misunderstanding compounds. Each person who misunderstands makes decisions that others build on. Front-loaded clarity prevents cascading rework."

### Extracting from system design:
"**Specific experience**: We built a feature with lots of configuration options. Users found it confusing. We removed options and made it opinionated. Users loved it.

**Why this worked**:
- Options require users to understand trade-offs
- Most users don't have context for those decisions
- Default behavior is easier than choice
- Opinionated design guides users

**First principle**: Fewer choices is often better UX.

**Too simple - let's go deeper**:
- When is choice good? When users have information to decide.
- When is choice bad? When it requires expertise users don't have.

**Better principle**: Make decisions on behalf of users when you have more information than they do. Let users decide when they have context you lack.

**Testing**:
- Predicts: Expert modes work when users are actually experts
- Predicts: Progressive disclosure works (show options as users learn)
- Counter-example: Some domains require user choice (privacy settings)

**Refined principle**: The right amount of configuration matches user expertise and the importance of the decision. High-stakes or domain-specific decisions need user input. Technical implementation details should have good defaults.

**Why it's true**: Cognitive load. Every decision costs attention. Only ask users to spend attention where they have relevant information and the decision matters to their goals."

### Extracting from project failures:
"**Specific failure**: Project ran over deadline because we kept finding edge cases we hadn't considered.

**Pattern across failures**:
- Underestimated complexity
- Discovered hidden requirements late
- Each fix revealed more problems

**First extraction**: We need better estimation.

**That's not a principle, that's advice. Go deeper.**

**Why estimation failed**:
- We estimated based on happy path
- Edge cases are numerous but individually small
- They compound in ways that aren't linear

**Principle**: Complexity hides in interaction between simple parts. Estimating components individually misses the integration cost.

**Testing**:
- Predicts: Integration always takes longer than expected
- Predicts: Well-defined interfaces reduce this
- Explains: Why rewriting seems faster than modifying (fewer hidden interactions)

**Actionable principle**: When estimating, budget for unknown unknowns proportional to the number of integration points. Simple features in complex systems carry hidden costs.

**Meta-principle**: Your first explanation is usually about symptoms. Keep asking why until you hit something that predicts other situations."

## When to use this skill

- When you've observed a pattern multiple times but haven't articulated why it occurs
- Before creating guidelines or rules, to ensure they capture the underlying truth rather than surface patterns
- When teaching others and you need to move from "here's what happened" to "here's why this matters"
- Before making design decisions based on past experience, to verify the lesson actually applies
- When building mental models and you need to distill what's fundamental versus contextual
- After project retrospectives when you want reusable knowledge, not just a story about what happened
- When you catch yourself following advice without understanding why it works or when it doesn't
- Before advocating for a practice, to distinguish timeless principles from temporary solutions
