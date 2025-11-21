---
name: fork-detect
description: Recognize critical decision points where paths diverge significantly and the choice shapes everything that follows, preventing drift into default decisions
---

# Fork Detect

Identify moments where you're at a meaningful decision point, even when it doesn't feel like one.

## Instructions

When detecting decision forks:

1. **Notice the choice moment**:
   - You're about to proceed in some direction
   - Feels like the natural next step
   - But pause: is this actually a choice?
   - What else could you do instead?

2. **Identify what makes it a fork**:
   - Paths diverge significantly from here
   - Different paths lead to different outcomes
   - Choice will be harder to reverse later
   - Commits resources or shapes future options
   - Not just "what now" but "what becomes possible"

3. **Map the divergent paths**:
   - What are the distinct directions available?
   - How do they differ?
   - What does each path enable or foreclose?
   - What's the default if you don't choose actively?

4. **Assess reversibility**:
   - How hard to change direction later?
   - One-way doors vs two-way doors
   - What gets locked in?
   - True forks are harder to reverse

5. **Check if you're drifting**:
   - Did you decide, or just continue?
   - Are you making a choice or following momentum?
   - Is "obvious next step" actually obvious?
   - Could you articulate why this path vs others?

6. **Look for hidden forks**:
   - Choices disguised as non-choices
   - "Just" or "simply" often marks hidden decisions
   - "We always" might be unexamined default
   - "Everyone does" might not fit your context

7. **Consider timing**:
   - Is this the right moment to fork?
   - Forking too early commits before information
   - Forking too late wastes effort on wrong path
   - Some forks have a window

8. **Make the fork visible**:
   - Name the decision explicitly
   - Write down the options
   - Share with team or stakeholders
   - Making it visible enables real choice

## Examples

### Detecting architectural fork:

"**Situation**: About to add a feature to existing codebase.

**Initial thought**: 'I'll just add it to the UserService class.'

**Fork detection**:
Wait - this feels like adding to existing structure, but is this actually a fork?

**What makes this a fork**:
- This is the first feature that spans multiple domains
- Where we put it sets a pattern others will follow
- Affects how we think about system boundaries
- Hard to move later once dependencies form

**Divergent paths**:

**Path A**: Add to UserService (default/momentum)
- Pro: Fast now
- Con: Expands responsibility, harder to maintain
- Enables: Continuing monolithic pattern
- Forecloses: Clean service boundaries

**Path B**: Create new BillingService
- Pro: Clear boundaries, focused services
- Con: More files, more structure
- Enables: Future service extraction, clearer ownership
- Forecloses: Simple single service approach

**Path C**: Create shared domain layer
- Pro: Reusable across services
- Con: New architectural pattern to maintain
- Enables: Richer domain model approach
- Forecloses: Simple CRUD patterns

**The actual decision**: How do we want to handle cross-domain features?

This isn't 'where does this code go' - it's 'what architectural direction are we taking?'

**Making it visible**:
- Pause implementation
- Write up three approaches with trade-offs
- Discuss with team
- Choose deliberately, document why
- Now everyone knows this is the pattern"

### Detecting product fork:

"**Situation**: Customer requests a customization.

**Initial reaction**: 'Sure, we can add a configuration flag for that.'

**Fork detection**:
This feels routine, but is this the first of many custom requests?

**What makes this a fork**:
- First request for customer-specific behavior
- Sets precedent for how we handle custom needs
- Affects product complexity and maintainability
- Signals whether we're a product or services company

**Divergent paths**:

**Path A**: Add configuration flag
- Enables: Meeting this customer need
- Forecloses: Product simplicity
- Leads to: More custom requests, configuration complexity
- Long-term: Becomes semi-custom solution

**Path B**: Say no, keep product standard
- Enables: Product focus, simpler codebase
- Forecloses: This deal, maybe others
- Leads to: Clear product identity
- Long-term: Easier to maintain and scale

**Path C**: Build it as standard feature everyone gets
- Enables: Product improvement for all
- Forecloses: Fast custom solution
- Leads to: Generalized feature design
- Long-term: Product gets richer

**The actual decision**: What kind of product company are we?

