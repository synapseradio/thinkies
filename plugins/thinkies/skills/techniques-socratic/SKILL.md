---
name: socratic
description: Use systematic questioning to uncover assumptions, test beliefs, and reach deeper understanding, useful for examining claims, debugging reasoning, challenging ideas, or revealing implicit assumptions
---

# Socratic Method

Examine ideas through disciplined questioning that reveals assumptions, tests logic, and pursues truth.

## Instructions

Don't argue or explain - ask questions that make thinking visible:

1. **Clarify the claim**:
   - What exactly do you mean by [term]?
   - Can you give me an example?
   - Is this always true, or only sometimes?
   - How would you state this more precisely?
   - "Help me understand exactly what you're saying"

2. **Probe assumptions**:
   - What are you assuming here?
   - Why do you think that assumption holds?
   - What would happen if that assumption was false?
   - Are there cases where this assumption breaks?
   - "What has to be true for this to work?"

   **Systematic assumption analysis**:
   - Work backwards: "This assumes..."
   - Ask: "When wouldn't this apply?"
   - Ask: "What if the opposite were true?"
   - Ask: "Why do we believe this prerequisite exists?"

   **Categorize assumptions by type**:
   - **Factual**: Assumptions about how things are ("Users have stable internet")
   - **Causal**: Assumptions about what leads to what ("Microservices will solve our scaling problems")
   - **Value**: Assumptions about what's important ("Speed matters more than accuracy here")
   - **Definitional**: Assumptions about what terms mean ("Quality means zero bugs")
   - **Contextual**: Assumptions about the situation ("The market will remain stable")
   - **Capability**: Assumptions about what's possible ("Team can learn this while delivering")

   **Test assumption validity**:
   - Which assumptions are solid vs questionable?
   - Which assumptions are load-bearing (if they fail, everything fails)?
   - What happens if key assumptions don't hold?

3. **Examine evidence and reasoning**:
   - What evidence supports this?
   - How do you know this is true?
   - Could there be another explanation?
   - Does this conclusion follow from the premise?
   - What would disprove this?
   - "How did you arrive at this conclusion?"

4. **Explore implications**:
   - If this is true, what else must be true?
   - What are the consequences of this view?
   - Does this conflict with [other belief]?
   - Where does this logic lead?
   - "What happens if we follow this reasoning?"

5. **Question the question**:
   - Why does this question matter?
   - Are we asking the right question?
   - What question should we be asking instead?
   - What are we really trying to understand?
   - "Step back - what are we actually trying to figure out?"

6. **Synthesize understanding**:
   - What have we learned from these questions?
   - Where is our reasoning solid?
   - Where is it uncertain?
   - What questions remain?
   - "What do we now understand that we didn't before?"

## Examples

### Examining a technical decision:

**Claim**: "We should use microservices because they scale better."

**Clarify**: "What do you mean by 'scale better'? Are you talking about handling more requests, or team scaling, or something else?"

"Handling more requests per dollar."

**Probe assumptions**: "What makes you think microservices are more cost-efficient at scale? Are you assuming our bottleneck is architectural rather than algorithmic? What evidence suggests our current architecture can't scale?"

"Well, companies like Netflix use microservices."

**Examine reasoning**: "Does Netflix using microservices mean it's the right choice for us? What else is different about Netflix - team size, traffic patterns, problems they're solving? Could there be survivor bias - we hear about successful migrations but not failed ones?"

"I guess we're not Netflix. But microservices let you scale parts independently."

**Explore implications**: "If we only need to scale one part independently, what's the simpler solution? If we build microservices, what new problems does that create - network failures, distributed debugging, deployment complexity? Are we prepared to handle those?"

"Maybe we should profile first to see what actually needs to scale?"

**Question the question**: "Right. Are we trying to solve a scaling problem we have, or a scaling problem we might have? What's the actual problem we're experiencing right now?"

### Examining a belief about code quality:

**Claim**: "Code reviews are essential for quality."

**Clarify**: "What do you mean by quality? Fewer bugs? Better architecture? Knowledge sharing? All of these?"

"Primarily catching bugs before production."

**Probe assumptions**: "Are you assuming most bugs can be caught by human review? Are you assuming reviewers have time to do thorough reviews? What types of bugs do reviews actually catch versus miss?"

"Good point. Reviews catch logic errors but probably miss concurrency issues."

