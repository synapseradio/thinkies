---
name: integrate
description: Weave diverse threads into coherent wholes that preserve nuance while creating unity, useful when combining multiple perspectives, reconciling tensions, or building comprehensive understanding from parts
---

# Integrate

Combine multiple ideas, perspectives, or insights into a coherent whole that's greater than the sum of parts.

## Instructions

When integrating:

1. **Lay out what you're combining** - List the pieces clearly, note their origins and individual value, and resist simplifying them yet.

2. **Find points of contact** - Identify where ideas naturally touch, where they support each other or fill gaps, and what one explains about another.

3. **Address tensions** - Determine where conflicts exist, whether they're real or apparent, whether both can be true in different contexts, and what the tension itself reveals.

4. **Build the synthesis** - Describe the larger picture they create together, how each piece fits, what emerges that wasn't in any single piece, and the organizing principle.

5. **Test coherence** - Check whether this holds together, preserves what matters from each piece, creates new understanding, and can be explained simply.

6. **Check what's missing** - Identify remaining gaps, what doesn't fit, and what new questions arise.

## Examples

### System design tensions
"**Performance engineer**: We need caching everywhere, database queries are slow.

**Security engineer**: Caching sensitive data creates risk, we need fresh data.

**User researcher**: Users expect consistency more than speed.

**Tension**: Speed vs security vs consistency.

**Integration attempt 1**: Cache some things but not others.
*Too simple - doesn't resolve the underlying tensions.*

**Deeper look**:
- Performance problem is real (slow queries)
- Security concern is real (cached sensitive data)
- Consistency issue is real (stale data confusion)
- All three aim to serve user needs

**Integrated view**:
The question isn't whether to cache, but what data characteristics matter for each use case:
- **Cacheable**: Public data, computed results, reference data (speed safe)
- **Fresh-required**: Security state, permissions, user identity (security critical)
- **Consistency-critical**: Anything user modifies or depends on for decisions (UX critical)

**Synthesis**: Design caching strategy by data characteristics, not blanket rules. Some data should be cached aggressively, some never cached, some needs versioning to detect staleness.

**What emerges**: The performance problem might be solvable without caching sensitive data - we're addressing the wrong problem by caching when we should optimize queries or data model.

**Unified principle**: Match data freshness strategy to the consequences of staleness for that specific data."

### Product strategy conflicts
"**Users**: The product is too expensive, we need a cheaper tier.

**Business**: We can't lower prices, margins are thin.

**Support**: Free tier generates high support burden.

**Product**: Users want features we haven't built yet.

**Tension map**:
- Price vs value received (user perspective)
- Revenue vs costs (business perspective)
- Features vs support load (operational perspective)

**Failed integration**: Lower price + cut features.
*Doesn't solve value perception, might reduce revenue.*

**Looking at what's being said**:
- Users: Not getting enough value for price
- Business: Can't reduce revenue per customer
- Support: Low-value customers are expensive to serve
- Product: We're not solving the right problems

**Integrated insight**:
The problem isn't price, it's value delivery to customer segments. We're trying to serve everyone with one offering.

**Synthesis**:
Segment by value delivered, not price:
- Self-serve tier: Powerful tools, minimal support, lower price (reduces support burden)
- Guided tier: Current features + support, current price (maintains revenue)
- Enterprise: Custom solutions, dedicated support, higher price (new revenue)

**What this integrates**:
- Users get options matching their needs
- Business maintains/grows revenue
- Support focuses on high-value relationships
- Product can optimize for different use cases

**New understanding**: We were trying to be everything to everyone. Integration reveals that differentiation serves all stakeholders better than compromise."

### Learning from project failures
"**Project A failed**: We didn't involve users early enough.

**Project B failed**: We spent too long gathering requirements.

**Project C failed**: Scope kept changing.

**Apparent contradiction**: Need more user input vs need to move faster vs need stable scope.

**Looking deeper**:
- Project A: Built wrong thing, learned late
- Project B: Analysis paralysis, market moved on
- Project C: Couldn't say no, tried to do everything

**Not contradictory - about timing and boundaries**:
- A: Feedback loop too late
- B: Feedback loop too slow
- C: Feedback loop too permissive

**Integration**:
All three point to the same principle: Learn continuously in small batches with clear constraints.
- Early user involvement (A's lesson)
- Quick validation cycles (B's lesson)
- Protected scope (C's lesson)

**Synthesized approach**:
1. Define small, testable scope
2. Get user feedback on working software
3. Learn quickly but don't expand scope
4. Repeat with next small scope

**What emerges**: The failures weren't about different problems - they were different symptoms of not managing learning cycles well. Integration reveals the meta-pattern."

### Integrating contradictory advice:
"**Advice A**: Move fast and break things.
**Advice B**: Measure twice, cut once.
**Advice C**: Perfect is the enemy of good.
**Advice D**: Quality is not negotiable.

**These seem to contradict**, but they're all useful in context.

**Integration by asking 'when'**:
- Move fast: When cost of delay exceeds cost of mistakes
- Measure twice: When mistakes are expensive or irreversible
- Perfect is the enemy: When iteration is possible and valuable
- Quality is not negotiable: When safety, security, or trust is involved

**Synthesized principle**:
Match your speed and quality bar to the cost of being wrong:
- **Experiment mode**: Fast, rough, easy to reverse (prototypes, tests)
- **Build mode**: Balanced, good enough, can iterate (features, improvements)
- **Commit mode**: Slow, careful, hard to change (architecture, security, data models)

**What this reveals**: The contradictions are features, not bugs. Different situations need different approaches. Wisdom is knowing which applies when, not picking one rule forever."

## When to use this skill

- When you have multiple perspectives or viewpoints that each seem valid but don't obviously connect
- Before dismissing conflicting information as simply wrong rather than exploring what each reveals
- When analysis has generated insights but you haven't yet woven them into actionable understanding
- When team members advocate for different approaches and you need alignment rather than choosing sides
- When research or feedback points in different directions and you need to find the coherent signal
- When constraints seem to conflict and you're tempted to sacrifice one rather than satisfy all
- Before presenting disparate findings without showing how they relate to form a complete picture
