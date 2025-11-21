---
name: premortem
description: Imagine a decision has failed spectacularly and work backwards to identify what went wrong, surfacing risks and failure modes before they happen
---

# Premortem

Imagine your decision has failed catastrophically, then work backwards to discover what went wrong.

## Instructions

When conducting a premortem:

1. **Set the future state**:
   - Imagine it's 6-12 months from now
   - The decision you're considering has failed badly
   - Not just "didn't work" but "was a disaster"
   - Make the failure vivid and specific

2. **Generate failure stories**:
   - Write the headline: "Project X Failed Because..."
   - Describe what the failure looks like
   - How did stakeholders react?
   - What's the damage?
   - Be creative and pessimistic

3. **Work backwards**:
   - Given this failure, what must have happened?
   - What sequence of events led here?
   - What early warning signs were missed?
   - What assumptions were wrong?

4. **Identify failure modes**:
   - Technical failures
   - People/team failures
   - Process failures
   - External/market failures
   - Timing failures
   - Usually multiple causes compound

5. **Surface hidden assumptions**:
   - What did you assume would go right?
   - What did you assume wouldn't change?
   - What dependencies did you take for granted?
   - What did you not know you needed to know?

6. **Look for preventable vs inevitable**:
   - What could you control?
   - What was outside your control?
   - What were early indicators?
   - Focus mitigation on preventable failures

7. **Design interventions**:
   - What could prevent each failure mode?
   - What early warning systems?
   - What contingency plans?
   - What would you do differently from the start?

8. **Pressure test the plan**:
   - Does your actual plan address these failure modes?
   - Are you over-confident somewhere?
   - What are you still vulnerable to?

## Examples

### Premortem for microservices migration:

"**The future**: It's 12 months from now. The microservices migration has failed catastrophically.

**Failure story**:
'Company announces rollback to monolith after 10-month disaster. Engineering velocity dropped 60%. Three major outages. CTO departed. Team morale at all-time low. Investors questioning technical leadership.'

**Working backwards - What happened?**

**Technical failure path**:
- Distributed tracing was never set up properly
- Debugging production issues took days instead of hours
- Services had circular dependencies nobody mapped
- Data consistency issues led to corruption
- No one understood the full system anymore

**People failure path**:
- Senior engineer who understood monolith left in month 3
- Knowledge was in their head, not documented
- Remaining team struggled with distributed systems
- Hired contractors who made it worse
- Team burned out from constant firefighting

**Process failure path**:
- Migrated everything at once instead of incrementally
- No rollback plan
- Testing didn't catch distributed system issues
- No one owned cross-service concerns
- Communication overhead exploded

**Assumption failures**:
- Assumed team had distributed systems expertise
- Assumed observability tools would be easy to set up
- Assumed services could be independent (wrong boundaries)
- Assumed performance would improve (got worse)
- Assumed we had a scaling problem (we didn't)

**Early warning signs that were missed**:
- First service took 3x longer than estimated
- Team asking questions showed knowledge gaps
- Observability POC revealed tooling complexity
- Load testing showed latency increases
- Team expressed concerns but pushed forward

**What should have prevented this**:

Before starting:
- Validate we actually have the problem microservices solve
- Ensure team has distributed systems experience or training plan
- Prove observability tooling works in POC
- Define service boundaries based on data and team structure

During migration:
- Migrate one service as full learning experience
- Document learnings and update approach
- Create rollback checkpoints
- Stop if early signals are bad
- Measure velocity and system reliability continuously

Safety nets:
- Keep monolith running in parallel initially
- Automated testing for distributed scenarios
- Observability before migration, not after
- Regular architecture review checkpoints
- Clear success/failure criteria to decide continuation"

### Premortem for hiring decision:

"**The future**: 6 months later, this hire was a disaster.

**Failure story**:
'New senior engineer left after 5 months. Delivered nothing production-ready. Created conflicts with team. Left codebase more complex. Lost time and money.'

**Working backwards**:

**Technical mismatch**:
- Their expertise was in different tech stack
- Couldn't adapt to our architecture patterns
- Over-engineered solutions for our scale
- Didn't understand our domain constraints
- Code reviews became arguments

**Culture mismatch**:
- Solo work style in collaborative team
- Dismissed existing code as "legacy"
- Didn't invest in relationships
- Team stopped asking them for help
- Became isolated

**Expectation mismatch**:
- Expected greenfield projects, got maintenance
- Expected architectural authority, team resisted
- Expected different technologies than we use
- Expected autonomy, we needed collaboration
- Expected mentorship role we didn't need

**Process failure**:
- Interview focused on algorithms, not collaboration
- Didn't check cultural fit deeply
- Reference calls were superficial
- Didn't involve team in decision
- Rushed because role was open too long

**Hidden signals missed**:
- Job hopping every 18 months
- In interviews, criticized past teams
- Didn't ask questions about team or codebase
- Portfolio showed individual projects only
- References were vague about teamwork

**What could prevent this**:

Interview process:
- Pair programming session on real codebase problem
- Team lunch to assess cultural fit
- Discuss actual challenges, not hypotheticals
- Deep reference checks on collaboration
- Have team vote on hire

Onboarding design:
- 30-60-90 day goals and checkpoints
- Assigned peer for cultural integration
- Start with small, real problems
- Regular feedback both directions
- Clear expectations in writing

Early warning system:
- Weekly 1:1s in first month
- Team feedback at 30 days
- Review code patterns for alignment
- Monitor relationship health
- Address concerns immediately, not after months"

### Premortem for product launch:

"**The future**: 8 months later, product launch completely failed.

**Failure story**:
'Product shut down after 7 months. Fewer than 100 active users. Burned $2M in development. Team reassigned. Customers uninterested.'

**Working backwards**:

**Market failure**:
- Customers said they wanted it, but didn't actually buy
- Pricing was way off (too high or too low)
- Market timing was wrong
- Competitors launched similar product first with more features
- Didn't solve painful enough problem

**Product failure**:
- Built what we thought users needed, not what they needed
- Too complex for target users
- Missing critical features
- Poor performance at scale
- Incompatible with their existing workflows

**Go-to-market failure**:
- Wrong distribution channel
- Marketing message didn't resonate
- Sales team couldn't explain value
- No one knew how to buy it (procurement friction)
- Support couldn't handle questions

**Assumption failures**:
- Assumed people having problem meant they'd pay
- Assumed we understood customer workflow
- Assumed our solution was differentiated
- Assumed we could reach customers
- Assumed first version would be good enough

**What was missed**:
- Beta users were too polite with feedback
- Didn't test with paying customers
- Didn't validate pricing before building
- Didn't check procurement process
- Didn't have metrics for success

**Prevention strategy**:

Before building:
- Validate willingness to pay (pre-orders, pilots)
- Shadow customers doing the work now
- Test core value prop with prototype
- Map competitive landscape deeply
- Understand buying process

During building:
- Weekly contact with target users
- Monthly usability testing
- Metrics from day one
- Beta with paying customers
- Regular build vs buy checks

Launch criteria:
- 10 customers pre-committed to buy
- Core workflow validated in real environment
- Support processes tested
- Clear metrics for success/failure
- Kill decision criteria defined upfront"

## When to use this skill

- Major decisions or projects
- Before significant investment
- Launching new products or features
- Organizational changes
- Technical architecture decisions
- Hiring key roles
- Mergers or partnerships
- Anytime optimism feels too high
- When stakes are high
- Planning complex initiatives
