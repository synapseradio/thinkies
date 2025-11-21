---
name: weigh-options
description: Systematically evaluate trade-offs between different choices by mapping costs, benefits, and hidden consequences to make informed decisions
---

# Weigh Options

Compare alternatives by systematically evaluating their trade-offs across multiple dimensions.

## Instructions

When weighing options:

1. **List your options clearly** - Name each alternative specifically, including the "do nothing" option if relevant. Usually 2-5 options provide meaningful comparison without overwhelming the analysis.

2. **Identify evaluation dimensions** - Determine which factors actually matter for this decision by considering multiple perspectives like cost, time, risk, complexity, reversibility, and team impact. Ask what you're truly optimizing for beyond the obvious factors.

3. **Map trade-offs for each option** - Systematically catalog what you gain (benefits), what you lose or pay (costs), what could go wrong (risks), what this requires (constraints), and what else changes as a consequence (second-order effects).

4. **Rate significance honestly** - Distinguish major differences from minor ones and deal-breakers from preferences. Not all factors weigh equally, so be specific with estimates like "saves 2 weeks" rather than vague terms like "faster."

5. **Look for hidden trade-offs** - Surface what's not immediately visible by examining long-term versus short-term consequences, impacts on team morale, accumulation of technical debt, and future flexibility. Ask what you'll be living with months or years from now.

6. **Consider reversibility** - Assess how difficult it would be to undo this choice if it proves wrong. Reversible decisions permit bolder moves, while irreversible decisions demand more careful deliberation.

7. **Check your values** - Clarify which trade-offs you're willing to make in this context, what matters most given your principles and constraints, and whether this choice aligns with your core commitments.

## Examples

### Weighing technical approaches:

"**Option A: Microservices architecture**

Benefits:
- Independent scaling of components
- Team autonomy on services
- Technology flexibility per service

Costs:
- Operational complexity increases significantly
- Need distributed tracing and monitoring
- 3-6 months migration timeline
- Requires ops expertise we need to hire

Risks:
- Distributed debugging is harder
- Data consistency challenges
- Could slow development velocity initially

Reversibility: Hard (one-way door)

**Option B: Modular monolith**

Benefits:
- Keeps operational simplicity
- Fast deployment and debugging
- Can refactor to services later if needed
- Works with current team skills

Costs:
- Shared scaling (all or nothing)
- Requires discipline to maintain boundaries
- Single deployment coordinates all changes

Risks:
- Boundaries might erode over time
- May hit scaling limits sooner

Reversibility: Medium (can extract services later)

**Trade-off analysis**:
- A optimizes for scale/autonomy at cost of complexity
- B optimizes for velocity/simplicity at cost of flexibility
- Current constraint: team size (5 engineers)
- Key question: Do we have scaling problem or complexity problem?
- Decision leans toward B: we're not at scale that justifies A's complexity cost"

### Weighing product decisions:

"**Option A: Build custom solution**

Benefits:
- Exactly fits our needs
- Full control over features
- No vendor lock-in
- Competitive differentiation

Costs:
- 4 months engineering time
- Ongoing maintenance burden
- Delayed other features
- Need to build expertise

Risks:
- Might underestimate complexity
- Opportunity cost on core product
- Could build wrong thing

**Option B: Use third-party service**

Benefits:
- Live in 2 weeks
- Proven, maintained by vendor
- Focus our time on core value
- Includes features we'd skip

Costs:
- Monthly cost scaling with usage
- Depends on vendor reliability
- Limited customization
- Potential data sharing concerns

Risks:
- Vendor could change pricing or shut down
- Might not grow with our needs
- Integration complexity

**Trade-off analysis**:
- A trades time now for control later
- B trades money for speed and focus
- Key factor: Is this core to our value proposition?
- If no: B is likely better (buy commodity)
- If yes: A might be worth it (build differentiator)"

### Weighing organizational changes:

"**Option A: Hire senior engineer**

Benefits:
- Immediate expertise and productivity
- Can mentor junior team
- Handles complex problems independently

Costs:
- Higher salary (160k vs 100k)
- Longer hiring timeline (3-4 months)
- Might leave faster for next opportunity

**Option B: Hire two junior engineers**

Benefits:
- More total capacity
- Usually stay longer
- Faster hiring process
- Lower salary cost

Costs:
- Need more mentorship time
- Slower to productivity
- Can't solve complex problems alone
- Might not know what they don't know

**Trade-off analysis**:
- A is better if: bottleneck is complexity, team needs direction
- B is better if: bottleneck is capacity, have mentorship bandwidth
- Current situation: complex architecture problems blocking progress
- Decision: A addresses root problem; B might amplify mentorship burden"

## When to use this skill

- When presenting multiple solution approaches to the user without making the decision for them
- When you find yourself drawn to one option but recognize valid concerns about it
- Before recommending a technical architecture that carries significant trade-offs
- When the user asks "which is better" and the honest answer is "it depends on what you value"
- When you notice yourself oversimplifying a decision by ignoring costs or risks
- Before resource allocation decisions where different stakeholders care about different outcomes
- When buy versus build decisions require balancing immediate cost against long-term control
- To help the user understand why you're recommending a particular approach by showing what you're trading away
