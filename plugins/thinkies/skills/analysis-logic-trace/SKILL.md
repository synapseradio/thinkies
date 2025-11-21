---
name: logic-trace
description: Trace reasoning steps to identify gaps, leaps, or errors in logical chains, useful for validating complex arguments, mathematical proofs, debugging reasoning, or ensuring rigorous thinking
---

# Logic Trace

Follow reasoning step-by-step to ensure each link in the logical chain is sound.

## Instructions

When tracing logic:

1. **Break reasoning into atomic steps** - Decompose the argument into its smallest logical moves where each step represents a single inference, making implicit steps explicit and numbering them for reference.

2. **Examine each link for validity and hidden assumptions** - For each step, identify what's being claimed, what evidence or prior conclusions it's based on, whether the inference is valid, and what unstated assumptions make the inference work.

3. **Check the inference type being used** - Determine whether the step uses deduction (conclusion necessarily follows from premises), induction (generalizing from specific examples), abduction (inferring best explanation from observations), or analogy (applying patterns from comparable situations), and verify that the inference type is appropriate and correctly applied.

4. **Identify gaps, leaps, and circular dependencies** - Look for missing steps between premises and conclusions, unjustified jumps in reasoning, connections that are assumed but need proof, and cases where conclusions are used to support their own premises.

5. **Verify logical connectors and trace dependencies** - Check that AND, OR, IF-THEN, and NOT operators are used correctly, then map which conclusions depend on which premises to understand how failures propagate and whether alternative reasoning paths exist.

6. **Assess overall chain strength** - Determine whether the conclusion follows validly from the premises, where the reasoning is strongest and weakest, and what would be required to strengthen weak links.

## Examples

### Infrastructure investment

"**Claim**: Building a new highway will reduce traffic congestion

**Logic trace**:
1. Current roads are congested [Observed]
2. Insufficient capacity causes congestion [Traffic principle]
3. New highway adds capacity [By design]
4. Added capacity reduces congestion [From 2,3]
5. Therefore new highway solves congestion [From 4]

**Gaps identified**:
- Step 4: LEAP - ignores induced demand (more capacity attracts more traffic)
- Missing: Do travel patterns shift when new routes become available?
- Missing: What happens to surface streets when highway draws traffic?
- Missing: Does increased capacity enable sprawl that generates more trips?
- Step 2→4: Assumes demand is fixed, but it responds to supply

**Logical flaw**: Linear reasoning treats capacity and demand as independent when they're coupled. Adding capacity changes demand patterns, potentially recreating congestion at higher traffic volumes."

### Hiring decision

"**Reasoning**: Candidate attended prestigious university, therefore they'll be a strong performer

**Logic trace**:
1. Candidate has degree from top-ranked school [Verified]
2. Top schools have rigorous selection and training [Generally true]
3. Graduates from these schools perform well [Statistical pattern]
4. Therefore this candidate will perform well [From 1,2,3]

**Examining links**:
- Step 2: Valid but doesn't specify what skills are trained
- Step 3: True on average but high variance within group
- Step 3→4: LEAP - group statistics don't predict individual outcomes

**Missing pieces**:
- No evaluation of candidate's actual skills for this role
- Haven't assessed alignment with team culture
- Don't know if prestige correlates with performance in our specific context
- Ignoring that school selection is partly based on pre-existing advantages
- Haven't considered that recent graduates need different support than experienced hires

**Logical flaw**: Reasoning from group membership to individual capability without direct assessment. The credential is a weak proxy for job-specific competence."

### Resource allocation

"**Reasoning**: We should fund the project with highest ROI estimate

**Logic trace**:
1. Project A shows 300% ROI, Project B shows 150% ROI [From projections]
2. Higher ROI means better investment [Financial principle]
3. Project A has higher ROI than Project B [From 1]
4. Therefore fund Project A [From 2,3]

**Gaps found**:
- Step 1: Assumes ROI estimates are equally reliable (ignores uncertainty)
- Step 2: LEAP - ROI is one factor, not the only consideration
- Missing: What are the confidence intervals on these estimates?
- Missing: How certain are the assumptions underlying each projection?
- Missing: Do projects have different risk profiles?
- Missing: Are there strategic considerations beyond ROI?
- Missing: What's the opportunity cost if Project A fails versus Project B?

**Logical flaw**: Treats point estimates as facts and optimizes on single metric without accounting for uncertainty, risk, or strategic fit. A 150% ROI with high confidence may be superior to 300% ROI with high uncertainty."

## When to use this skill

- When you notice yourself making a logical leap in your reasoning that you can't fully justify
- Before presenting a multi-step argument to verify each inference actually follows from the previous one
- When you find yourself saying "therefore" or "thus" without being certain the conclusion necessarily follows
- Before recommending a decision based on a chain of reasoning, to identify where the logic might be weakest
- When you notice hidden assumptions in your own thinking that you're treating as if they were established facts
- To verify that what feels like sound reasoning isn't actually circular or dependent on unproven premises
- When debugging complex issues where the relationship between cause and effect involves multiple steps
- Before claiming something is proven or certain, to ensure the logical chain from evidence to conclusion is valid