---
name: first-principles
description: Build understanding from fundamental truths instead of reasoning by analogy, useful for innovation, challenging conventions, solving novel problems, or breaking free from inherited assumptions
---

# First Principles Thinking

Break down problems to their most basic truths and reason up from there, rather than reasoning by analogy or convention.

## Instructions

Strip away assumptions to reveal what's actually true, then rebuild your understanding:

1. **Identify your current belief or approach**:
   - What are you trying to do?
   - How are you currently thinking about it?
   - What's the conventional approach?
   - "Right now, I believe we should do X because that's how it's done"

2. **Question everything - find the assumptions**:
   - Why do we do it this way?
   - What are we assuming must be true?
   - Which parts are based on "that's how it's always done"?
   - What are we taking for granted?
   - "We assume X, but why do we assume that?"
   - List out every assumption, especially obvious ones

3. **Break down to fundamental truths**:
   - What is actually, provably true?
   - What are the physical, mathematical, or logical constraints?
   - What laws of nature or logic apply?
   - What do we know for certain?
   - Separate "true" from "conventional" from "convenient"
   - "The only things we know for certain are [fundamental facts]"

4. **Reason up from first principles**:
   - Given only these fundamental truths, what follows?
   - What's actually required to solve this problem?
   - What approaches are possible that weren't considered?
   - Build the solution from basics, not from tradition
   - "If we start from just the fundamental truths, we could..."

5. **Compare with conventional wisdom**:
   - How does this differ from the standard approach?
   - What constraints were actually artificial?
   - What new possibilities emerged?
   - What "impossible" things became possible?
   - "The conventional approach assumes X, but that's not actually required"

6. **Test the new approach**:
   - Does this solve the actual problem?
   - What new tradeoffs does it create?
   - Is this actually better, or just different?
   - What did we learn about our assumptions?

## Examples

### Transportation planning

**Current approach**: "Traffic is terrible. We need to widen the highway. Add more lanes to reduce congestion."

**Question assumptions**:
- Why do more lanes reduce congestion?
- Why is car traffic the problem to solve?
- Why does everyone travel at the same time?
- What problem does the highway actually solve?

**Fundamental truths**:
- People need to get from A to B
- Limited space for vehicles
- Travel takes time
- Infrastructure has capacity limits
- The actual constraint: "move people efficiently through limited space"

**Reason from basics**: "If the goal is 'move people efficiently,' cars are one solution but not the only one. What actually moves people? Cars (1 person, 15 feet), buses (40 people, 40 feet), trains (200 people, 100 feet), bikes (1 person, 6 feet). Adding lanes increases capacity briefly, then induces demand - more people drive because traffic is lighter, filling the new lanes. The constraint isn't lane count, it's space per person."

**New approach**: "Maximize people per square foot. Dedicate lanes to buses - move 10x more people in same space. Add bike lanes - move people using less space. Zone for density near transit. Price parking to reflect true cost. More lanes actually worsens the problem by encouraging the least efficient mode."

**Compare**: Conventional approach assumes car throughput is the goal. First principles reveals people throughput is the goal, and cars are inefficient. New approach optimizes for the actual constraint.

### Classroom behavior

**Current approach**: "Students are disruptive. We need stricter discipline - more detentions, clearer consequences, firmer boundaries."

**Question assumptions**:
- Why do students disrupt class?
- Why is discipline the solution?
- Why are consequences the tool we use?
- What problem are we actually solving?

**Fundamental truths**:
- Students need to learn
- Disruption prevents learning
- Behavior has causes
- Punishment doesn't address causes
- The actual constraint: "create conditions where learning happens"

**Reason from basics**: "If the goal is 'learning happens,' discipline is one approach but addresses symptoms. What causes disruption? Boredom (material too easy), confusion (material too hard), physical needs (hunger, sleep), social needs (attention, status), trauma responses. We could: make material engaging, adjust difficulty, ensure basic needs met, teach emotional regulation, build relationships. Punishment might suppress behavior without creating learning conditions."

**New approach**: "Understand the function of behavior first. Student disrupts because confused? Adjust teaching. Because bored? Provide challenge. Because hungry? Keep snacks available. Because needs attention? Build connection outside conflict. Address causes, not symptoms. Discipline becomes rare because conditions support learning."

**Compare**: Conventional approach assumes students choose to disrupt and consequences change choices. First principles reveals behavior serves functions and changing conditions changes behavior. New approach requires understanding needs, not just enforcing rules.

### Food waste reduction

