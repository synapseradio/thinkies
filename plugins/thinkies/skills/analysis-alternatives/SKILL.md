---
name: alternatives
description: Generate plausible alternative explanations for the same evidence or observations, useful for avoiding confirmation bias, thorough analysis, and scientific thinking about problems
---

# Alternatives

Create multiple plausible explanations for the same observations or evidence.

## Instructions

When generating alternatives:

1. **Start with the current explanation**: What's the existing theory about why something happens?
   - State it clearly
   - Note what evidence supports it

2. **Identify what needs explaining**:
   - What are the key observations?
   - What patterns need accounting for?
   - What's surprising or unexpected?

3. **Generate diverse alternatives**:
   - **Different mechanism**: Same outcome, different cause
   - **Different scope**: More specific or more general cause
   - **Different timing**: Earlier/later cause than assumed
   - **Multiple causes**: Not one thing but several
   - **Reverse causation**: Effect might be cause
   - **Coincidence**: Maybe unrelated
   - **Selection bias**: Seeing pattern that isn't there

4. **Make each alternative concrete**:
   - How would this explanation work?
   - What would be its mechanism?
   - What else would we expect to see?

5. **Evaluate plausibility**:
   - Which explanations fit all evidence?
   - Which require fewer assumptions?
   - Which are testable?

6. **Identify discriminating tests**:
   - What would distinguish between alternatives?
   - What evidence would rule out each explanation?

## Examples

### Alternative explanations for a performance problem:
"**Observation**: System slows down every day at 2 PM

**Current explanation**: Lunch-return traffic spike

**Alternative explanations**:
1. **Scheduled job**: A batch process runs at 2 PM
   - Would see CPU/memory spike
   - Check cron schedules

2. **Geographic pattern**: European end-of-day + US mid-day overlap
   - Would see geographic distribution
   - Check user locations

3. **Cache expiry**: Morning cache expires after 4-5 hours
   - Would see cache miss rate increase
   - Check cache TTLs

4. **Cumulative leak**: Memory/connections leak throughout day, critical by 2 PM
   - Would see gradual degradation
   - Check resource usage trends

5. **External dependency**: Third-party service has issues at 2 PM
   - Would see external call latency
   - Check dependency metrics

**Discriminating test**: Monitor all metrics at 2 PM on weekend - if it's user traffic, weekend should be different."

### Alternative explanations for user behavior:
"**Observation**: Users abandon cart at payment page

**Current explanation**: Payment form is confusing

**Alternative explanations**:
1. **Sticker shock**: Total with shipping/tax surprises them
   - Would see abandonment correlate with total amount
   - Test showing full price earlier

2. **Trust issues**: Don't trust our payment security
   - Would see higher abandonment for new vs returning users
   - Add trust badges and test

3. **Comparison shopping**: Using cart to check final price
   - Would see same users return later
   - Check user journey patterns

4. **Payment method**: Their preferred method isn't available
   - Would vary by geographic region
   - Survey abandoned carts

5. **Technical issues**: Page fails silently for some users
   - Would see JavaScript errors
   - Check error logs

6. **Time to think**: Need approval from someone else
   - Would see eventual completion
   - Check cart recovery rates

**Key insight**: Different explanations suggest completely different solutions."

## When to use this skill

- Investigating mysterious bugs
- Understanding user behavior
- Avoiding confirmation bias
- Scientific problem-solving
- Incident analysis
- Market research interpretation
- A/B test analysis
- Medical or technical diagnosis