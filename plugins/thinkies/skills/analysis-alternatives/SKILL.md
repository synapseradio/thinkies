---
name: alternatives
description: Generate plausible alternative explanations for the same evidence or observations, useful for avoiding confirmation bias, thorough analysis, and scientific thinking about problems
---

# Alternatives

Create multiple plausible explanations for the same observations or evidence.

## Instructions

When generating alternatives:

1. **State the current explanation and what needs explaining** - Articulate the existing theory clearly, noting what evidence supports it, then identify the key observations, patterns, and surprising elements that any explanation must account for.

2. **Generate diverse alternatives through multiple lenses** - Create different explanations by varying the mechanism (same outcome, different cause), scope (more specific or general), timing (earlier or later cause), considering multiple causes working together, reverse causation where the effect might be the cause, pure coincidence where the pattern isn't real, or selection bias where you're seeing what you expect.

3. **Make each alternative concrete and testable** - For each explanation, describe how it would actually work, what additional observations you'd expect to see, what assumptions it requires, and what evidence would distinguish it from other alternatives.

4. **Identify distinguishing tests** - Determine what would rule out each explanation, what evidence favors which alternatives, and which explanations are testable and how you would test them.

## Examples

### Manufacturing quality issue

"**Observation**: Widget defect rate increased from 2% to 8% over three months

**Current explanation**: New supplier materials are lower quality

**Alternative explanations**:
1. **Calibration drift**: Testing equipment now flags good parts as defective
   - Would see defects cluster at borderline measurements
   - Testing known-good parts would reveal

2. **Seasonal humidity**: Temperature and moisture affecting production line
   - Would correlate with weather patterns
   - Environmental monitoring would confirm

3. **Training gap**: Recent staff turnover means less experienced operators
   - Would see defects concentrated on specific shifts or stations
   - Operator experience data would distinguish

4. **Multiple causes**: Material variation plus temperature plus operator experience compounding
   - Would see markers for several factors
   - Addressing single cause wouldn't fully resolve

5. **Definition change**: Quality standards tightened, catching previously acceptable variation
   - Would see inspection criteria modified in documentation
   - Historical parts re-tested would now fail

**Key insight**: Changing suppliers based on the first explanation could be expensive and wrong if the real cause is calibration or environmental."

### Student engagement decline

"**Observation**: Class participation dropped significantly after switching to discussion-based format

**Current explanation**: Students prefer lectures

**Alternative explanations**:
1. **Preparation gap**: Discussion requires advance reading students aren't doing
   - Would see participation correlate with reading completion
   - Pre-discussion quizzes would test

2. **Social anxiety**: Format exposes students who fear speaking publicly
   - Would see same students contributing online but not in person
   - Anonymous participation tools would distinguish

3. **Group size**: Discussion works poorly with 40 students versus 15
   - Would see few voices dominating, many silent
   - Small group breakouts would reveal engagement

4. **Assessment mismatch**: Students unsure how discussion affects their grade
   - Would see participation increase after grading rubric clarified
   - Direct questions about grading would surface confusion

5. **Topic difficulty**: Current material is too complex for productive discussion
   - Would see engagement vary by topic
   - Simpler discussion topics would test

**Key insight**: Each explanation suggests a different fix—clearer expectations, smaller groups, scaffolding, or hybrid formats."

### Network performance degradation

"**Observation**: Application response times increased from 200ms to 2000ms over two weeks

**Current explanation**: Recent code deployment introduced inefficiency

**Alternative explanations**:
1. **Data growth**: Database size crossed threshold where queries became slow
   - Would see query time correlate with data volume
   - Database metrics would show size changes

2. **External dependency**: Third-party API slowed down, blocking our requests
   - Would see timeouts concentrated on external calls
   - Monitoring external service latency would confirm

3. **Load increase**: User traffic grew and system hit capacity limits
   - Would see performance degrade during peak hours only
   - Load testing would reproduce

4. **Resource contention**: Another system now sharing infrastructure
   - Would see resource utilization increased across the board
   - Infrastructure monitoring would identify competing processes

5. **Cache invalidation**: Recent change broke caching, hitting database repeatedly
   - Would see cache hit rate drop
   - Cache metrics would show the pattern

**Key insight**: Rolling back the deployment won't help if the cause is data growth, traffic, or external dependencies."

## When to use this skill

- When you find yourself confidently presenting a single explanation without having considered alternatives
- Before stating "this happened because..." to verify you've tested the explanation against alternatives
- When noticing you've jumped to the first plausible explanation that came to mind
- Before recommending action based on assumed causation, ensuring alternatives wouldn't suggest different interventions
- When investigating problems where the obvious explanation feels too convenient or aligns suspiciously well with existing beliefs
- To avoid confirmation bias when analyzing incidents, failures, or unexpected outcomes
- When research findings or diagnostic evidence could support multiple interpretations
- Before committing resources to solutions based on untested causal assumptions
