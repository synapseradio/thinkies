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

### Product feature prioritization

**White Hat**: "Feature A would take 2 weeks, requested by 15 users. Feature B takes 1 week, requested by 3 enterprise clients. Current sprint has 3 weeks capacity. Revenue from enterprise is 60% of total."

**Red Hat**: "Feature A feels more fun to build. Anxious about enterprise clients leaving. Frustrated that small requests take so long. Excited about Feature B's technical challenge."

**Black Hat**: "Feature A might not actually solve the user problem - they asked for X but might need Y. Feature B serves only 3 clients, risky dependency. Both could have scope creep. We haven't validated either assumption."

**Yellow Hat**: "Feature A could unlock viral growth - those 15 users are influencers. Feature B demonstrates we listen to enterprise, could lead to upsells. Either would boost team morale. Both are technically feasible."

**Green Hat**: "What if we ship a minimal version of both? Could Feature A be a setting instead of new code? What if we interview those 15 users first? Could we do Feature B as a plugin? What about a completely different approach to both problems?"

**Blue Hat**: "Green Hat revealed we're guessing at solutions. White Hat shows enterprise dependency. Next step: 30-minute calls with 3 of the 15 users and 2 of the 3 enterprise clients to validate actual needs before building either."

### Career transition decision

**White Hat**: "Current role pays $90k, 5 years experience in field, new offer pays $110k in different industry, would require relocation to higher cost city, have $40k savings, partner's job is location-dependent."

**Red Hat**: "Excited by the challenge but terrified of failing in unfamiliar territory. Feel stuck in current role. Anxious about uprooting my partner. Gut says this is a once-in-a-decade opportunity but also that timing is terrible."

**Black Hat**: "Skills may not transfer as well as I think. Cost of living increase could eat the salary bump. Partner might resent the move. New industry is volatile - could be laid off within a year. Leaving established network and reputation."

**Yellow Hat**: "Could accelerate career growth significantly. New skills would make me more versatile. Partner has talked about wanting a change too. Savings provide 6-month runway. Could always return to this field with broader experience."

**Green Hat**: "What if I negotiated remote work for the new role? Could I try a 3-month contract first? What if partner found work in new city before we moved? Could current employer counter-offer with new responsibilities? What about a sabbatical to test the waters?"

**Blue Hat**: "Emotional pull is strong but risks are real. Missing information about partner's actual preferences and new city job market. Next step: Have honest conversation with partner about their priorities. Research cost of living calculator for real numbers. Ask new employer about trial period or remote options."

### Technical debt prioritization

**White Hat**: "Monolithic codebase, 8 identified areas of technical debt, team of 5 engineers, debt items range from 1 week to 2 months effort, feature velocity has dropped 30% over 6 months, no production outages but debugging takes longer."

**Red Hat**: "Frustrated by slow progress. Feel embarrassed showing this code to new hires. Anxious that we're one incident away from a crisis. Excited about the idea of clean architecture but overwhelmed by the scope."

**Black Hat**: "Refactoring could introduce new bugs. Business won't see value in technical work. Two months is an eternity - priorities will shift. Team lacks experience with the proposed architecture. Could spend all this time and velocity still doesn't improve."

**Yellow Hat**: "Clean architecture could attract better engineers. Velocity improvement would compound over time. Some refactoring could happen incrementally during feature work. Could use this to mentor junior engineers. Modern architecture might enable features currently impossible."

**Green Hat**: "What if we refactor only the most painful module first? Could we do 20% of the work for 80% of the benefit? What about strangler fig pattern - new code in new architecture, gradually migrate? Could we timebox exploration - 1 week to prove feasibility? What if we made it a background task during slow periods?"

**Blue Hat**: "The anxiety about crisis and velocity drop are key signals. Yellow and Green hats suggest incremental approach rather than big-bang rewrite. Next step: Identify single highest-pain module. Timebox 1 week to refactor it and measure impact on debugging time. Use that data to decide on further investment."

## When to use this skill

- When you notice yourself stuck in one perspective and can't see other angles
- Before making decisions where emotions are running high and clouding judgment
- When analysis paralysis is setting in from trying to think about everything at once
- To deliberately separate facts from feelings from risks from opportunities
- When group discussions keep conflating different types of thinking
- When you need to get past knee-jerk reactions to evaluate something fairly
- To balance your natural tendency toward either optimism or caution
- When creative alternatives are needed after getting stuck in logical analysis
- Before evaluating proposals where people have entrenched positions
- To ensure comprehensive thinking across multiple dimensions of a complex decision

## Related Skills

**perspective-shift** - For flexible viewpoint changes without a predefined framework. Use perspective-shift when you want to freely explore different stakeholder viewpoints or system angles. six-hats provides a structured framework with six specific thinking modes (facts, emotions, risks, benefits, creativity, process), which is particularly useful for group decision-making or systematic analysis where you want shared vocabulary and clear separation of thinking types.