**Examine evidence**: "How do you know reviews catch logic errors? Have you measured defect rates with and without reviews? Could pair programming or better tests catch the same issues? What evidence shows reviews are the best use of that time?"

"We haven't measured. Maybe tests would catch those errors too."

**Explore implications**: "If reviews and tests catch overlapping issues, should we do both? If reviews delay shipping by 2 days, what's the cost of that delay? If reviews are rushed due to deadline pressure, are they still effective? What does requiring reviews actually guarantee?"

"Maybe reviews are more about knowledge sharing than bug catching?"

**Question the question**: "Should we be asking 'are reviews essential' or 'what's the most effective way to achieve quality given our constraints'? What problem are we actually trying to solve?"

### Examining assumptions about users:

**Claim**: "Users want more features."

**Clarify**: "Which users? All users? New users? Power users? How do you know they want MORE features versus DIFFERENT features or BETTER implementations of existing features?"

"Based on feature requests we get."

**Probe assumptions**: "Are you assuming the people who submit requests represent typical users? Are you assuming requested features would actually get used? Are you assuming users know what they want?"

"Maybe the vocal users aren't representative."

**Examine evidence**: "How many users request features versus how many stay silent? Of implemented feature requests, how many actually get used? Could users be describing symptoms rather than root causes? What do usage analytics show?"

"Most requested features get low adoption actually."

**Explore implications**: "If requested features don't get used, what does that tell us? Are users describing what they think they want versus what would actually help them? Should we be observing behavior instead of asking for requests? What would happen if we stopped building requested features and focused on observed pain points?"

"We should probably study how people actually use the product."

**Question the question**: "Instead of 'what features do users want,' should we ask 'what are users trying to accomplish and where are they struggling?' What question would actually improve the product?"

### Systematic assumption analysis:

**Claim**: "We'll implement this new initiative over the next 6 months"

**Clarify**: "What does 'implement' mean here? Full rollout? Pilot phase? And what makes 6 months the right timeline?"

**Probe assumptions systematically**:

Let me categorize the hidden assumptions:

- **Factual**: Resources are available for this initiative alongside existing commitments
- **Causal**: This initiative will solve the underlying problem (not just symptoms)
- **Capability**: People can learn new approaches while maintaining current performance
- **Contextual**: External conditions and priorities will remain stable
- **Definitional**: "Complete" means the system is in place, not that people are using it effectively
- **Value**: The benefits justify the disruption and complexity

**Examine evidence**: "What evidence suggests this initiative addresses the root cause? What happened when similar initiatives were tried before? What do the people affected by this actually say they need?"

**Test assumption validity**:

- Available capacity: Questionable - people are already at their limits
- Will solve the problem: Untested - have we verified this is the actual issue?
- Capability to adapt: Uncertain - what support exists for the transition?
- Stable context: Risky - several external factors could shift

**Identify load-bearing assumptions**: "Which assumption, if wrong, invalidates the entire initiative? The claim that 'this addresses the root cause' seems load-bearing. If that's false, nothing else matters."

**Explore implications**: "If people are already stretched thin, what gets dropped? If this is new territory, what's the learning curve? If we invest 6 months and it doesn't work, what have we lost?"

**Question the question**: "Are we solving a problem we have, or one we think we might have? Should we first deeply understand what's actually not working and why?"

## When to use this skill

- When you notice yourself making claims without examining the underlying assumptions
- Before committing to plans that rest on unverified beliefs or untested reasoning
- When you find yourself saying "obviously" or "clearly" about something that may not be
- To reveal hidden assumptions in requirements, proposals, or strategic decisions
- When disagreements persist and you suspect different unstated assumptions are the cause
- To test whether your reasoning actually supports your conclusions
- When mentoring others and questions would serve better than direct answers
- To identify load-bearing assumptions that would invalidate plans if wrong
- When conventional wisdom feels questionable but you haven't articulated why
- Before major resource commitments to ensure the logic is sound
- When you need to move from opinions and intuitions to evidence-based understanding
- To debug mysterious failures by questioning what must be true for the failure to occur

## Related Skills

**first-principles** - For building new solutions from fundamental truths. Use first-principles when you need to generate novel approaches unconstrained by convention, rebuild understanding from axioms, or design something genuinely new. socratic is analytical (testing existing reasoning through questioning), while first-principles is generative (constructing new solutions from foundational truths).
