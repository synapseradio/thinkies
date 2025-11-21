---
name: six-hats
description: Explore problems from six distinct perspectives to achieve balanced, comprehensive thinking, useful for decision-making, planning, problem-solving, or breaking out of narrow viewpoints
---

# Six Thinking Hats

Systematically examine a problem from six different perspectives, one at a time, to avoid conflating different types of thinking.

## Instructions

Work through each hat in sequence. Don't mix hats - fully explore one perspective before moving to the next.

1. **White Hat - Facts and Information**:
   - What do we know?
   - What data do we have?
   - What information is missing?
   - What facts are relevant?
   - No interpretation, just objective information

2. **Red Hat - Emotions and Intuition**:
   - How do I feel about this?
   - What's my gut reaction?
   - What emotions does this trigger?
   - What do others feel about this?
   - No justification needed - pure emotional response

3. **Black Hat - Caution and Risks**:
   - What could go wrong?
   - What are the weaknesses?
   - What obstacles exist?
   - Why might this fail?
   - What are the downsides?
   - Focus on legitimate concerns, not pessimism

4. **Yellow Hat - Benefits and Optimism**:
   - What could go right?
   - What are the benefits?
   - What opportunities exist?
   - Why might this succeed?
   - What's the best case scenario?
   - Focus on realistic positives, not wishful thinking

5. **Green Hat - Creativity and Alternatives**:
   - What are other possibilities?
   - How else could we approach this?
   - What's a wild idea?
   - Can we combine approaches?
   - What if we changed the constraints?
   - Generate options without judgment

6. **Blue Hat - Process and Overview**:
   - What have we learned from all perspectives?
   - What patterns emerged?
   - What's the next step?
   - How should we proceed?
   - What thinking do we need more of?
   - Synthesize and organize

## Examples

### Software architecture decision:

**White Hat**: "We have 3 services running on EC2, averaging 60% CPU. Current architecture is monolithic. Budget is $5k/month. Team has 4 developers, all know Node.js, two know Go."

**Red Hat**: "I'm excited about microservices but anxious about the complexity. My gut says our team isn't ready. I feel pressure to modernize but also protective of our working system."

**Black Hat**: "Risk of over-engineering. Team lacks distributed systems experience. Could introduce network failures, debugging difficulty, deployment complexity. Might slow down development initially. No clear problem we're solving."

**Yellow Hat**: "Could enable independent scaling of hot paths. Teams could deploy independently. Might attract better talent. Could handle future growth. Opportunity to learn modern architecture."

**Green Hat**: "What about modular monolith first? Or extract just the authentication service? Could we do feature flags instead? What if we kept monolith but improved observability? Hybrid approach where new features are services?"

**Blue Hat**: "The emotional resistance and risk analysis outweigh the speculative benefits. Missing key information about what problem we're actually solving. Next step: identify specific pain points in current system. If performance, profile first. If team velocity, look at modular monolith."

### Product feature prioritization:

**White Hat**: "Feature A would take 2 weeks, requested by 15 users. Feature B takes 1 week, requested by 3 enterprise clients. Current sprint has 3 weeks capacity. Revenue from enterprise is 60% of total."

**Red Hat**: "Feature A feels more fun to build. Anxious about enterprise clients leaving. Frustrated that small requests take so long. Excited about Feature B's technical challenge."

**Black Hat**: "Feature A might not actually solve the user problem - they asked for X but might need Y. Feature B serves only 3 clients, risky dependency. Both could have scope creep. We haven't validated either assumption."

**Yellow Hat**: "Feature A could unlock viral growth - those 15 users are influencers. Feature B demonstrates we listen to enterprise, could lead to upsells. Either would boost team morale. Both are technically feasible."

**Green Hat**: "What if we ship a minimal version of both? Could Feature A be a setting instead of new code? What if we interview those 15 users first? Could we do Feature B as a plugin? What about a completely different approach to both problems?"

**Blue Hat**: "Green Hat revealed we're guessing at solutions. White Hat shows enterprise dependency. Next step: 30-minute calls with 3 of the 15 users and 2 of the 3 enterprise clients to validate actual needs before building either."

## When to use this skill

- Group decision-making sessions
- When stuck in one perspective
- Complex decisions with multiple stakeholders
- Breaking analysis paralysis
- Getting past emotional reactions
- Balancing optimism and caution
- Generating creative alternatives after logical analysis
- Conflict resolution where people are attached to positions
- Strategic planning
- Evaluating opportunities or proposals
