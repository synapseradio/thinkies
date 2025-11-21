---
name: leverage-find
description: Identify high-leverage intervention points where small efforts create disproportionate impact, useful for maximizing ROI, strategic planning, and finding force multipliers
---

# Leverage Find

Discover where small actions create outsized results through amplification, compounding, or removal of bottlenecks.

## Instructions

When finding leverage points:

1. **Map the system and identify bottlenecks** - Understand what you're trying to improve by sketching key components, flows, and causal relationships, then locate limiting factors where things get stuck or slow down, since removing bottlenecks that block multiple other things creates multiplier effects.

2. **Find amplification and network effects** - Look for points where one action affects many outcomes through reuse or repetition, identify what many things depend on (like teaching, tooling, templates, or documentation), and spot where one person's contribution helps everyone or where value increases as more people participate.

3. **Spot compounding opportunities and root causes** - Identify what builds on itself over time through small advantages that accumulate (skills, processes, culture, technical foundations), distinguish root causes that create many symptoms from surface symptoms themselves, and consider second-order effects where foundational work enables other improvements.

4. **Evaluate leverage ratio and watch for false leverage** - Compare effort invested against impact produced while accounting for sustainability and maintenance costs, aiming for true leverage of 10x or better, while avoiding approaches that look high-impact but require constant effort, provide one-time boosts without lasting effect, or create dependencies and technical debt.

## Examples

### Technical system improvement

"**System**: Engineering team struggling with frequent production bugs.

**Low leverage approaches** (linear effort): Fix bugs one by one as they appear, add more QA testing to catch issues, write better documentation explaining workarounds.

**Bottleneck investigation**: Deploy process takes two hours and requires manual steps, causing developers to batch fixes rather than deploy immediately, resulting in large releases with poor isolation of issues.

**Leverage point identified**: Automate deployment pipeline.
- Investment: 20 hours of engineering work
- Impact: Enables fast fixes, reduces batch size, creates faster feedback loops
- Multiplier: 10x or more by enabling continuous improvement culture

**Amplification investigation**: Same validation bugs repeat across 15 different microservices because each team reimplements validation logic.

**Leverage point identified**: Build shared validation library once.
- Investment: 40 hours to build and document
- Impact: Every service gets better validation automatically when they adopt it
- Multiplier: 15x immediate (15 services), ongoing as new services use it

**Network effect investigation**: Knowledge about system behavior and failure modes is trapped in individual developer heads.

**Leverage point identified**: Implement blameless post-mortem process for incidents.
- Investment: Ongoing but low effort per incident
- Impact: Each incident improves everyone's understanding of the system
- Compounding: Team collectively gets better at prevention over time

**Highest leverage sequence**: Fix deployment bottleneck first since it unblocks rapid iteration, then introduce shared validation library to prevent most common bug category, then establish post-mortems for continuous learning."

### Organizational efficiency

"**System**: Sales team struggling to close deals despite sufficient leads.

**Linear approaches** (expensive, slow): Hire more salespeople, offer discounts that erode margins, increase call volume without addressing conversion.

**Bottleneck investigation**: Sales representatives spend 60% of time on deals with poor product fit because marketing generates unqualified leads.

**Leverage point identified**: Improve lead qualification criteria and process.
- Investment: One person, two weeks to redesign qualification
- Impact: Sales focuses time on good-fit customers with higher close rates
- Multiplier: 2.5x sales efficiency without hiring

**Amplification investigation**: Each salesperson recreates the same presentation materials, proposals, and objection responses from scratch.

**Leverage point identified**: Create comprehensive sales playbook with templates.
- Investment: 40 hours once to document best practices
- Impact: Every current salesperson uses proven approaches, new hires become productive faster
- Multiplier: 10x (10 salespeople plus faster onboarding)

**Compounding investigation**: Losing enterprise deals when security questionnaire responses take weeks because answers aren't documented.

**Leverage point identified**: Pre-answer common security and compliance questions.
- Investment: 20 hours to document
- Immediate impact: Faster enterprise deal cycles
- Compound impact: Builds trust, enables larger deals, unlocks new customer segments
- Secondary effect: Can now pursue enterprise segment that was previously inaccessible

**Highest leverage sequence**: Lead qualification for immediate 2.5x efficiency gain, sales playbook to multiply individual effectiveness, then security documentation to unlock enterprise segment."

### Product activation

"**System**: User activation rate is low despite signup growth.

**Moderate leverage approaches**: Improve onboarding tutorial, add more features, redesign UI throughout the product.

**Root cause investigation**: Data analysis reveals users who complete one specific action (connecting a data source) have 80% retention, while others have 20% retention.

**Leverage point identified**: Optimize the product experience specifically for first successful data connection.
- Instead of: Improving everything equally
- Focus: One critical action that predicts success
- Multiplier: 5x higher impact through concentration of effort

**Bottleneck investigation**: Email verification blocks 40% of signups who never verify and never return to the product.

**Leverage point identified**: Allow users to skip verification or send it after first value moment.
- Impact: 40% more users reach the activation moment
- Trade-off: Some spam risk, but worth testing

**Template investigation**: Analysis shows 90% of successful users build the same three dashboard types.

**Leverage point identified**: Provide pre-built templates instead of blank slate.
- Impact: Users reach success faster and see product value immediately
- Multiplier: Every new user benefits from what previous users discovered

**Network effect investigation**: Users who experience success invite an average of 2-3 teammates.

**Leverage point identified**: Make sharing friction-free immediately after first win.
- Impact: Each successful user brings additional users
- Viral coefficient above 1 creates exponential growth

**Highest leverage sequence**: Remove verification bottleneck (40% more users reach activation moment), add templates for common use cases (faster time to value), optimize data connection flow (increase conversion of those who start), enable easy sharing after success (viral growth). This sequence compounds because each step increases the pool for the next step."

## When to use this skill

- When resources are constrained and you need maximum impact from limited capacity
- Before committing to plans that require significant effort to determine if there are higher-leverage alternatives
- When current efforts aren't producing proportional results despite hard work
- To evaluate competing priorities and identify which will create multiplicative rather than additive value
- When planning how to help the user, to find the intervention that unlocks the most value
- Before recommending the most obvious solution, to check if there's a leverage point being missed
- When you notice yourself suggesting linear solutions to systemic problems
