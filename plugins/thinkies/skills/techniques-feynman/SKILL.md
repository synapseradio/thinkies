---
name: feynman
description: Learn deeply and validate understanding by explaining concepts in simple terms, useful for learning new domains, identifying knowledge gaps, preparing to teach, or debugging confusion
---

# Feynman Technique

Learn and validate understanding by explaining concepts as if teaching someone with no background knowledge.

## Instructions

The technique has four steps that reveal what you truly understand versus what you only think you understand:

1. **Choose and explain the concept** - Pick the specific concept you want to understand and write out an explanation as if teaching a bright 12-year-old, using plain language with concrete examples and analogies.

2. **Identify gaps** - Mark where you struggled to explain, fell back on jargon or hand-waving, or can't answer questions a curious student would ask.

3. **Fill the gaps** - Return to source material for unclear areas, research specific questions you couldn't answer, find better analogies for abstract concepts, and work through examples until the mechanism is clear.

4. **Simplify and refine** - Remove unnecessary complexity, find clearer analogies, organize logically, and test whether someone could actually learn this from your explanation.

## Examples

### Understanding async/await:

**First attempt**: "Async/await is syntactic sugar for promises. You use async to mark a function and await to pause execution until the promise resolves."

**Gap identified**: What does "pause execution" actually mean? What's happening during the pause? Why do we need this?

**After filling gaps**: "When JavaScript hits code that takes time - like fetching data from a server - it has two choices: wait for the result (blocking everything else) or continue doing other work and come back later. Async/await is the 'come back later' approach made readable.

Think of it like a restaurant: The waiter (JavaScript) takes your order (starts the fetch), doesn't stand at your table waiting (blocking), but goes to help other customers (runs other code), then comes back when your food is ready (promise resolves). The 'await' keyword is the waiter checking 'is the food ready yet?'"

**Simplified**: "Async/await lets JavaScript start a slow task, do other things while waiting, then continue where it left off when the task finishes. It's like setting a timer - you don't stare at it, you do other stuff until it beeps."

### Understanding database indexes:

**First attempt**: "An index is a data structure that improves query performance by creating a sorted reference to table data."

**Gap identified**: How does sorting help? What's the tradeoff? When would you NOT want an index?

**After filling gaps**: "A database without an index is like a book without a table of contents. To find information about 'databases' the computer reads every single page from start to finish. With an index, it's like having a sorted list at the back: 'databases - see page 47, 103, 299'. Jump directly to those pages.

The tradeoff: every time you add a page to the book, you must update the index. More writing work, faster reading. If you're constantly writing and rarely reading, maintaining the index might cost more than it saves."

**Simplified**: "An index is a sorted shortcut that trades write speed for read speed. Like a book's table of contents - takes effort to maintain, but makes finding things much faster."

### Understanding gradient descent:

**First attempt**: "Gradient descent is an optimization algorithm that iteratively adjusts parameters in the direction of steepest descent of the loss function."

**Gap identified**: What does "steepest descent" actually mean in practice? Why does this work? What could go wrong?

**After filling gaps**: "Imagine you're blindfolded on a mountain and want to reach the valley. You can feel the ground under your feet. Gradient descent is: feel which direction slopes down the most steeply, take a step that way, repeat.

The 'gradient' is the slope direction. 'Descent' means going downhill. Each step adjusts your position (the model parameters) to reduce your altitude (the error).

Problems: You might find a small dip (local minimum) but miss the actual valley. If steps are too big, you'll jump over the valley. Too small, you'll take forever. The ground might be bumpy (noisy data)."

**Simplified**: "Gradient descent finds the best answer by repeatedly asking 'which direction makes things better?' and stepping that way, like walking downhill by feeling which way slopes down."

## When to use this skill

- When learning a new technology or domain and you need to verify you actually understand rather than just recognize terms
- Before technical interviews or presentations to identify knowledge gaps while you can still fill them
- When documentation seems clear but you can't apply it, suggesting surface familiarity without real understanding
- When team members seem confused and you suspect the explanation relies on unstated expert context
- Before mentoring or teaching to ensure you can explain without falling back on jargon
- When you catch yourself saying "it just works" or "basically" instead of explaining the actual mechanism
- Before creating documentation to test whether you're communicating or just demonstrating expertise
- When you need genuine intuition for making decisions rather than memorized rules you can't adapt
