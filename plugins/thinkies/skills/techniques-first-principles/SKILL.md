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

### Rethinking API design:

**Current approach**: "We need to version our API. The standard is to put v1, v2 in the URL path. When we make breaking changes, we increment the version."

**Question assumptions**:
- Why do breaking changes require new versions?
- Why do versions go in the URL?
- Why do all endpoints version together?
- What problem does versioning actually solve?

**Fundamental truths**:
- Clients depend on specific behavior
- Code evolves and changes
- Breaking client code is bad
- Maintaining many versions is expensive
- The actual constraint: "don't break existing clients while improving the API"

**Reason from basics**: "If the only real requirement is 'don't break existing clients,' what actually achieves that? We could: add new fields without removing old ones, accept both old and new formats, make changes backward compatible, version individual fields instead of entire endpoints, let clients specify what they support. The conventional 'v1/v2' approach is one solution, but not the only one."

**New approach**: "Use backward-compatible evolution. Add new optional fields. Deprecated fields stay forever but return null. Clients declare capabilities via headers. Never need v2 because nothing breaks. Only version when truly incompatible formats needed, and do it per-endpoint, not API-wide."

**Compare**: Conventional approach assumes changes must break things and versions must be global. First principles reveals that's only one path. The new approach trades field proliferation for version maintenance.

### Rethinking authentication:

**Current approach**: "Users need passwords. We'll hash them with bcrypt, have a forgot-password flow, enforce complexity requirements, require changes every 90 days."

**Question assumptions**:
- Why do users need passwords?
- Why does the password live in our database?
- Why do WE authenticate users?
- Why is this our responsibility?

**Fundamental truths**:
- We need to know who is making requests
- We need to prevent unauthorized access
- Users need a way to prove identity
- The actual constraint: "reliably identify users without friction"

**Reason from basics**: "If the goal is just 'identify users reliably,' passwords are one solution, but they shift security burden to users and us. What else identifies uniquely? Email they control. Phone they possess. Hardware token they own. Biometrics. We could send a login link to their email - proves they control it. We could use magic links exclusively - no password to store, hash, forget, or crack."

**New approach**: "Passwordless authentication via email magic links. User enters email, we send a time-limited token. Click link, you're in. No passwords to manage, no password resets, no complexity requirements, no password database to breach. Trust the email provider's security."

**Compare**: Conventional approach assumes we must store and verify secrets. First principles shows we can delegate to email providers. Trades one security problem (password management) for another (email account security), but users already secure their email.

### Rethinking meeting scheduling:

**Current approach**: "Finding meeting times is hard. We need a tool that checks everyone's calendar, finds overlaps, sends invites. Use Calendly or similar."

**Question assumptions**:
- Why do we need everyone at the same time?
- Why does it need to be synchronous?
- Why is finding overlap the problem we're solving?
- What's the actual goal?

**Fundamental truths**:
- We need to exchange information or make decisions
- People have different schedules
- Time is limited
- Context switching is expensive
- The actual constraint: "effectively collaborate given different schedules"

**Reason from basics**: "If the goal is 'effective collaboration,' real-time presence is one approach but not always needed. What actually requires synchronous time? Brainstorming, heated debate, building rapport. What doesn't? Status updates, information sharing, most decisions. We could: async document collaboration, recorded video updates, discussion threads with clear decision deadlines, only meet for genuine synchronous work."

**New approach**: "Default to async. Write the proposal in a doc, give people 48 hours to comment, make the decision. Use meetings only for: complex disagreements, creative brainstorming, or sensitive conversations. Stop trying to optimize calendar Tetris; optimize for the outcome."

**Compare**: Conventional wisdom treats meetings as default. First principles reveals most "meetings" are information transfer that doesn't need synchronous time. New approach eliminates most scheduling problems by eliminating most meetings.

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

- Challenging industry conventions
- Designing novel solutions
- When "best practices" don't fit your context
- Breaking through innovation barriers
- Questioning expensive or complex systems
- Simplifying over-engineered solutions
- Understanding why things work the way they do
- Finding creative solutions to constraints
- Avoiding cargo-cult engineering
- Building something genuinely new
