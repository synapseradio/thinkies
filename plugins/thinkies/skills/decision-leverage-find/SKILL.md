---
name: leverage-find
description: Identify high-leverage intervention points where small efforts create disproportionate impact, useful for maximizing ROI, strategic planning, and finding force multipliers
---

# Leverage Find

Discover where small actions create outsized results through amplification, compounding, or removal of bottlenecks.

## Instructions

When finding leverage points:

1. **Map the system**:
   - What are you trying to improve?
   - What are the key components and flows?
   - Where does value get created or destroyed?
   - Sketch the causal relationships

2. **Look for bottlenecks**:
   - What's the limiting factor?
   - Where do things get stuck or slow?
   - What's blocking multiple other things?
   - Removing bottlenecks has multiplier effects

3. **Find amplification points**:
   - Where can one action affect many outcomes?
   - What gets reused or repeated?
   - What do many things depend on?
   - Teaching, tooling, and templates amplify

4. **Identify network effects**:
   - What becomes more valuable as more people use it?
   - Where does one person's contribution help everyone?
   - Documentation, shared tools, standards

5. **Spot compounding opportunities**:
   - What builds on itself over time?
   - Where do small advantages accumulate?
   - Skills, processes, culture, technical foundations

6. **Look for root causes**:
   - What creates many symptoms?
   - Fixing causes beats treating symptoms
   - One fix that prevents many problems

7. **Consider second-order effects**:
   - What enables other improvements?
   - What makes future work easier?
   - Infrastructure and foundations have delayed but large impact

8. **Evaluate leverage ratio**:
   - Effort in vs impact out
   - Account for sustainability and maintenance
   - True leverage should be 10x or better

9. **Watch for false leverage**:
   - Looks high-impact but requires constant effort
   - One-time boost without lasting effect
   - Creates dependencies or technical debt

## Examples

### Finding technical leverage:

"**System**: Team struggling with production bugs

**Initial options** (low leverage):
- Fix bugs one by one (linear, never-ending)
- Add more QA testing (helps but doesn't prevent)
- Write better documentation (symptom treatment)

**Higher leverage investigation**:

**Bottleneck found**: Deploy process takes 2 hours, requires manual steps
- Result: Developers avoid deploying fixes until many accumulate
- Leverage point: Automate deployment (20 hours investment)
- Impact: Enables fast fixes, reduces batch size, faster feedback
- Multiplier: 10x+ (enables continuous improvement)

**Amplification found**: Same types of bugs repeat across services
- Root cause: No shared validation library
- Leverage point: Build shared validation once (40 hours)
- Impact: Every service gets better validation automatically
- Multiplier: 15x (15 services)

**Network effect found**: Knowledge trapped in individual heads
- Leverage point: Implement blameless post-mortems (ongoing, low effort)
- Impact: Each incident improves everyone's understanding
- Compounding: Team gets better at prevention over time

**Highest leverage choice**: Fix deployment first (unblocks other improvements), then shared validation (prevents most common bugs), then post-mortems (continuous learning)"

### Finding organizational leverage:

"**System**: Sales team struggling to close deals

**Linear approaches** (low leverage):
- Hire more salespeople (expensive, slow)
- Offer discounts (erodes margins)
- More customer calls (doesn't scale)

**Leverage investigation**:

**Bottleneck found**: Sales spends 60% of time on deals that don't fit
- Root cause: Marketing generates unqualified leads
- Leverage point: Improve lead qualification (one person, 2 weeks)
- Impact: Sales focuses on good-fit customers
- Multiplier: 2.5x sales efficiency without hiring

**Amplification found**: Salespeople recreating same materials
- Leverage point: Create sales playbook and templates (40 hours once)
- Impact: Every salesperson uses best practices
- Additional: New hires productive faster
- Multiplier: 10x (10 salespeople × faster onboarding)

**Compounding found**: Losing deals due to security questionnaire delays
- Leverage point: Pre-answer common security questions (20 hours)
- Immediate: Faster responses
- Compound: Builds trust, enables larger deals
- Secondary: Can pursue enterprise customers

**Highest leverage**: Lead qualification (immediate 2.5x, enables focus), then sales playbook (multiplies individual effectiveness), then security materials (unlocks new segment)"

### Finding product leverage:

"**System**: Low user activation rate

**Obvious approaches** (moderate leverage):
- Improve onboarding tutorial
- Add more features
- Better UI design

**Leverage investigation**:

**Root cause found**: Users succeed if they complete one key action
- Data shows: Users who connect data source have 80% retention
- Leverage point: Optimize specifically for first connection
- Instead of: Improving everything equally
- Multiplier: Focus creates 5x higher impact

**Network effect found**: Users invite teammates after success
- Leverage point: Make sharing easy after first win
- Impact: Each successful user brings 2-3 others
- Viral coefficient > 1 creates exponential growth

**Bottleneck found**: Email verification blocks 40% of signups
- Users start, never verify, never return
- Leverage point: Allow skip or send verification later
- Impact: 40% more users reach activation moment
- Risk: Some spam, but worth testing

**Template leverage**: 90% of users build same three dashboards
- Leverage point: Provide templates instead of blank slate
- Impact: Faster success, reveals product value immediately
- Multiplier: Every new user benefits

**Highest leverage sequence**:
1. Remove verification bottleneck (40% more reach activation)
2. Add templates for common use cases (faster time to value)
3. Optimize data connection flow (increase conversion)
4. Add sharing after success (viral growth)

This sequence compounds: each step increases the pool for the next step"

### Finding learning leverage:

"**System**: Team needs to improve technical skills

**Low leverage**:
- Send everyone to conferences (expensive, inconsistent)
- Individual online courses (slow, isolated learning)
- Lunch-and-learns (shallow, forgotten quickly)

**Leverage investigation**:

**Amplification point**: Senior engineer knowledge only helps when working together
- Leverage point: Pair programming rotation (infrastructure change)
- Impact: Skills spread across team continuously
- Multiplier: Knowledge compounds with each rotation

**Bottleneck found**: Team doesn't know what they need to learn
- Root cause: No visibility into upcoming challenges
- Leverage point: Quarterly tech radar review (4 hours per quarter)
- Impact: Targeted learning, ahead of need
- Prevention: Avoids scrambling later

**Compounding opportunity**: Team learns same lessons repeatedly
- Leverage point: Document decisions and context (ADRs)
- Impact: Future team learns from past decisions
- Time frame: 5-year value horizon
- Multiplier: Every future team member benefits

**Highest leverage**: Start pair rotation (immediate skill transfer), implement ADRs (builds knowledge base), add tech radar (strategic learning direction)"

## When to use this skill

- Resource constrained situations
- Strategic planning
- Deciding between many options
- Team or organizational improvements
- Technical architecture decisions
- Process improvements
- When effort isn't producing results
- Startup or high-growth contexts
- Maximizing impact of small teams
