---
name: dialectic
description: Develop stronger ideas by examining thesis and antithesis to reach synthesis, useful for resolving opposing views, refining arguments, finding middle paths, or transcending false dichotomies
---

# Dialectic Reasoning

Move toward truth by examining opposing positions and synthesizing a higher understanding that incorporates valid insights from both.

## Instructions

Work through thesis, antithesis, and synthesis to develop more complete understanding:

1. **State the thesis clearly** - Articulate the initial position with its core arguments, what it explains well, and its strengths.

2. **Develop the antithesis** - Present the opposing position as a genuine alternative view with its own core arguments, not just negation, showing what it explains well and reveals that thesis missed.

3. **Examine the conflict** - Identify where exactly they contradict, what each position gets right or misses, whether they're answering different questions or operating on different assumptions.

4. **Identify deeper truth** - Determine what higher-level understanding resolves the contradiction, whether this is a false dichotomy, whether both are partially right in different contexts, and what the conflict itself reveals.

5. **Construct the synthesis** - Build a new position that incorporates insights from both, transcends the either/or framing, and explains what neither alone could.

6. **Test the synthesis** - Verify it accounts for what each side got right, resolves the original conflict, and identify what new tensions or questions it creates.

## Examples

### Code organization debate:

**Thesis**: "We should organize code by feature. Each feature has its own directory with all its components, styles, tests. This keeps related code together and makes features easy to find and modify."

**Antithesis**: "We should organize code by type. All components in one directory, all styles in another, all tests in another. This makes the architecture clear and enforces separation of concerns."

**Examine conflict**: They disagree about what makes code navigable and maintainable. Feature organization optimizes for changing one feature. Type organization optimizes for understanding architectural layers. Neither is wrong - they're optimizing for different workflows.

**Deeper truth**: The conflict reveals that code organization serves different purposes at different times. Sometimes you're working on a feature, sometimes on a layer. The structure should support both.

**Synthesis**: "Organize by feature at the top level, but maintain consistent internal structure within each feature. Features are directories, but each feature organizes its internals by type in a standard way. This makes features easy to locate while keeping architectural patterns visible. It's not feature vs type - it's feature-containing-types."

**Test**: Does this let you work on one feature without touching others? Yes. Can you still see all components to enforce patterns? Yes, they're in the same place within each feature. New question: How do we handle shared components?

### Technical debt vs velocity:

**Thesis**: "We must pay down technical debt now. The codebase is becoming unmaintainable. Every feature takes longer. We need to stop new features and refactor, or we'll grind to a halt."

**Antithesis**: "We can't afford to stop shipping. Customers need features. Competitors are moving fast. Technical debt is just the cost of moving quickly. Perfect code doesn't matter if we lose market position."

**Examine conflict**: They disagree about timing and priority. Both acknowledge the debt exists. Both acknowledge features matter. They're weighing short-term versus long-term differently. Neither is wrong about the stakes.

**Deeper truth**: This isn't actually debt vs velocity - it's about which debt matters and when. Not all technical debt slows you down equally. Not all features provide equal value. The conflict assumes we must choose between "all debt" or "all features."

**Synthesis**: "Identify which technical debt directly blocks the most valuable features. Pay down only that debt, integrated with feature work. Refactor the authentication layer because three high-value features need it. Leave the old reporting code alone if no one's touching it. Make debt paydown earn its place by unblocking specific value, not as a moral imperative."

**Test**: Can we keep shipping features? Yes, even faster for the ones we unblocked. Are we improving the codebase? Yes, the parts that matter. New question: How do we decide which features are high-value?

### Testing philosophy:

**Thesis**: "Test everything. Full coverage catches bugs before production. Untested code is broken code. The confidence is worth the time investment. Tests are documentation."

**Antithesis**: "Tests have diminishing returns. High coverage creates brittle tests that break on refactors. Test the contract, not the implementation. Many bugs can't be caught by unit tests anyway. Tests have a maintenance cost."

**Examine conflict**: They disagree about the cost-benefit tradeoff. Thesis emphasizes risk reduction. Antithesis emphasizes development friction. Both are right about different types of tests. Neither addresses which tests provide which benefits.

**Deeper truth**: Not all tests provide the same value or cost. Unit tests are cheap but fragile. Integration tests are expensive but catch real issues. The question isn't "how much to test" but "what type of testing for what purpose."

**Synthesis**: "Test at the level of abstraction that matches the risk and change frequency. Core business logic: extensive unit tests. API contracts: integration tests. UI implementation details: minimal testing. Critical paths: end-to-end tests. Areas that rarely change: less investment. The goal is confidence, and different code needs different strategies for that."

**Test**: Does this catch serious bugs? Yes, in high-risk areas. Does it avoid brittleness? Yes, by not testing implementation details. Does it acknowledge resource constraints? Yes, by prioritizing. New question: How do we measure if our testing strategy is working?

### Individual vs team optimization:

**Thesis**: "The best engineers should work on the hardest problems. Maximize their output by giving them challenging work and removing obstacles. This produces the most value - your 10x engineers should work on 10x problems."

**Antithesis**: "Concentrating knowledge in individuals creates bottlenecks and risk. The best engineers should spend time teaching and reviewing. Team capability matters more than individual output. A team of good engineers beats a few great ones."

**Examine conflict**: They disagree about how value is created. Thesis assumes value comes from direct work on problems. Antithesis assumes value comes from team capability. Both acknowledge that great engineers are valuable, but deploy them differently.

**Deeper truth**: This isn't individual vs team - it's about what creates sustainable value. Individual output has short-term impact but creates dependencies. Knowledge sharing has long-term impact but slower immediate results. The conflict assumes these are mutually exclusive.

**Synthesis**: "Great engineers should work on hard problems in a way that builds team capability. Tackle the challenging problem, but pair while doing it. Write the complex code, but structure it to teach others. Review PRs not just for correctness but for learning. The work itself becomes the teaching medium. This isn't choosing between shipping and teaching - it's doing both through the same activities."

**Test**: Do hard problems get solved? Yes, by great engineers. Does the team's capability grow? Yes, through direct involvement. Is knowledge shared? Yes, embedded in the work. New question: How do we create work that naturally facilitates teaching?

## When to use this skill

- When team members advocate for opposing approaches and both arguments seem valid
- Before dismissing a contrary position when you notice it has merit despite disagreeing with it
- When debates become polarized and people talk past each other rather than toward understanding
- When design decisions face competing concerns that each matter rather than one clearly dominating
- Before choosing between options when you suspect the choice itself is the problem
- When strategic planning surfaces different stakeholder priorities that seem incompatible
- When you catch yourself thinking in binary terms and "between extremes" might miss the point
- Before advocating for your position when the other side raises points you can't easily dismiss
- When architectural or philosophical debates generate more heat than light and need reframing
