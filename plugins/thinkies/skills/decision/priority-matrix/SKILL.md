---
name: priority-matrix
description: Assess tasks across impact and effort dimensions to identify what to work on first, useful for backlog prioritization, resource allocation, and maximizing value delivery
---

# Priority Matrix

Map tasks across impact and effort dimensions to reveal what deserves attention first.

## Instructions

When creating a priority matrix:

1. **List all options**:
   - What are the possible things to do?
   - Include both obvious and less obvious choices
   - Aim for 5-15 items for meaningful comparison
   - Be specific: "Add password reset" not "improve auth"

2. **Define impact clearly**:
   - Impact on what? Revenue, users, technical health, team velocity?
   - Use consistent criteria across all items
   - Think about timeframe: immediate vs long-term
   - Consider both positive impact and avoided negative

3. **Estimate effort realistically**:
   - Time, people, complexity, risk
   - Include hidden costs: maintenance, coordination, learning
   - What else gets blocked or delayed?
   - Check assumptions with team

4. **Plot on the matrix**:
   ```
   High Impact │ INVEST    │ STRATEGIC
               │ (Do First)│ (Plan Carefully)
   ────────────┼───────────┼──────────────
   Low Impact  │ QUICK WINS│ AVOID
               │ (If Easy) │ (Waste)
               └───────────┴──────────────
                Low Effort   High Effort
   ```

5. **Interpret the quadrants**:
   - **High Impact, Low Effort**: Do these first (rare and valuable)
   - **High Impact, High Effort**: Important strategic work (plan carefully)
   - **Low Impact, Low Effort**: Quick wins if time permits
   - **Low Impact, High Effort**: Usually skip these

6. **Challenge the easy quadrant placements**:
   - Are you overestimating impact because you like the idea?
   - Are you underestimating effort because you don't understand it?
   - Get second opinions on placement

7. **Consider dependencies**:
   - Some high-effort items unblock many low-effort ones
   - Some low-impact items are prerequisites
   - Sequence matters, not just priority

8. **Revisit regularly**:
   - Impact and effort change over time
   - New information shifts placement
   - Completed work opens new options

## Examples

### Prioritizing technical debt:

"**Items to evaluate**:
1. Upgrade outdated authentication library (security vulnerability)
2. Add database indexes for slow queries
3. Refactor user service into microservices
4. Add caching layer
5. Improve test coverage from 40% to 80%
6. Document API endpoints
7. Set up automated backups

**Plotting**:

**High Impact, Low Effort** (Do First):
- Item 1: Upgrade auth library
  - Impact: Critical security risk
  - Effort: 2-3 days, well-documented upgrade path
  - Decision: Immediate priority

- Item 2: Add database indexes
  - Impact: Fixes major performance bottleneck
  - Effort: Half day to identify and add
  - Decision: Do this week

**High Impact, High Effort** (Strategic):
- Item 5: Improve test coverage
  - Impact: Reduces bugs, enables confident refactoring
  - Effort: 6-8 weeks ongoing work
  - Decision: Plan phased approach, critical paths first

**Low Impact, Low Effort** (Quick Wins):
- Item 6: Document API
  - Impact: Helps new developers, reduces questions
  - Effort: 1-2 days
  - Decision: Good filler work between bigger tasks

**Low Impact, High Effort** (Avoid):
- Item 3: Microservices refactor
  - Impact: Might improve scalability (but not current bottleneck)
  - Effort: 3-4 months, high risk
  - Decision: Defer until we have actual scaling problems

**Re-evaluated**:
- Item 4: Add caching - moved from medium to high impact after realizing it would fix user-reported slowness
- Item 7: Automated backups - realized this should be high impact (data loss risk) even though it's medium effort"

### Prioritizing features:

"**Quadrant mapping**:

**High Impact, Low Effort**:
- Email notifications for order status
  - Every customer asks for this
  - Use existing email service, just new templates
  - Do in sprint 1

**High Impact, High Effort**:
- Mobile app
  - 60% of traffic is mobile web
  - 3-4 month project with app store deployment
  - Plan for Q2, research competitors first

- Real-time inventory sync
  - Prevents overselling (major customer complaint)
  - Requires new infrastructure, third-party integrations
  - Start architecture planning now

**Low Impact, Low Effort**:
- Dark mode
  - Small but vocal user request
  - CSS changes mostly, 2-3 days
  - Nice-to-have when between major features

**Low Impact, High Effort**:
- Social media integration
  - Marketing wants it but no user demand
  - OAuth, content sharing, moderation needed
  - Skip unless marketing can show clear ROI

**Insights**:
- Two high-impact items in easy quadrant is unusual (grab them)
- High-effort quadrant needs sequencing: inventory sync unblocks mobile app features
- Questioned social media placement: is impact really low or are we missing something?"

### Prioritizing team improvements:

"**Items plotted**:

**High Impact, Low Effort**:
- Daily standup (team is distributed, losing sync)
  - Effort: 15 min/day
  - Impact: Catches blockers early, improves coordination
  - Start tomorrow

**High Impact, High Effort**:
- Hire senior DevOps engineer
  - Impact: Unblocks deployment automation, reduces incidents
  - Effort: 3-4 month hiring process, 6 month onboarding
  - Start recruiting now, plan for Q3 impact

- Implement CI/CD pipeline
  - Impact: Faster deployments, fewer bugs to production
  - Effort: 4-6 weeks to build, need DevOps expertise
  - Dependencies: May need that hire first, or could start with contractor

**Low Impact, Low Effort**:
- Switch to new project management tool
  - Current one works fine, new one is prettier
  - Skip - solving non-problem

**Realization**: CI/CD is dependent on DevOps hire, so sequence is: start hire process (now) → implement CI/CD (when hire is close or use contractor) → hire comes in to maintain and improve"

## When to use this skill

- Backlog grooming
- Sprint planning
- Quarterly planning
- Resource allocation
- Deciding what not to do
- When everything feels urgent
- Evaluating requests from stakeholders
- Making trade-offs visible
