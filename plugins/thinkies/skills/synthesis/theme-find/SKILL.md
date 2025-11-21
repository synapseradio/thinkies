---
name: theme-find
description: Identify unifying concepts and common threads that run through multiple observations or ideas, useful for making sense of diverse feedback, understanding what really matters, or finding the signal in noise
---

# Theme Find

Discover recurring patterns and unifying concepts that connect multiple separate observations.

## Instructions

When finding themes:

1. **Collect instances**: What are the individual pieces you're looking at?
   - Gather examples, observations, or data points
   - Don't categorize yet, just collect
   - Include things that seem unrelated

2. **Look for repetition**:
   - What keeps coming up?
   - What's mentioned in different contexts?
   - What appears across different sources?
   - What recurs over time?

3. **Notice variation**:
   - How does the same thing appear differently?
   - What's the common element in different forms?
   - What's the idea beneath different words?

4. **Name the theme**:
   - What's the essence that repeats?
   - Try multiple names to find the right fit
   - Use clear, specific language
   - Capture what makes it meaningful

5. **Test the theme**:
   - Does it explain most instances?
   - Does it predict where else you'd see this?
   - Are there counter-examples?
   - Is it actually multiple themes overlapping?

6. **Explore relationships between themes**:
   - Which themes appear together?
   - Which themes seem to oppose each other?
   - Which is most fundamental?
   - What's the hierarchy or structure?

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

- Analyzing qualitative data or feedback
- Making sense of multiple bug reports
- Understanding recurring problems
- Finding what really matters in a discussion
- Synthesizing research findings
- Identifying root causes
- Understanding team dynamics
- Making sense of complex situations
- Deciding what to prioritize
