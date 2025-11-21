---
name: theme-find
description: Identify unifying concepts and common threads that run through multiple observations or ideas, useful for making sense of diverse feedback, understanding what really matters, or finding the signal in noise
---

# Theme Find

Discover recurring patterns and unifying concepts that connect multiple separate observations.

## Instructions

When finding themes:

1. **Collect instances** - Gather examples, observations, or data points without categorizing yet, including things that seem unrelated.

2. **Look for repetition** - Identify what keeps coming up across different contexts, sources, or over time.

3. **Notice variation** - Observe how the same thing appears differently, what common element exists in different forms, and what idea lives beneath different words.

4. **Name the theme** - Articulate the essence that repeats by trying multiple names until you find clear, specific language that captures what makes it meaningful.

5. **Test the theme** - Verify it explains most instances, predicts where else you'd see this, and check for counter-examples or whether it's multiple themes overlapping.

6. **Explore relationships between themes** - Determine which themes appear together or oppose each other, which is most fundamental, and what hierarchy or structure exists.

## Examples

### Finding themes in user feedback:
"**Individual feedback**:
- 'The button was hard to find'
- 'I didn't know what would happen'
- 'The error message was confusing'
- 'I wasn't sure if it worked'
- 'I had to ask someone how to do this'
- 'The settings were overwhelming'

**Surface theme**: Usability problems.

**Looking deeper**:
- Hard to find, didn't know, wasn't sure = **lack of confidence**
- Confusing message, had to ask = **unclear communication**
- Overwhelming settings = **too much complexity**

**Core theme**: Users feel uncertain. They're making decisions without enough information to feel confident.

**Validation**: This predicts we'd also hear 'I was afraid to try it' or 'I used the workaround instead' - and we do.

**Insight**: The problem isn't any specific UI element. It's that the system doesn't help users feel sure of themselves."

### Finding themes in code issues:
"**Various bugs reported**:
- Race condition in checkout flow
- Inconsistent state after network interruption
- Duplicate records when user clicks twice
- Lost data during concurrent edits
- Cache invalidation happening too late

**Initial grouping**: These seem like different problems.

**Looking for patterns**:
- Race condition, duplicate records, concurrent edits = **timing**
- Inconsistent state, cache invalidation = **synchronization**
- Network interruption, lost data = **partial failures**

**Unifying theme**: All involve managing state across time and multiple actors. The system assumes sequential, complete operations.

**Core insight**: We're missing a coherent strategy for handling concurrency and partial failures. Each bug fix is point solution to a systemic problem.

**What this reveals**: Need to design for distributed state management, not patch individual race conditions."

### Finding themes in project challenges:
"**Team struggles**:
- Unclear requirements from stakeholders
- Frequent mid-sprint scope changes
- Disagreements about technical approach
- Rework due to misunderstood goals
- Difficulty estimating tasks

**Theme exploration**:
- Unclear requirements + mid-sprint changes = **shifting understanding**
- Disagreements + misunderstood goals = **alignment gaps**
- Difficulty estimating = **uncertainty**

**Deeper theme**: We're treating discovery as failure instead of process. Every 'change' is seen as someone getting it wrong initially.

**Counter-theme present**: Some uncertainty is inherent in new work.

**Synthesis**: The struggle isn't that we don't know everything upfront - it's that our process assumes we should. Need to design for learning, not just execution."

### Finding themes in system behavior:
"**Performance observations**:
- Page load varies wildly (200ms to 5s)
- Some users report fast, others slow
- Performance degrades over session duration
- Certain features always slow, others usually fast
- Weekend performance better than weekday

**Theme hunt**:
- Wild variation = not a simple bottleneck
- User-dependent = **contextual factors**
- Degrades over time = **accumulation**
- Feature-specific + time-dependent = **combination of factors**

**Emerging theme**: Performance isn't about the system itself, it's about system state. Fast when fresh, slow when loaded.

**Specific themes**:
- Memory accumulation (session duration)
- Data volume (user-dependent)
- Shared resources (weekday vs weekend)

**Meta-theme**: The system doesn't manage its own state well. It degrades rather than maintains performance."

## When to use this skill

- When you have diverse feedback or observations and need to identify what conceptually unifies them
- Before concluding "there's no pattern here" when faced with seemingly unrelated information
- When qualitative data feels overwhelming and you need to name what keeps recurring
- When deciding priorities and you need to understand what concerns keep appearing across stakeholders
- After gathering research and before making recommendations, to identify the central ideas
- When multiple people say different things but you sense they're pointing at the same underlying issue
- Before treating each piece of feedback as unique when patterns might reveal systemic themes
- When you need to distinguish signal from noise by recognizing what recurs versus what's random

## Related Skills

**connect-dots** - For discovering mechanical relationships and causal connections. Use connect-dots when you need to understand how things influence each other, trace cause-effect chains, or map system interactions. theme-find focuses on identifying what conceptually unifies observations, while connect-dots focuses on discovering how things mechanistically relate and interact.