This isn't 'can we add this feature' - it's 'do we do customizations?'

**Making it visible**:
- Bring to product/leadership team
- Discuss strategy implications
- Set policy for future requests
- Communicate decision criteria
- Document policy so pattern is clear"

### Detecting team fork:

"**Situation**: Senior developer leaving, need to replace.

**Initial plan**: 'Post the same job description, hire similar person.'

**Fork detection**:
This feels like replacement, but is this actually a reshaping moment?

**What makes this a fork**:
- Team dynamics will shift regardless
- Chance to rethink team structure
- Budget exists but doesn't have to be same role
- What we do now shapes team for years

**Divergent paths**:

**Path A**: Hire senior developer replacement
- Maintains current structure
- Needs 3-4 month search
- Preserves technical capability
- Forecloses using budget differently

**Path B**: Hire two junior developers
- Changes team composition
- Faster to hire
- More capacity, less experience
- Requires mentorship model

**Path C**: Promote from within, hire different role
- Grows internal person
- Could hire DevOps or designer instead
- Shows career path
- Changes team capabilities

**Path D**: Don't replace, redistribute work
- Use budget for tooling/contractors
- Smaller team, better equipped
- Tests if role was necessary
- Changes team operating model

**The actual decision**: What does this team need to be?

Not 'who replaces X' but 'what should our team look like?'

**Making it visible**:
- Assess what departing person actually did
- Identify what team needs vs what we had
- Consider strategic direction
- Involve team in discussion
- Choose based on future needs, not past structure"

### Detecting process fork:

"**Situation**: Bug found in production, about to hot-fix it.

**Initial response**: 'Let me push a quick fix directly to production.'

**Fork detection**:
This feels urgent, but is this a choice point about how we operate?

**What makes this a fork**:
- First production incident with new team members
- Sets precedent for emergency response
- Shapes culture around quality vs speed
- Affects trust in processes

**Divergent paths**:

**Path A**: Emergency hotfix, skip process
- Fixes problem now
- Sets precedent: process can be skipped
- Leads to: More process shortcuts
- Long-term: Process becomes optional

**Path B**: Fast-track through CI/CD
- Fix quickly but with checks
- Shows process enables speed
- Leads to: Improving emergency process
- Long-term: Trust in process

**Path C**: Full process despite urgency
- Slower fix, full review
- Shows process is never skipped
- Leads to: Either too slow or better process
- Long-term: Process credibility

**The actual decision**: What do we value under pressure?

Not 'how to fix this bug' but 'what are our principles?'

**Making it visible**:
- Acknowledge the fork: 'We're deciding our culture here'
- Choose based on values, not just expediency
- Document the decision and why
- Use this to improve process for next time
- Make principle explicit for future incidents"

### Detecting learning fork:

"**Situation**: Struggling with new framework, considering going back to old approach.

**Initial thought**: 'This is too hard, let's just use what we know.'

**Fork detection**:
This feels like a practical decision, but is it shaping team capability?

**What makes this a fork**:
- Decision about how team grows vs stays comfortable
- Affects technical options for years
- Shapes team identity
- Influences who we can hire

**Divergent paths**:

**Path A**: Return to old framework
- Immediate productivity
- Stays in comfort zone
- Forecloses: New patterns, modern tools
- Long-term: Technical stagnation

**Path B**: Push through learning curve
- Short-term pain
- Expands capabilities
- Enables: Better tools, market relevance
- Long-term: Growth culture

**Path C**: Split approach
- Use both frameworks
- Reduces risk
- Enables: Migration path
- Long-term: Maintenance burden

**The actual decision**: Does this team learn hard things?

Not 'which framework' but 'what kind of engineers are we?'

**Making it visible**:
- Name the real question
- Discuss team capability goals
- Consider market direction
- Make cultural choice explicit
- Use decision to shape future learning choices"

## When to use this skill

- Before starting implementation
- When something feels routine but might not be
- During planning sessions
- When team is moving fast
- Before committing resources
- When facing "obvious" next steps
- First instance of new situation
- Strategy discussions
- Team structure changes
- Any time you hear "just" or "simply"
