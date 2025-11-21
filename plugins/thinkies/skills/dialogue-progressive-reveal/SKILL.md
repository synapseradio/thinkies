---
name: progressive-reveal
description: Layer information from simple to complex, building understanding incrementally so learners grasp fundamentals before adding nuance, useful for explanations, teaching, and introducing complex topics
---

# Progressive Reveal

Build understanding layer by layer, starting simple and adding complexity only as foundations solidify.

## Instructions

When revealing progressively:

1. **Start with the simplest true version** - Find the core concept stripped of qualifications and edge cases. Make it concrete and immediately applicable, verifying it's genuinely useful at this level before saving complications for later layers.

2. **Check understanding before layering** - Confirm the foundation makes sense by watching for confusion or uncertainty. Let simple versions settle in before adding complexity, resisting the urge to rush toward comprehensive explanations.

3. **Add complexity one layer at a time** - Introduce each complication separately rather than bundling multiple qualifications together. Connect new layers explicitly to established concepts, explaining why each matters while keeping the core visible through additions.

4. **Mark transitions between layers** - Signal shifts with phrases like "Now that makes sense..." or "There's a complication..." or "In practice..." to help the learner track where they are in the progression.

5. **Preserve what came before** - Ensure earlier layers stay true though incomplete, so new information refines understanding rather than contradicting it. Show how layers connect to maintain narrative coherence throughout the explanation.

6. **Adjust to the learner** - Accelerate when they demonstrate they're ahead, slow down when signals suggest confusion, follow their curiosity into specific areas, and match depth to their demonstrated need rather than your planned structure.

## Examples

### Technical concept
"**Layer 1 - Core mechanism**:
'Caching means keeping a copy nearby instead of fetching from the source each time. Like salt on the table rather than walking to the pantry every pinch.'

**Layer 2 - The cost**:
'Copies can become stale. Salt stays fresh, but milk on the table spoils. You're deciding: how long is this copy valid?'

**Layer 3 - Strategy variations**:
'Time-based caching says "good for 5 minutes." Event-based says "discard when source changes." The choice depends on staleness tolerance and whether you can detect changes.'

**Layer 4 - Distributed scenarios**:
'Multiple caches create synchronization problems. You're managing consistency, invalidation timing, and cache stampedes. Still the same core: nearby copies that age.'"

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

- When explaining a concept that has important nuances but dumping all qualifications upfront would overwhelm
- Before answering a user question where the simple answer is useful but incomplete
- When you notice yourself about to say "well, it's complicated" without offering a starting point
- When introducing technical concepts to users who may have varying levels of expertise
- Before presenting architectural decisions that involve multiple layers of reasoning
- When the user asks a question that has a genuinely simple answer at one level and important complications at another
- To avoid the trap of either oversimplifying or overwhelming with comprehensive detail
- When onboarding users to complex systems where they need to be productive quickly but will need deeper understanding later
