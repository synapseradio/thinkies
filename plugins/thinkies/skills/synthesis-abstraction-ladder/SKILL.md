---
name: abstraction-ladder
description: Move flexibly between specific details and general concepts to find the right level of thinking for each problem, useful when stuck at wrong altitude, connecting theory to practice, or finding patterns across examples
---

# Abstraction Ladder

Navigate between concrete specifics and abstract principles to think at the most useful level.

## Instructions

When using the abstraction ladder:

1. **Locate your current level** - Determine whether you're working with specific instances, particular cases, categories and types, general patterns, or fundamental principles.

2. **Recognize misalignment** - Notice when you're lost in details without seeing patterns, floating in generalities without actionable steps, or working at the wrong altitude for the problem at hand.

3. **Climb up** - Generalize by asking what this exemplifies, what pattern it follows, or what principle underlies it, moving from specifics toward broader understanding.

4. **Climb down** - Concretize by asking what this looks like in practice, what specific example demonstrates it, or what actual steps implement it, moving from principles toward actionable details.

5. **Move sideways** - Find alternatives at the same abstraction level by asking what else is like this, what other examples exist here, or how else this principle manifests.

6. **Find the working level** - Identify where understanding enables action, where patterns become visible without losing practical grounding, and where communication achieves clarity for your audience.

## Examples

### Working up from specifics:
"**Very concrete**: The login button doesn't respond when clicked on iPhone 12 running iOS 16.3 in Safari.

**Climb up**: Login button not responsive on some mobile devices.

**Climb up**: Touch event handling issue on mobile Safari.

**Climb up**: Inconsistent event handling across browsers.

**Climb up**: Interface adaptation across platforms.

**Climb up**: Systems must handle environmental variation.

**Finding the useful level**: 'Touch event handling issue on mobile Safari' is probably right level for fixing this specific bug. 'Interface adaptation across platforms' might be right level for preventing this class of bug. 'Systems must handle environmental variation' is too abstract to act on, but might inform architecture decisions.

**Key insight**: The fix happens at concrete level, but understanding why it happens helps at middle level. Going too high loses actionability; staying too low misses prevention opportunities."

### Working down from abstract:
"**Very abstract**: Software should be maintainable.

**Climb down**: Code should be easy for others to understand and modify.

**Climb down**: Functions should do one clear thing, with descriptive names.

**Climb down**: This function should be split because it handles both validation and formatting.

**Climb down**: Extract the email validation logic into a separate `isValidEmail()` function.

**Very concrete**: Move lines 45-67 into a new function in utils/validation.ts.

**Finding the useful level**: 'Functions should do one thing' is good principle. 'Split this function' is good code review feedback. 'Move lines 45-67' is good for actual implementation. Each level has its place.

**Key insight**: Principles guide decisions, but you need concrete specifics to actually change code. Move up for why, down for how."

### Navigating to solve a problem:
"**Starting point (concrete)**: User clicked 'Save' but got error 'Database connection timeout'.

**Stuck at this level**: Can't see beyond this one error.

**Climb up**: What kind of error is this? Database connectivity problem.

**Climb up**: What pattern? Service dependency failure.

**Too high - come back down**: How do we handle service failures?
- Retry logic
- Graceful degradation
- User feedback

**Right level found**: We need retry logic for transient failures.

**Climb down**: How to implement retry?
- Exponential backoff
- Max attempts
- User notification

**Climb down to concrete**: Add retry decorator to database call, 3 attempts, exponential backoff, show user 'Saving...' indicator.

**Ladder in action**:
1. Started concrete (one error)
2. Climbed up to see pattern (service failures)
3. Climbed down to solution approach (retry logic)
4. Climbed down to implementation (specific code changes)

**What the movement reveals**: The solution wasn't visible at the starting level. Going up revealed it was a common pattern. Going down made it actionable."

### Moving sideways to find alternatives:
"**Current level**: Caching API responses to improve performance.

**Asking 'what else is like this?'** (same abstraction level):
- Precomputing results
- Indexing data
- Batching requests
- Lazy loading

**All are at same level**: Performance optimization through reduced work.

**Value of sideways movement**: Reveals alternatives you might not see when locked in one approach. Maybe the right answer isn't caching - it's batching requests to reduce round trips.

**Climb up to choose**: What's the actual bottleneck?
- Too many requests? → Batch
- Slow computation? → Cache or precompute
- Large data transfer? → Lazy load

**Sideways movement at higher level reveals the choice framework.**"

### Recognizing the wrong level:
"**Team discussion**:
Person A: 'We need to refactor the authentication module.'
Person B: 'Which part specifically?'
Person A: 'The whole thing, it's not maintainable.'
Person B: 'What can't you maintain?'
Person A: 'It's just bad architecture.'

**Problem**: Person A is stuck too high. 'Bad architecture' and 'not maintainable' are too abstract to act on.

**Climbing down**:
- What specific change is hard to make?
- 'Adding a new OAuth provider takes 200 lines of boilerplate.'

**Now actionable**: That's concrete enough to address.

**Going back up one level**: 'Too much boilerplate for adding auth providers' points to solution space: provider abstraction, configuration-driven approach.

**Right level found**: Somewhere between 'bad architecture' (too high) and 'this specific function' (too low). Level of 'provider integration pattern' lets you see the problem and the solution space."

### Using the ladder for communication:
"**Explaining to different audiences**:

**To user**: 'The save button will now show you progress and retry automatically if there's a network hiccup.'
*Concrete, specific to their experience*

**To junior developer**: 'We're adding retry logic with exponential backoff to handle transient network failures.'
*Concrete implementation with some pattern language*

**To senior developer**: 'Implementing resilience patterns for external service dependencies.'
*Pattern level, they'll know what that means*

**To architect**: 'Moving toward fault-tolerant service integration.'
*High level architectural principle*

**Same change, different altitudes**. Each audience needs different level to understand and act on the information."

## When to use this skill

- When stuck in implementation details without seeing the broader pattern
- When working with abstract principles that lack concrete application paths
- Before explaining concepts to audiences with different expertise levels
- While searching for alternative solutions by exploring at different abstraction levels
- When debugging requires understanding both specific symptoms and systemic patterns
- During architectural decisions that need to balance vision with practical constraints
- When learning new concepts by connecting theory to concrete examples
- To find the appropriate scope for changes by working at the right level of generality
