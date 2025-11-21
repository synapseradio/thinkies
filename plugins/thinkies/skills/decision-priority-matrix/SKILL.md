---
name: priority-matrix
description: Assess tasks across impact and effort dimensions to identify what to work on first, useful for backlog prioritization, resource allocation, and maximizing value delivery
---

# Priority Matrix

Map tasks across impact and effort dimensions to reveal what deserves attention first.

## Instructions

When creating a priority matrix:

1. **List specific options and define impact criteria** - Enumerate 5 to 15 possible actions with enough specificity to evaluate them (like "Add password reset" rather than "improve auth"), then establish what impact means in this context (revenue, users, technical health, team velocity) using consistent criteria across all items while considering both immediate and long-term timeframes.

2. **Estimate effort realistically** - Account for time, people, complexity, and risk including hidden costs like ongoing maintenance, coordination overhead, and learning curves, while considering what else gets blocked or delayed, then validate assumptions with the team who will do the work.

3. **Plot items and interpret quadrants** - Map each option as high or low on both dimensions: high impact with low effort items are rare and valuable (do first), high impact with high effort items are strategic work (plan carefully), low impact with low effort items are quick wins (do if time permits), and low impact with high effort items usually warrant skipping entirely.

4. **Challenge placements and consider dependencies** - Question whether you're overestimating impact because you like an idea or underestimating effort because you don't fully understand it, seek second opinions on placement, recognize that some high-effort items unblock many low-effort ones while some low-impact items are prerequisites for more valuable work, and remember that sequence matters beyond just individual priority.

## Examples

### Technical debt backlog

"**Items to evaluate**: Upgrade authentication library with known security vulnerability, add database indexes for slow queries, refactor user service into microservices, add caching layer, improve test coverage from 40% to 80%, document API endpoints, set up automated backups.

**High impact, low effort** (do first):

Upgrade auth library: Critical security risk that could lead to breach, but well-documented upgrade path makes it 2 to 3 days of work. Immediate priority this week.

Add database indexes: Fixes major performance bottleneck affecting user experience, identified specific queries, implementation is half a day to add the indexes. Do this week.

**High impact, high effort** (strategic planning):

Improve test coverage: Significantly reduces bugs in production and enables confident refactoring, but requires 6 to 8 weeks of ongoing work. Plan phased approach focusing on critical paths first, integrate into sprint planning.

**Low impact, low effort** (quick wins):

Document API: Helps new developers and reduces repetitive questions, takes 1 to 2 days. Good filler work between bigger tasks or for onboarding someone new.

**Low impact, high effort** (avoid):

Microservices refactor: Might improve scalability but that's not our current bottleneck, would take 3 to 4 months with high risk of introducing new problems. Defer until we have actual scaling problems that justify this complexity.

**Placement challenges**: Initially put caching as medium priority, but after recognizing it would fix user-reported slowness, moved to high impact. Realized automated backups should be high impact due to data loss risk even though effort is moderate. Questioned whether microservices truly has the impact we assumed or if we're just attracted to the technology."

### Feature roadmap

"**Quadrant mapping for product features**:

**High impact, low effort**:

Email notifications for order status: Every customer asks for this in support tickets, and we already have email service infrastructure so it's just new templates and triggers. Implement in sprint 1.

**High impact, high effort**:

Mobile app: 60% of traffic comes from mobile web with poor experience, but native app is 3 to 4 month project including app store processes. Plan for Q2, research competitor apps first to avoid missteps.

Real-time inventory sync: Prevents overselling which is major customer complaint causing refunds and reputation damage, but requires new infrastructure and third-party integrations with vendors. Start architecture planning now, recognize this is a foundation for other features.

**Low impact, low effort**:

Dark mode: Small but vocal user request with no business impact evidence, mostly CSS changes taking 2 to 3 days. Nice-to-have when between major features or as onboarding task.

**Low impact, high effort**:

Social media integration: Marketing team wants it but no user demand in feedback or interviews, would require OAuth implementation, content sharing features, and moderation. Skip unless marketing demonstrates clear ROI with data, not just intuition.

**Insights from mapping**: Having two high-impact items in the easy quadrant is unusual and valuable, grab those wins immediately. The high-effort quadrant needs sequencing analysis since inventory sync infrastructure could enable better mobile app features. Questioned social media placement by asking marketing for evidence, confirming impact really is low based on actual user research rather than assumptions."

### Team process improvements

"**Items plotted for team efficiency**:

**High impact, low effort**:

Daily standup: Team is distributed and losing synchronization, causing duplicated work and blocked progress. Takes only 15 minutes per day but catches blockers early and improves coordination. Start tomorrow.

**High impact, high effort**:

Hire senior DevOps engineer: Would unblock deployment automation and reduce incidents significantly, but hiring process takes 3 to 4 months and onboarding another 6 months before full productivity. Start recruiting process now, plan for Q3 impact.

Implement CI/CD pipeline: Enables faster deployments and catches bugs before production, but requires 4 to 6 weeks to build properly and needs DevOps expertise we don't currently have.

**Low impact, high effort**:

Switch to new project management tool: Current tool works adequately and team knows it, new one is prettier but provides no material benefit. This is solving a non-problem, skip it entirely.

**Dependency realization**: CI/CD pipeline depends on DevOps expertise, so sequence is start hire process immediately, then either implement CI/CD when hire is close to starting or use contractor to build it, then new hire maintains and improves the system. Without recognizing this dependency, we might have started CI/CD and struggled, or waited to start hiring."

## When to use this skill

- When evaluating what to work on next from a backlog of options
- Before committing to recommendations for the user, to ensure you're suggesting high-leverage work
- When everything feels urgent and you need objective framework to distinguish true priorities
- To make trade-offs visible between competing options rather than implicit
- When stakeholders request work and you need to evaluate it against existing priorities
- Before planning sprints or quarters to maximize value delivery
- When you notice yourself recommending work based on interest rather than impact
