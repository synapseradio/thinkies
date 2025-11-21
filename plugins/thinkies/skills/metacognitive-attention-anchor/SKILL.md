---
name: attention-anchor
description: Maintain focus points while exploring tangents, useful when investigating requires depth but you need to remember where you started and why
---

# Attention Anchor

Keep track of your original focus while allowing productive exploration.

## Instructions

When anchoring attention:

1. **Set your anchor explicitly** - State clearly what you're actually trying to accomplish, what core question you're answering, or what decision you're trying to make before beginning exploration.

2. **Notice when you drift** - Periodically check whether you're still working on the original problem, whether the current tangent is relevant, and how far you've wandered from your starting point.

3. **Evaluate tangent value** - Assess whether each exploration helps your original goal, whether it's a productive detour or a distraction, and whether to follow the thread or return to anchor.

4. **Mark your trail** - Track the chain of reasoning that led from your anchor to your current position, making it possible to retrace steps or explain the connection.

5. **Return to anchor periodically** - After each exploration, assess how what you learned changes your approach to the original problem, whether you're ready to answer the original question, or whether you need to keep exploring.

6. **Recognize when to change anchor** - Identify when the original question is no longer the right one, when investigation reveals the real problem differs from what you started with, and when to pivot rather than persist.

## Examples

### Setting clear anchor

"**Anchor**: Why does this API call fail intermittently?

As I investigate, I might look at network issues, rate limiting, authentication, and data validation. Every tangent should connect back to answering that core question. If I find myself debugging something else entirely, I need to notice and redirect."

### Noticing drift

"**Drift detected**: I started trying to understand why the tests are flaky, but now I'm refactoring the test utilities to use a different pattern. That's not the same thing. The refactoring might be worthwhile, but it's not helping me understand the flakiness.

**Returning to anchor**: Why are these tests flaky?"

### Productive tangent

"**Anchor**: How to optimize this query

**Trail**: Query optimization → indexing strategy → database schema → discovered missing key index

**Assessment**: This tangent was productive. It's directly relevant to my original goal. The detour helped me find the real issue - the missing index explains the slow query performance."

### Unproductive tangent

"**Anchor**: Investigate performance issue

**Trail**: Performance → caching layer → cache implementation → 20 minutes on eviction policies

**Assessment**: Interesting, but not helpful. The performance issue has nothing to do with caching. I lost my anchor and spent time on something irrelevant to the original problem."

### Tracking investigation depth

"**Anchor**: Understand why users are getting logged out

**Current position**: Three layers deep
- Layer 1: Session management code
- Layer 2: Cookie settings
- Layer 3: Browser compatibility

**Trail check**: Browser compatibility affects cookies, cookies store sessions, sessions keep users logged in. Still on track - each layer connects to the anchor."

### Recognizing pivot points

"**Original anchor**: Fix bug in payment flow

**Discovery**: Through investigation, the real problem is that our entire payment flow design is flawed. The bug is actually a symptom of deeper architectural issues.

**New anchor**: Redesign payment flow architecture

This is a bigger scope, but it's the real work that needs doing."

### Using anchor for decisions

"**Anchor**: Reduce latency for this specific API

**Options found**:
- Approach A: Reduces latency but adds complexity
- Approach B: Elegant solution but doesn't improve latency

**Decision**: My anchor tells me to choose A. Despite the complexity, it's the only option that addresses the actual goal."

## When to use this skill

- When starting any investigation or research session where exploration might lead in multiple directions
- When you notice yourself going down rabbit holes or exploring tangents without clear purpose
- When working on open-ended problems without natural boundaries or clear stopping points
- When you find yourself thinking "wait, what was I doing?" or losing track of your original purpose
- When debugging complex issues where following one thread often reveals others worth investigating
- When returning to work after an interruption and needing to reestablish focus
- When exploring unfamiliar territory where interesting discoveries might pull you away from your goal
- When you keep getting distracted by related but ultimately tangential concerns
- During long conversations or investigations where maintaining direction over time is challenging
