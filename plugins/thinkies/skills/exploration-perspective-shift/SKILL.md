---
name: perspective-shift
description: View situations from multiple vantage points to gain comprehensive understanding, useful for breaking out of fixed viewpoints, understanding stakeholder needs, or seeing problems differently
---

# Perspective Shift

Systematically view situations from different angles and stakeholder viewpoints.

## Instructions

When shifting perspectives:

1. **Identify the current lens** - Recognize what perspective you're naturally taking, whether it's technical versus user-focused, expert versus beginner, builder versus maintainer, or system-level versus individual-component thinking.

2. **Choose contrasting viewpoints** - Select perspectives that fundamentally differ from your current stance, considering viewpoints like the user experiencing it, the builder creating it, the maintainer supporting it long-term, the business evaluating value and cost, the beginner encountering it fresh, the expert assessing sophistication, or the outsider seeing hidden assumptions.

3. **Inhabit each perspective fully** - Use "I" statements from that viewpoint to make it real, consider what goals and constraints that perspective operates under, identify what causes pain from that angle, and understand what success looks like through those eyes.

4. **Note perspective conflicts** - Identify where viewpoints genuinely clash, recognize what's optimal for one perspective but problematic for another, and distinguish which tensions are fundamental trade-offs versus solvable through better design.

5. **Find synthesis opportunities** - Consider whether multiple perspectives can be satisfied simultaneously, determine what each viewpoint would need to compromise for a workable solution, and look for approaches that honor the core needs of different perspectives even if they can't all get exactly what they want.

## Examples

### Viewing a feature request:
"**As the user**: I just want this to work without thinking about it. Why do I need to configure so many things?

**As the developer**: Each configuration option handles a different edge case we've encountered. Removing them would break existing workflows.

**As the support team**: Every option is another thing users get wrong and then need help with. We're drowning in config-related tickets.

**As the product owner**: We're trying to serve too many use cases. Maybe we need different products for different user types instead of one configurable monster.

**Synthesis**: What if we had smart defaults that work for 90% of cases, with an 'advanced' mode for the edge cases?"

### Debugging a performance issue:
"**From the code's perspective**: I'm doing exactly what I was told - checking every item against every rule.

**From the CPU's perspective**: I'm constantly context-switching and cache-missing because the data access pattern is random.

**From the user's perspective**: I clicked the button and nothing happened for 5 seconds.

**From the database's perspective**: I'm getting hammered with thousands of identical queries.

**Insight**: The performance issue isn't in any one place - it's in the interaction between layers."

## When to use this skill

- When you realize you're stuck viewing a problem from only one angle and need to deliberately shift stance
- Before making design decisions that affect multiple stakeholders, to understand what each perspective values
- If you're trying to resolve disagreements by understanding why different parties see the situation differently
- When designing user experiences and need to shift between technical implementation and user perception
- To break analysis paralysis by viewing the decision through different lenses that prioritize different factors
- Before dismissing an objection or concern, to fully inhabit that perspective and understand its validity
- When searching for win-win solutions by understanding what each viewpoint truly needs versus what they're requesting
- If you catch yourself thinking "they just don't understand" about stakeholders, signaling you need to inhabit their perspective more fully

## Related Skills

**six-hats** - For structured thinking using six predefined modes. Use six-hats when you want systematic examination of facts, emotions, risks, benefits, creativity, and process - particularly valuable for group decision-making with shared vocabulary. perspective-shift offers more flexible viewpoint exploration where you choose which perspectives to inhabit based on the specific situation and stakeholders involved.