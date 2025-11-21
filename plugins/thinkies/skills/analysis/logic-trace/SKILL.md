---
name: logic-trace
description: Trace reasoning steps to identify gaps, leaps, or errors in logical chains, useful for validating complex arguments, mathematical proofs, debugging reasoning, or ensuring rigorous thinking
---

# Logic Trace

Follow reasoning step-by-step to ensure each link in the logical chain is sound.

## Instructions

When tracing logic:

1. **Break into atomic steps**: Decompose reasoning into smallest logical moves
   - Each step should be a single inference
   - Make implicit steps explicit
   - Number steps for reference

2. **Examine each link**:
   - What's claimed in this step?
   - What's it based on?
   - Is the inference valid?
   - Are there hidden assumptions?

3. **Check inference types**:
   - **Deduction**: Does conclusion necessarily follow?
   - **Induction**: Is generalization justified by examples?
   - **Abduction**: Is this the best explanation?
   - **Analogy**: Are situations truly comparable?

4. **Identify gaps and leaps**:
   - Missing steps between premises and conclusion
   - Unjustified jumps in reasoning
   - Assumed connections that need proof
   - Circular dependencies

5. **Verify logical connectors**:
   - AND: All conditions really required?
   - OR: Are these truly alternatives?
   - IF-THEN: Does consequence always follow?
   - NOT: Is negation properly applied?

6. **Trace dependencies**:
   - Which conclusions depend on which premises?
   - If a premise fails, what else fails?
   - Are there alternative paths to the same conclusion?

## Examples

### Tracing technical reasoning:
"**Claim**: Our database can't handle the load, so we need to shard

**Logic trace**:
1. Database has performance problems [Observed]
2. Performance problems mean can't handle load [Assumes problems = capacity]
3. Can't handle current load [From 1,2]
4. Sharding increases capacity [Generally true]
5. Therefore need sharding [From 3,4]

**Gaps identified**:
- Step 2: Performance might not be capacity (could be query optimization)
- Step 3→5: Jumps to sharding without considering alternatives
- Missing: Have we identified what kind of load?
- Missing: Would sharding actually help our specific problem?

**Logical flaw**: Assumes single cause and single solution without elimination of alternatives."

### Tracing a debugging hypothesis:
"**Hypothesis**: Race condition causes intermittent test failures

**Logic trace**:
1. Test fails intermittently [Observed]
2. Same input produces different outputs [From 1]
3. Non-determinism requires varying state [Logic principle]
4. Varying state suggests timing issues [From 3]
5. Timing issues in concurrent code = race condition [Definition]
6. Therefore race condition causes failures [From 2,4,5]

**Examining links**:
- Step 2: Valid - intermittent = different outputs
- Step 3: Valid - deterministic systems don't vary
- Step 4: LEAP - could be random numbers, external state, etc.
- Step 5: Assumes we have concurrent code (need to verify)

**Missing pieces**:
- No evidence of concurrent execution
- Haven't ruled out test pollution
- Haven't checked for time-dependent code"

### Tracing a design decision:
"**Reasoning**: Microservices will improve deployment speed

**Logic trace**:
1. Current deployment is slow [Premise]
2. Slow because entire app deploys together [Assumption]
3. Microservices deploy independently [True by definition]
4. Independent deployment is faster [Assumes no dependencies]
5. Therefore microservices improve deployment speed [From 3,4]

**Gaps found**:
- Step 2: Is coupling the actual cause of slowness?
- Step 4: Ignores coordination overhead
- Missing: Cost of maintaining service boundaries
- Missing: Deployment vs development speed trade-off"

## When to use this skill

- Validating complex arguments
- Debugging mysterious issues
- Reviewing mathematical proofs
- Analyzing decision rationale
- Code review reasoning
- Checking your own thinking
- Understanding disagreements
- Building bulletproof cases