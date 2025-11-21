---
name: connect-dots
description: Find patterns and relationships across disparate ideas to reveal hidden connections, useful when working with information from multiple domains or trying to see how separate concepts relate
---

# Connect Dots

Discover meaningful relationships between seemingly unrelated ideas, concepts, or observations.

## Instructions

When connecting dots:

1. **Assemble observations** - Gather separate ideas, facts, or observations without forcing connections, noting their origins and keeping them simultaneously visible.

2. **Identify shared qualities** - Look for similar structures, common constraints, parallel problems, analogous mechanisms, or matching patterns across seemingly disparate pieces.

3. **Trace relationships** - Explore how pieces might relate mechanically, whether through cause and effect, mutual influence, shared dependencies, or coordinated behavior.

4. **Test connection validity** - Verify that similarities run deeper than surface resemblance by checking whether understanding one genuinely illuminates the other, whether the connection makes testable predictions, and what evidence would falsify it.

5. **Map the network** - Identify how multiple connections relate to each other, revealing hubs where many things converge, isolated clusters, and larger emergent patterns.

6. **Extract meaning** - Determine what underlying principle or mechanism explains why these connections exist and what previously hidden insight this network reveals.

## Examples

### Connecting technical observations:
"I noticed three separate things this week:
- Database queries slow down during batch processing
- UI feels sluggish when background sync runs
- Error rates spike during automated reports

**Surface connection**: They're all performance issues.

**Deeper connection**: They all happen when background jobs run. The background workers aren't actually 'background' - they're competing for the same resources as user-facing features.

**Revealed insight**: We need resource isolation, not just task scheduling. The problem isn't when things run, but how they share resources."

### Connecting across domains:
"**Observation from gardening**: Plants grow better when stressed slightly - too much water or perfect conditions make them weak.

**Observation from learning**: Students who struggle a bit retain information better than those for whom everything comes easily.

**Observation from code**: Systems that gracefully handle small failures tend to be more robust than those optimized for perfect conditions.

**Connection**: Optimal growth happens at the edge of capability, not in comfort. Whether organisms, minds, or systems, resilience comes from regular exposure to manageable challenges.

**Application**: Our error handling shouldn't just prevent failures - it should help the system learn from them."

### Connecting user feedback:
"Different users said:
- 'I wish I could see my history'
- 'I keep making the same mistakes'
- 'I forget what I did last time'
- 'There's no way to learn from experience'

**Connection**: They're all talking about memory and learning. Users want the system to help them remember and improve, not just execute tasks.

**Insight**: We framed this as a 'history feature' but it's really about learning support. That changes what we build - not just a log, but a reflection tool."

### Connecting patterns in data:
"Noticing:
- Feature requests cluster around automation
- Support tickets cluster around repetitive tasks
- User session data shows repeated action sequences
- Power users have extensive keyboard shortcuts

**Connection web**:
- Automation requests + repetitive support tickets = pain points
- Repeated sequences + keyboard shortcuts = efficiency seeking
- All four = users want to teach the system their patterns

**Synthesis**: Users are trying to encode their expertise into the tool. We should build pattern recognition and suggestion, not just more automation options."

## When to use this skill

- When multiple observations seem related but the connection isn't obvious
- While building system models that show how components interact and influence each other
- To trace causal chains and understand how separate phenomena affect one another
- When working with information from different domains or sources that might interconnect
- To map networks of relationships and identify central hubs or isolated clusters
- While explaining why multiple things consistently happen together
- When seeking new solutions by recognizing analogous mechanisms from different contexts
- To understand what underlying principle links apparently disparate observations

## Related Skills

**theme-find** - For identifying recurring conceptual patterns rather than mechanical relationships. Use theme-find when you need to name what keeps coming up, categorize observations into themes, or identify unifying concepts. connect-dots focuses on discovering how things causally relate and influence each other, while theme-find focuses on recognizing what conceptually unifies diverse observations.
