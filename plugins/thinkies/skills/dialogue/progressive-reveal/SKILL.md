---
name: progressive-reveal
description: Layer information from simple to complex, building understanding incrementally so learners grasp fundamentals before adding nuance, useful for explanations, teaching, and introducing complex topics
---

# Progressive Reveal

Build understanding layer by layer, starting simple and adding complexity only as foundations solidify.

## Instructions

When revealing progressively:

1. **Start with the simplest true thing**:
   - Find the core concept stripped of caveats
   - Make it concrete and relatable
   - Ensure it's genuinely useful at this level
   - Don't mention complications yet

2. **Confirm understanding before adding**:
   - Check if the foundation makes sense
   - Watch for confusion signals
   - Let the simple version settle
   - Don't rush to complexity

3. **Add one layer at a time**:
   - Introduce complications individually
   - Connect each new layer to what came before
   - Explain why this layer matters now
   - Keep the core idea visible

4. **Signal transitions clearly**:
   - "Now that makes sense..."
   - "There's a complication..."
   - "In practice..."
   - "Building on that..."

5. **Preserve earlier understanding**:
   - Simple version stays true, just incomplete
   - New layers refine, don't invalidate
   - Show how pieces fit together
   - Maintain coherent narrative

6. **Calibrate to response**:
   - If they're ahead, move faster
   - If confused, spend more time
   - If curious about specifics, follow that thread
   - Adapt depth to their needs

## Examples

### Explaining caching:
"**Layer 1 - Core concept**:
'Caching is keeping a copy of something nearby so you don't have to get it from far away every time. Like keeping salt on the table instead of walking to the pantry for every pinch.'

**Layer 2 - The tradeoff**:
'The copy might get stale. The salt stays fresh, but imagine keeping milk on the table. Now you have to decide: how long is your copy good for?'

**Layer 3 - Strategies**:
'Different caching strategies handle staleness differently. Time-based says "this copy is good for 5 minutes." Event-based says "throw it away when the original changes." Your choice depends on how stale you can tolerate and whether you can detect changes.'

**Layer 4 - Real complexity**:
'In distributed systems, you have multiple caches that might get out of sync. Now you're juggling consistency, invalidation timing, and cache stampedes. But it's all variations on that core idea: copies nearby that might get stale.'"

### Explaining a technical decision:
"**Layer 1 - What we did**:
'We split the monolith into separate services for users, orders, and inventory.'

**Layer 2 - Why**:
'Each piece can now scale independently. During holiday sales, we need lots of order processing but user management stays the same. We can add order servers without adding user servers.'

**Layer 3 - Tradeoffs**:
'The downside is these services need to talk to each other over the network. That's slower and can fail in more ways than a function call. So we gained scaling flexibility but added complexity in communication.'

**Layer 4 - How we addressed it**:
'We use message queues for anything that doesn't need an immediate response and circuit breakers to handle failures gracefully. We accept that some operations now take longer but gain the ability to handle 10x traffic spikes.'"

### Teaching a debugging approach:
"**Layer 1 - The basic loop**:
'Debugging is: see the problem, form a guess about the cause, test your guess, repeat.'

**Layer 2 - Making it systematic**:
'The key is making your guesses testable. Instead of "the database is slow," try "the users table query takes more than 100ms." Now you can check if that's true.'

**Layer 3 - Narrowing efficiently**:
'Good guesses divide the problem space. Add logging at the halfway point of your code path. If the problem happens before that point, you've eliminated half the code. Binary search through your system.'

**Layer 4 - When the pattern breaks**:
'This works until you hit race conditions, timing-dependent bugs, or heisenbugs that disappear when observed. Then you need different tools: distributed tracing, sampling, or statistical analysis. But start with the simple loop, it solves most problems.'"

### Introducing a complex system:
"**Layer 1 - What users see**:
'Users upload a file, and we show them insights from it. That's the whole user experience.'

**Layer 2 - What happens internally**:
'We store the file, process it to extract data, run analysis on that data, and generate visualizations. Four steps.'

**Layer 3 - Why it's structured this way**:
'Each step has different requirements. Storage needs reliability. Processing needs CPU. Analysis needs memory. Visualization needs speed. Separate services let us optimize each differently.'

**Layer 4 - How the pieces communicate**:
'Upload triggers a message to the processor. Processor saves results and triggers analysis. Analysis completes and triggers visualization generation. It's a pipeline where each stage is independent but coordinated through messages.'"

## When to use this skill

- Explaining technical concepts
- Onboarding new team members
- Teaching complex topics
- Presenting to mixed audiences
- Writing documentation
- Introducing architectural decisions
- Code reviews with junior developers
- Any time understanding must be built, not dumped
