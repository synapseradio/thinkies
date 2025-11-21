---
name: attention-anchor
description: Maintain focus points while exploring tangents, useful when investigating requires depth but you need to remember where you started and why
---

# Attention Anchor

Keep track of your original focus while allowing productive exploration.

## Instructions

When anchoring attention:

1. **Set your anchor explicitly**:
   - What am I actually trying to accomplish?
   - What's the core question I'm answering?
   - What decision am I trying to make?
   - "My main goal is X, even as I explore Y"

2. **Notice when you drift**:
   - Am I still working on the original problem?
   - Is this tangent relevant?
   - How far have I wandered?
   - "I started looking at A but now I'm deep into B"

3. **Evaluate tangent value**:
   - Is this exploration helping my original goal?
   - Is this a productive detour or a distraction?
   - Should I follow this thread or return to anchor?
   - "This is interesting but doesn't actually help with my original question"

4. **Mark your trail**:
   - How did I get here from there?
   - What was the chain of reasoning?
   - Can I retrace my steps?
   - "I started with X, which led me to Y, which made me wonder about Z"

5. **Return to anchor periodically**:
   - Does what I just learned change my approach to the original problem?
   - Am I ready to answer the original question?
   - Do I need to keep exploring?
   - "Now that I know this about Y, how does it affect my approach to X?"

6. **Recognize when to change anchor**:
   - Is the original question still the right one?
   - Have I discovered the real problem is different?
   - Should I pivot or persist?
   - "I came here to fix X, but I've learned the real issue is Y"

## Examples

### Setting an anchor:
"My main question is: 'Why does this API call fail intermittently?' As I investigate, I might look at network issues, rate limiting, authentication, and data validation. But every tangent should connect back to answering that core question. If I find myself debugging something else entirely, I need to notice and redirect."

### Noticing drift:
"Wait, I started trying to understand why the tests are flaky, but now I'm refactoring the test utilities to use a different pattern. That's not the same thing. The refactoring might be worthwhile, but it's not helping me understand the flakiness. Let me return to the anchor: why are these tests flaky?"

### Productive tangent:
"I was trying to figure out how to optimize this query, which led me to wonder about the indexing strategy, which made me check the database schema, which revealed that we're missing a key index. This tangent was productive; it's directly relevant to my original goal. The detour helped me find the real issue."

### Unproductive tangent:
"I was investigating a performance issue, got curious about how the caching layer works, went down a rabbit hole reading the cache implementation, and spent 20 minutes on cache eviction policies. Interesting, but not helpful. The performance issue has nothing to do with caching. I lost my anchor."

### Marking the trail:
"Original goal: understand why users are getting logged out. First tangent: session management code. Second tangent: cookie settings. Third tangent: browser compatibility. I'm three layers deep, but I can trace back: browser compatibility affects cookies, cookies store sessions, sessions keep users logged in. Still on track."

### Recognizing pivot moment:
"I came here to fix a bug in the payment flow, but through investigation I've discovered the real problem is that our entire payment flow design is flawed. The 'bug' is actually a symptom. I need to change my anchor from 'fix this bug' to 'redesign this flow.' That's a bigger scope, but it's the real work."

### Using anchor for decision-making:
"I found two interesting approaches while researching: A and B. Both are cool, but returning to my anchor helps me decide. My goal is to reduce latency for this specific API. Approach A reduces latency but is complex. Approach B is elegant but doesn't help latency. My anchor tells me: choose A."

## When to use this skill

- Starting an investigation or research session
- When exploring unfamiliar territory
- While debugging complex issues
- During open-ended problem-solving
- When you feel yourself going down rabbit holes
- Working on something without clear boundaries
- When you keep getting distracted
- In long, exploratory conversations
- When returning to work after an interruption
- Any time you think "wait, what was I doing?"
