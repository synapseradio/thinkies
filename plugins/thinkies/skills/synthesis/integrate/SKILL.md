---
name: integrate
description: Weave diverse threads into coherent wholes that preserve nuance while creating unity, useful when combining multiple perspectives, reconciling tensions, or building comprehensive understanding from parts
---

# Integrate

Combine multiple ideas, perspectives, or insights into a coherent whole that's greater than the sum of parts.

## Instructions

When integrating:

1. **Lay out what you're combining**:
   - List the pieces clearly
   - Note where they come from
   - Acknowledge their individual value
   - Don't simplify them yet

2. **Find points of contact**:
   - Where do they naturally touch?
   - Where do they support each other?
   - Where do they fill each other's gaps?
   - What does one explain about another?

3. **Address tensions**:
   - Where do they conflict?
   - Are conflicts real or apparent?
   - Can both be true in different contexts?
   - What does the tension reveal?

4. **Build the synthesis**:
   - What's the larger picture they create together?
   - How does each piece fit in?
   - What emerges that wasn't in any single piece?
   - What's the organizing principle?

5. **Test coherence**:
   - Does this hold together?
   - Does it preserve what matters from each piece?
   - Does it create new understanding?
   - Can you explain it simply?

6. **Check what's missing**:
   - What gaps remain?
   - What doesn't fit?
   - What new questions arise?

## Examples

### Integrating technical perspectives:
"**Performance engineer says**: We need caching everywhere, database queries are killing us.

**Security engineer says**: Caching sensitive data is a huge risk, we need fresh data.

**User researcher says**: Users care about consistency more than raw speed.

**Tension**: Speed vs security vs consistency.

**Integration attempt 1**: Cache some things but not others.
*Too simple - doesn't resolve the underlying tensions.*

**Deeper look**:
- Performance problem is real (slow queries)
- Security concern is real (cached sensitive data)
- Consistency issue is real (stale data confusion)
- All three are trying to serve the user

**Integrated view**:
The real question isn't whether to cache, but what data characteristics matter for each use case:
- **Cacheable**: Public data, computed results, reference data (speed safe)
- **Fresh-required**: Security state, permissions, user identity (security critical)
- **Consistency-critical**: Anything user modifies or depends on for decisions (UX critical)

**Synthesis**: Design caching strategy by data characteristics, not by blanket rules. Some data should be cached aggressively, some should never be cached, some needs versioning to detect staleness.

**What emerges**: The performance problem might be fixable without caching sensitive data - we're solving the wrong problem by caching when we should be optimizing queries or data model.

**Unified principle**: Match data freshness strategy to the consequences of staleness for that specific data."

### Integrating user feedback and business needs:
"**Users say**: The product is too expensive, we need a cheaper tier.

**Business says**: We can't lower prices, margins are already thin.

**Support says**: Free tier generates massive support burden.

**Product says**: Users want features we haven't built yet.

**Tension map**:
- Price vs value received (user perspective)
- Revenue vs costs (business perspective)
- Features vs support load (operational perspective)

**Failed integration**: Lower price + cut features.
*Doesn't solve value perception, might hurt business more.*

**Looking at what's really being said**:
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

### Integrating learning from multiple failures:
"**Project A failed**: Because we didn't involve users early enough.

**Project B failed**: Because we spent too long gathering requirements.

**Project C failed**: Because scope kept changing.

**Apparent contradiction**: Need more user input vs need to move faster vs need stable scope.

**Looking deeper**:
- Project A: Built wrong thing, learned late
- Project B: Analysis paralysis, market moved on
- Project C: Couldn't say no, tried to do everything

**Not contradictory - they're about timing and boundaries**:
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

- Combining multiple viewpoints
- Resolving apparent contradictions
- Building comprehensive understanding
- Creating shared vision from diverse inputs
- Synthesizing research or feedback
- Finding solutions that satisfy multiple constraints
- Moving from analysis to action
- Building team alignment
- Creating frameworks from examples
