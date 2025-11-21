---
name: premortem
description: Imagine a decision has failed spectacularly and work backwards to identify what went wrong, surfacing risks and failure modes before they happen
---

# Premortem

Imagine your decision has failed catastrophically, then work backwards to discover what went wrong.

## Instructions

When conducting a premortem:

1. **Set the future failure state** - Imagine it's 6 to 12 months from now and the decision has failed badly (not just "didn't work" but "was a disaster"), making the failure vivid and specific with details about stakeholder reactions and damage, then write the headline describing what happened.

2. **Work backwards through failure modes** - Given this catastrophic outcome, trace what sequence of events must have led here and what early warning signs were missed, identifying technical failures, people and team failures, process breakdowns, external or market shifts, and timing issues, since failures usually compound from multiple causes rather than single points.

3. **Surface hidden assumptions and preventable causes** - Examine what you assumed would go right, what you assumed wouldn't change, what dependencies you took for granted, and what you didn't know you needed to know, then distinguish what you could control from what was outside your control to focus mitigation on preventable failures.

4. **Design interventions and pressure test the plan** - For each identified failure mode, determine what could prevent it, what early warning systems could detect it, what contingency plans could contain it, and what you would do differently from the start, then check whether your actual plan addresses these risks or whether you're still vulnerable due to overconfidence.

## Examples

### Infrastructure migration

"**The future**: 12 months from now, our microservices migration has failed catastrophically.

**Failure headline**: 'Company announces rollback to monolith after 10-month disaster. Engineering velocity dropped 60%. Three major outages. CTO departed. Team morale at all-time low. Investors questioning technical leadership.'

**Working backwards - what happened?**

**Technical failure path**: Distributed tracing was never properly implemented, making debugging take days instead of hours. Services had circular dependencies nobody mapped upfront. Data consistency issues led to corruption. System became too complex for anyone to fully understand.

**People failure path**: Senior engineer who understood the monolith left in month three, taking undocumented knowledge with them. Remaining team lacked distributed systems expertise. Hired contractors who made architecture worse. Team burned out from constant firefighting.

**Process failure path**: Migrated everything at once instead of incremental rollout. No rollback plan existed. Testing didn't catch distributed system issues. Nobody owned cross-service concerns. Communication overhead exploded.

