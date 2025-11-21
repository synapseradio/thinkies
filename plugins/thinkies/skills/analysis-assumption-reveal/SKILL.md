---
name: assumption-reveal
description: Uncover hidden assumptions and unstated premises in arguments, plans, or beliefs using systematic questioning, useful for deep analysis, challenging ideas, or understanding root beliefs
---

# Assumption Reveal

Surface hidden assumptions that underlie reasoning, decisions, or beliefs.

## Instructions

When revealing assumptions:

1. **Start with the surface claim**: What's being stated or proposed?
   - Write it out explicitly
   - Note what seems obvious or "goes without saying"

2. **Work backwards with "This assumes..."**:
   - What must be true for this to work?
   - What conditions are being taken for granted?
   - What's being treated as fixed that might be variable?

3. **Use assumption-revealing questions**:
   - "What if the opposite were true?"
   - "When wouldn't this apply?"
   - "What needs to exist for this to make sense?"
   - "What are we not considering?"
   - "Why do we believe this prerequisite exists?"

4. **Categorize assumptions**:
   - **Factual**: About how things are
   - **Causal**: About what leads to what
   - **Value**: About what's important or good
   - **Definitional**: About what terms mean
   - **Contextual**: About the environment/situation

5. **Test assumption validity**:
   - Which assumptions are solid?
   - Which are questionable?
   - Which are probably wrong?
   - What happens if key assumptions fail?

6. **Explore implications**:
   - How does the conclusion change if assumptions change?
   - Which assumptions are load-bearing?

## Examples

### Revealing assumptions in a technical plan:
"**Plan**: We'll migrate to microservices over 6 months

**Hidden assumptions I'm finding**:
- Team has capacity for migration work (factual)
- Current monolith boundaries map to service boundaries (structural)
- Network reliability won't impact user experience (environmental)
- Team can learn distributed systems while delivering (capability)
- Microservices will solve our actual problems (causal)
- 6 months is enough time (temporal)
- Benefits outweigh operational complexity (value)

**Testing validity**:
- Team capacity: Questionable - we're already at capacity
- Service boundaries: Untested - never mapped this
- Network reliability: False - we have latency issues now
- Distributed systems skill: Weak - team lacks experience

**Load-bearing assumption**: That microservices solve our specific problems. If this is wrong, everything else is moot."

### Revealing assumptions in a feature request:
"**Request**: Add real-time collaboration to our document editor

**Assumptions being made**:
- Users want to edit simultaneously (user need)
- Users have stable internet connections (infrastructure)
- Conflict resolution is solvable for our document type (technical)
- Real-time adds more value than complexity (cost-benefit)
- Our current architecture can support this (compatibility)
- We can maintain data consistency (feasibility)

**Questioning these**:
- Do users actually edit the same section simultaneously?
- What if they prefer async collaboration with clear ownership?
- Our documents have complex validation rules - can these work real-time?

**Key insight**: We're assuming synchronous = better, but our users might prefer clarity over immediacy."

## When to use this skill

- Analyzing strategic plans
- Debugging mysterious failures
- Understanding disagreements
- Challenging conventional wisdom
- Risk assessment
- Requirements analysis
- Cultural or process critiques
- Before major decisions