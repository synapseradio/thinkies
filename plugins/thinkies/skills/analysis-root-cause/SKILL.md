---
name: root-cause
description: Drill down through layers of causation to find fundamental causes using the Five Whys technique, useful for problem diagnosis, understanding failures, and preventing recurrence
---

# Root Cause

Systematically drill down through causation layers to find the fundamental source of problems.

## Instructions

When finding root causes:

1. **State the problem** - Describe what went wrong with specific impact and context, avoiding vague descriptions that obscure the actual failure.

2. **Ask why iteratively** - Begin with the immediate cause and ask why it occurred, then ask why that cause occurred, continuing through typically three to seven layers until reaching a fundamental issue that cannot be meaningfully questioned further.

3. **Ground each answer in evidence** - Base causal explanations on observable facts rather than speculation, noting uncertainty where it exists and investigating gaps before proceeding deeper.

4. **Branch when multiple causes emerge** - Recognize that problems often stem from several contributing factors and pursue parallel investigation paths, though some branches will prove more significant than others.

5. **Recognize when you reach bedrock** - Identify root causes by their position at the process, system, or decision level where further questioning becomes unproductive, where you've found something actionable, or where you've hit organizational or physical constraints.

6. **Validate the causal chain** - Work backward from proposed root to original problem, testing whether addressing the root cause would prevent recurrence and confirming that each link in the chain is necessary.

## Examples

### Medical clinic scheduling

"**Problem**: Patient wait times average 45 minutes beyond appointment time

**Why?**: Doctors run behind schedule throughout the day
→ **Why?**: Appointments take longer than the 15-minute slots allocated
→ **Why?**: Patients often have multiple concerns to address
→ **Why?**: No mechanism for patients to indicate appointment complexity when booking
→ **Why?**: Scheduling system assumes all appointments are equivalent

**Root cause**: Appointment scheduling lacks complexity differentiation

**Validation**: If the system could distinguish simple from complex visits and allocate time accordingly, doctors would stay on schedule and patient wait times would decrease."

### Bakery waste

"**Problem**: Bakery discards 30% of daily production

**Why?**: Too much inventory remains unsold
→ **Why?**: Production volumes don't match actual demand
→ **Why?**: Baking decisions made at 4 AM without current data
→ **Why?**: No system for tracking daily demand patterns

**But also** (parallel branch):
→ **Why?**: Customer arrivals highly variable
→ **Why?**: No incentive for customers to pre-order
→ **Why?**: Pre-ordering process doesn't exist

**Root causes**: Lack of demand forecasting and absence of pre-order system

**Validation**: Implementing demand tracking and pre-orders would allow production to align with actual need, reducing waste significantly."

### Community garden conflicts

"**Problem**: Gardeners frequently argue about water usage

**Why?**: Some plots use significantly more water than others
→ **Why?**: No usage limits or monitoring in place
→ **Why?**: Garden started small where informal norms worked
→ **Why?**: Water seemed abundant initially
→ **Why?**: Well capacity appeared unlimited until drought revealed constraints

**Root cause**: Resource governance didn't evolve as the garden scaled

**Validation**: If usage rules had been established as the garden grew, conflicts would have been prevented when scarcity emerged."

## When to use this skill

- When you notice yourself explaining what happened without explaining why it happened
- Before recommending solutions to verify you're addressing fundamental causes rather than symptoms
- When problems recur despite attempted fixes, suggesting earlier analysis missed the actual root
- To distinguish between immediate triggers and underlying systemic issues driving failures
- When you need to move from incident response to prevention
- Before presenting analysis to verify the causal chain holds under scrutiny

## Related Skills

**decompose** - For breaking down complexity into structural components. Use decompose when you need to understand how a system is organized, identify all the parts, or plan work distribution. root-cause drills down through layers of causation to find fundamental "why" answers, while decompose breaks things into structural pieces to understand composition and organization.