**Assumption failures**: Assumed team had distributed systems expertise (they didn't), assumed observability tools would be easy to add (they weren't), assumed services could be truly independent (wrong boundaries), assumed performance would improve (it got worse), assumed we had a scaling problem (we didn't actually need microservices).

**Early warning signs missed**: First service took three times longer than estimated. Team questions revealed knowledge gaps. Observability proof-of-concept showed tooling complexity. Load testing revealed latency increases. Team expressed concerns but momentum pushed forward anyway.

**Prevention strategy**:

Before starting: Validate we actually have the problem microservices solve, ensure team has distributed systems experience or create training plan, prove observability tooling works in realistic proof-of-concept, define service boundaries based on actual data flows and team structure.

During migration: Migrate one service as full learning experience, document learnings and update approach based on reality, create rollback checkpoints at each phase, establish clear stop criteria if early signals are bad, measure velocity and reliability continuously rather than assuming improvement.

Safety nets: Keep monolith running in parallel initially, create automated testing for distributed scenarios, implement observability before migration not after, schedule regular architecture review checkpoints, define clear success and failure criteria upfront to enable objective decision about continuation."

### Key hire decision

"**The future**: 6 months later, this hire was a disaster.

**Failure headline**: 'New senior engineer left after 5 months. Delivered nothing production-ready. Created conflicts with team. Left codebase more complex. Lost time and money.'

**Working backwards**:

**Technical mismatch**: Their expertise was in different technology stack. Couldn't adapt to our architecture patterns. Over-engineered solutions for our scale. Didn't understand our domain constraints. Code reviews became arguments about approach rather than collaboration.

**Culture mismatch**: Solo work style in collaborative team environment. Dismissed existing code as inferior without understanding context. Didn't invest in building relationships. Team stopped asking them for help. Became isolated.

**Expectation mismatch**: Expected greenfield projects, got maintenance work. Expected architectural authority, but team resisted changes. Expected different technologies than we actually use. Expected autonomy, but we needed collaboration. Expected to be mentor when we didn't need that role.

**Process failure**: Interview focused on algorithm skills rather than collaboration ability. Didn't assess cultural fit deeply enough. Reference calls were superficial checkbox exercise. Didn't involve team in decision. Rushed hiring because role was open too long and pressure was mounting.

**Hidden signals missed during interview**: Job history showed moves every 18 months. In interviews, primarily criticized past teams rather than discussing collaboration. Didn't ask questions about our team dynamics or codebase. Portfolio showed only individual projects, no team work. References were vague about teamwork when asked specifically.

**Prevention strategy**:

Interview redesign: Include pair programming session on real codebase problem, have team lunch to assess cultural fit naturally, discuss actual current challenges rather than hypotheticals, conduct deep reference checks specifically about collaboration and conflict resolution, give team voting power on hire decision.

Onboarding design: Set clear 30-60-90 day goals and checkpoints in writing, assign peer specifically for cultural integration not just technical onboarding, start with small real problems rather than big architecture projects, establish regular two-way feedback from day one, write down explicit expectations about working style.

Early warning system: Weekly one-on-ones in first month to surface issues early, gather team feedback at 30-day mark, review code patterns for alignment with team practices, monitor relationship health indicators, address concerns immediately rather than hoping they resolve over months."

### Product launch

"**The future**: 8 months later, our product launch completely failed.

**Failure headline**: 'Product shut down after 7 months. Fewer than 100 active users. Burned $2M in development budget. Team reassigned to other projects. Customers showed no interest despite initial positive feedback.'

**Working backwards**:

**Market failure**: Customers said they wanted it in interviews but didn't actually buy when available. Pricing was completely wrong (either too high or too low). Market timing was off. Competitors launched similar product first with more features and better go-to-market. Problem wasn't painful enough for customers to change behavior.

**Product failure**: Built what we thought users needed rather than validating real needs. Too complex for target users to understand value. Missing critical features that customers assumed would be included. Performance degraded at realistic scale. Didn't integrate with their existing workflows, creating adoption friction.

**Go-to-market failure**: Used wrong distribution channel for this buyer. Marketing message didn't resonate with actual decision makers. Sales team couldn't explain value proposition clearly. Nobody understood how to navigate their procurement process. Support team couldn't handle technical questions, eroding trust.

**Assumption failures**: Assumed people having a problem meant they'd pay to solve it (they wouldn't), assumed we understood customer workflow from brief interviews (we didn't), assumed our solution was differentiated (it wasn't enough), assumed we could reach customers easily (we couldn't), assumed first version would be good enough to gain traction (it wasn't).

**Missed validations**: Beta users were too polite with feedback and didn't reveal real issues. Didn't test with paying customers who have actual budget constraints. Didn't validate pricing before building. Didn't understand procurement process complexity. Didn't establish success metrics upfront, so couldn't recognize failure early enough to pivot.

**Prevention strategy**:

Before building: Validate willingness to pay through pre-orders or paid pilots, shadow customers doing the work today to understand real workflow, test core value proposition with prototype before full build, map competitive landscape deeply including why alternatives are currently winning, understand complete buying process including procurement and legal.

During building: Maintain weekly contact with target users throughout development, run monthly usability testing with realistic scenarios, implement metrics from day one to measure actual usage patterns, conduct beta with paying customers who have skin in the game, perform regular build versus buy checks to validate continued investment.

Launch criteria: Secure 10 customers pre-committed to purchase, validate core workflow in their real environment, test support processes with realistic question load, establish clear metrics for success and failure with specific thresholds, define kill decision criteria upfront while objective rather than when emotionally invested."

## When to use this skill

- Before major decisions or significant project investments to surface hidden risks
- When optimism about a plan feels unusually high and assumptions aren't being questioned
- Before launching new products, features, or organizational changes with substantial resources committed
- When planning complex initiatives where failure modes aren't obvious from normal analysis
- To pressure test your recommendations before presenting them to the user
- When you notice yourself making confident assertions about outcomes without examining what could go wrong
- Before committing to architectural decisions or key hires that are difficult to reverse
