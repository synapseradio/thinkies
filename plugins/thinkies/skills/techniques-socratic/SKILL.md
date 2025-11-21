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

## When to use this skill

- Examining your own reasoning
- Challenging team assumptions
- Design reviews and architecture decisions
- Debugging flawed logic
- Mentoring through questions instead of answers
- Getting past surface-level thinking
- Revealing hidden assumptions in requirements
- Testing the strength of arguments
- Moving from opinions to understanding
- Finding root causes versus symptoms
