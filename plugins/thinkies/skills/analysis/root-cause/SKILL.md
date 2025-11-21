---
name: root-cause
description: Drill down through layers of causation to find fundamental causes using the Five Whys technique, useful for problem diagnosis, understanding failures, and preventing recurrence
---

# Root Cause

Systematically drill down through causation layers to find the fundamental source of problems.

## Instructions

When finding root causes:

1. **Start with the problem**: State what went wrong clearly and specifically
   - Avoid vague descriptions
   - Include impact and context
   - "X happened, causing Y"

2. **Ask "Why?" iteratively**:
   - Why did this happen? [Answer]
   - Why did [answer] happen? [Deeper answer]
   - Continue until you reach a root cause
   - Usually takes 3-7 iterations, not always 5

3. **Stay factual at each level**:
   - Base answers on evidence, not speculation
   - If unsure, note it and investigate
   - Avoid jumping to conclusions

4. **Watch for multiple causes**:
   - Problems often have multiple roots
   - Branch your investigation when needed
   - Some branches might be more important

5. **Recognize root causes**:
   - Can't ask "why" meaningfully anymore
   - Reached a process/system/decision level
   - Found something you can actually fix
   - Hit organizational or physics limits

6. **Distinguish symptoms from causes**:
   - Symptoms: What you observe
   - Proximate causes: Immediate triggers
   - Root causes: Fundamental issues

7. **Validate the chain**:
   - Work backwards: Would fixing root prevent problem?
   - Are all links necessary?
   - Test when possible

## Examples

### Root cause analysis of a production outage:
"**Problem**: Website went down for 2 hours

**Why #1**: Database server ran out of connections
→ **Why?**: Connection pool was exhausted

**Why #2**: Apps weren't releasing connections
→ **Why?**: Missing connection timeout configuration

**Why #3**: Timeouts were removed during last update
→ **Why?**: Developer copied config from test environment

**Why #4**: Test environment doesn't need timeouts
→ **Why?**: Test has unlimited connections for debugging

**Why #5**: No config validation between environments
→ **Root cause**: Lack of environment-specific config validation

**Solution**: Add automated config validation in deployment pipeline"

### Root cause of a team problem:
"**Problem**: Features consistently delivered late

**Why #1**: Development takes longer than estimated
→ **Why?**: Unexpected complexity discovered during coding

**Why #2**: Complexity not known during estimation
→ **Why?**: Estimates done without technical investigation

**Why #3**: No time allocated for investigation
→ **Why?**: Pressure to commit to timelines quickly

**Why #4**: Business needs definite dates for planning
→ **Why?**: No process for handling uncertainty

**Root cause**: Organization lacks framework for communicating and managing technical uncertainty

**But also** (parallel branch):
**Why #2b**: Frequent context switching
→ **Why?**: Developers pulled into support issues
→ **Why?**: No dedicated support rotation
→ **Second root**: Lack of operational/development separation"

### Root cause of performance degradation:
"**Problem**: API response times doubled over 6 months

**Why #1**: Database queries taking longer
→ **Why?**: Table sizes grew significantly

**Why #2**: More data than expected
→ **Why?**: Not archiving old records

**Why #3**: Archival process was disabled
→ **Why?**: Caused errors with reporting

**Why #4**: Reports expect all historical data present
→ **Why?**: Reports designed with assumption of small data

**Why #5**: Original design didn't anticipate scale
→ **Root cause**: Lack of data growth planning in architecture

**Validation**: If we had planned for data growth, we would have designed reports to work with archived data"

## When to use this skill

- Post-incident analysis
- Debugging persistent problems
- Process improvement
- Quality issues
- Performance degradation
- Team dysfunction
- Customer complaint analysis
- Preventing problem recurrence