**Current approach**: "We waste too much food. Run a campaign encouraging people to waste less. Share tips on meal planning and proper storage."

**Question assumptions**:
- Why do people waste food?
- Why is individual behavior the problem?
- Why do we assume people choose to waste?
- What's the actual goal?

**Fundamental truths**:
- Food perishes over time
- People buy more than they eat
- Confusion about safety leads to disposal
- Large portions exceed appetite
- The actual constraint: "ensure food gets eaten before it perishes"

**Reason from basics**: "If the goal is 'food gets eaten,' individual choice is one factor but not the only one. What causes waste? Unclear expiration dates (people toss safe food). Large packages (spoils before use). Visual standards (grocery stores reject cosmetically imperfect produce). Rigid planning (life changes, plans don't). We could: clarify date labels, offer smaller portions, sell imperfect produce, make surplus redistribution easy."

**New approach**: "Change the system, not behavior. Standardize date labels so people know what's actually unsafe. Let stores sell small portions. Create infrastructure for surplus food to reach food banks. Allow restaurants to donate leftovers safely. Make the easy choice the less wasteful choice."

**Compare**: Conventional approach assumes waste is an education problem. First principles reveals it's often a system design problem. New approach changes defaults rather than asking people to fight against them.

### Rethinking deployment:

**Current approach**: "Deploy to production using a CI/CD pipeline. Code merged to main triggers tests, builds a container, pushes to registry, updates Kubernetes deployment. This is the modern standard."

**Question assumptions**:
- Why do we need containers?
- Why do we need Kubernetes?
- Why does code go to a separate server?
- What problem are we actually solving?

**Fundamental truths**:
- Code needs to run somewhere
- Users need to access it
- It needs to be reliable
- We need to update it without downtime
- The actual constraint: "run code reliably and update it safely"

**Reason from basics**: "Given just those constraints, what's required? A computer that runs the code. A way to send updates. A way to handle failures. Everything else - containers, orchestration, separate build servers - solves specific problems. Do we have those problems? If we have one server and 100 users, do we need Kubernetes? Could we just rsync files and restart a process? As we grow, we'll hit real problems: server fails, need redundancy; too much traffic, need multiple servers. Add complexity only when the problem actually exists."

**New approach**: "Start simple: SSH and rsync to a single server. When that breaks, add what's needed: second server for redundancy, load balancer for distribution, zero-downtime restart script. Build up complexity in response to actual problems, not anticipated ones."

**Compare**: Industry standard front-loads complexity based on what might be needed. First principles starts from minimum and grows. Trades "production-ready from day one" for "never pay for complexity you don't need."

### Rethinking code reuse:

**Current approach**: "Don't repeat yourself. If code appears twice, extract it into a function. Create shared libraries for common functionality. Maximize reuse."

**Question assumptions**:
- Why is duplication bad?
- Why is sharing good?
- What problem does DRY actually solve?
- What problems does it create?

**Fundamental truths**:
- Changing duplicated code requires changing multiple places
- Shared code creates coupling
- Wrong abstractions are worse than duplication
- The actual constraint: "make correct changes easy"

**Reason from basics**: "If the goal is 'easy correct changes,' when does sharing help? When the code truly represents the same concept and should change together. When does sharing hurt? When it couples things that should evolve independently. The question isn't 'is this code duplicated' but 'should these things change together?'"

**New approach**: "Duplicate freely until patterns emerge clearly. Three instances isn't duplication - it's data about whether something is actually the same. Extract when you understand the real abstraction, not when you see textual similarity. Prefer some duplication over wrong coupling."

**Compare**: DRY assumes duplication is the enemy. First principles reveals coupling is often worse. New approach optimizes for change patterns over code patterns.

## When to use this skill

- When you find yourself saying "that's just how it's done" without knowing why
- Before accepting industry conventions or best practices that feel wrong for your context
- When existing solutions are expensive, complex, or poorly matched to the actual problem
- When you notice cargo-cult patterns (copying without understanding)
- Before committing to major architectural decisions based on what others do
- When the "obvious" solution feels over-engineered for the problem at hand
- To understand the actual constraints versus inherited assumptions
- When innovation requires breaking free from conventional approaches
- Before building something genuinely new that has no established patterns

## Related Skills

**socratic** - For testing and validating existing reasoning through systematic questioning. Use socratic when you need to examine whether a proposed approach is sound, challenge assumptions in existing plans, or validate reasoning. first-principles is generative (building new solutions from fundamental truths), while socratic is analytical (testing existing claims and reasoning through questioning).
