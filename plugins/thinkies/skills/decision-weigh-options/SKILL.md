---
name: weigh-options
description: Systematically evaluate trade-offs between different choices by mapping costs, benefits, and hidden consequences to make informed decisions
---

# Weigh Options

Compare alternatives by systematically evaluating their trade-offs across multiple dimensions.

## Instructions

When weighing options:

1. **List your options clearly**:
   - Name each option specifically
   - Include the "do nothing" option if relevant
   - Usually 2-5 options for meaningful comparison
   - "Option A: [specific approach]"

2. **Identify evaluation dimensions**:
   - What factors matter for this decision?
   - Consider multiple perspectives: cost, time, risk, complexity, reversibility, team impact
   - Don't just look at obvious factors
   - "What are we actually optimizing for?"

3. **Map trade-offs for each option**:
   - **Benefits**: What do we gain?
   - **Costs**: What do we lose or pay?
   - **Risks**: What could go wrong?
   - **Constraints**: What does this require?
   - **Second-order effects**: What else changes?

4. **Rate significance honestly**:
   - Not all factors weigh equally
   - Major vs minor differences
   - Deal-breakers vs preferences
   - Be specific: "saves 2 weeks" not "faster"

5. **Look for hidden trade-offs**:
   - What's not immediately visible?
   - Long-term vs short-term
   - Team morale, technical debt, flexibility
   - "What will we be living with?"

6. **Consider reversibility**:
   - How hard to undo if wrong?
   - Reversible decisions can be bolder
   - Irreversible decisions need more care
   - "Is this a one-way door?"

7. **Check your values**:
   - Which trade-offs are you willing to make?
   - What matters most in this context?
   - Does this align with principles?

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

- Choosing between alternative solutions
- Architecture decisions
- Resource allocation choices
- Buy vs build decisions
- Prioritization conflicts
- Hiring decisions
- Process changes
- Any decision with meaningful trade-offs
