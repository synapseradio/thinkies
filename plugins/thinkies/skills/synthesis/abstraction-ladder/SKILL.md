---
name: abstraction-ladder
description: Move flexibly between specific details and general concepts to find the right level of thinking for each problem, useful when stuck at wrong altitude, connecting theory to practice, or finding patterns across examples
---

# Abstraction Ladder

Navigate between concrete specifics and abstract principles to think at the most useful level.

## Instructions

When using the abstraction ladder:

1. **Identify where you are**:
   - Very concrete: Specific implementation, exact data, particular instance
   - Somewhat concrete: This feature, this user, this bug
   - Middle: Type of feature, class of users, category of bug
   - Somewhat abstract: Patterns, principles, approaches
   - Very abstract: Fundamental truths, universal principles

2. **Notice if you're stuck**:
   - Too concrete: Lost in details, can't see patterns
   - Too abstract: No way to act, floating in generalities
   - Wrong level: Feels like you're missing something

3. **Climb up (abstract)**:
   - What is this an example of?
   - What pattern does this follow?
   - What's the general principle?
   - How would you explain this to someone outside the domain?
   - What's the essential nature of this?

4. **Climb down (concrete)**:
   - What does this look like in practice?
   - Can you give an example?
   - What would you actually do?
   - What specific case does this apply to?
   - How do you know it's working?

5. **Move sideways (same level)**:
   - What else is like this?
   - What's another example at this level?
   - How else could you implement this principle?

6. **Find the right level**:
   - Where can you see patterns but also act?
   - Where does understanding connect to doing?
   - Where is communication clearest?

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

- Stuck in details and can't see the big picture
- Have big ideas but can't make them concrete
- Need to explain something to different audiences
- Looking for alternative solutions
- Connecting theory to practice
- Debugging complex problems
- Making architectural decisions
- Learning new concepts
- Finding the right scope for a change
- Communicating across experience levels
