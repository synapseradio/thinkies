---
name: cognitive-load
description: Manage mental resources and complexity, useful when overwhelmed, juggling too many concepts, or needing to simplify without losing important nuance
---

# Cognitive Load

Monitor and manage how much you're trying to think about at once.

## Instructions

When managing cognitive load:

1. **Notice overload symptoms** - Recognize when you're losing track of details, when ideas are getting confused, or when thinking feels cluttered and overwhelmed.

2. **Count what you're juggling** - Explicitly inventory how many concepts you're tracking simultaneously, how many constraints you're considering, and how many threads you're following.

3. **Simplify strategically** - Decide what can be tabled for now, what can be written down instead of held in memory, and what can be decided later rather than immediately.

4. **Break down complexity** - Separate work into stages, solve simpler versions first, and distinguish core issues from peripheral details that can be handled separately.

5. **Use external memory** - Write down what doesn't need to be held in working memory, offload tracking to tools rather than mental effort, and distinguish between what you need to remember versus what you can look up.

6. **Recognize when to pause** - Notice when you're too deep in details, when you've lost sight of the larger context, and when stepping back would provide better perspective than continuing forward.

## Examples

### System design overload

"**Overload**: I'm trying to simultaneously think about API design, database schema, error handling, caching strategy, and authentication flow. That's five major concerns at once.

**Symptoms**: I keep forgetting details and confusing which component does what.

**Simplification**: Let me focus on just the API design first, with placeholder assumptions about the rest. Once the API contract is clear, I can tackle each other concern in sequence."

### Edge case proliferation

"**Overload**: This problem has 15 different edge cases I'm trying to account for. My thinking is getting tangled as I try to handle them all simultaneously.

**Simplification**: Let me solve it for the happy path first and verify that works. Then I'll add edge case handling one at a time. I can't hold all of this complexity at once effectively."

### Tracking state mentally

"**Overload**: I'm mentally tracking which files need which changes, what depends on what, what's breaking, and what's fixed. That's too much working memory.

**External memory**: Let me write out a list of files and their status, so I can focus my mind on one change at a time rather than trying to remember everything."

### Function complexity

"**Overload**: This function validates input, transforms data, calls three APIs, handles errors, caches results, and logs events. I can't reason about all of that at once.

**Breaking down**: Let me break it into functions that each do one thing, so I can think about them separately and verify each piece works correctly."

### Abstraction depth

"**Overload**: I've gone four levels deep into this abstraction trying to understand how it works. I've lost context for why I'm even here.

**Stepping back**: Let me come back up to the surface, remember what I'm actually trying to accomplish, and see if I even need to understand this deeply right now. Maybe the interface is all I need."

### Competing optimization goals

"**Overload**: I'm trying to optimize for speed, memory, readability, maintainability, and testability all at once. I can't hold all those goals in mind simultaneously.

**Prioritization**: Let me prioritize readability first, then I'll optimize if profiling shows I need to. That narrows what I need to think about to one primary concern."

### Minimal reproduction

"**Overload**: The real system has authentication, rate limiting, retries, and circuit breakers, but I'm trying to debug a specific issue.

**Strategic reduction**: To understand why this bug is happening, I don't need to think about all of that. Let me build a minimal reproduction that just focuses on the core behavior. Once I understand that, I can add complexity back and verify the fix works in the full system."

## When to use this skill

- When you feel mentally overwhelmed, scattered, or like your thinking is cluttered and unclear
- When you're making mistakes that stem from juggling too many things simultaneously rather than lack of knowledge
- When you lose track of what you're doing or find yourself rereading the same information repeatedly
- When you struggle to explain something clearly because you're trying to communicate too many interconnected pieces at once
- When you get confused by your own thinking or lose the thread of your reasoning
- When you notice yourself trying to optimize for too many competing factors simultaneously
- When simplification feels risky but continuing with current complexity feels unmanageable
- Before starting complex tasks where breaking down the approach would make execution clearer
- When debugging intricate systems where tracking all the moving parts mentally becomes error-prone
