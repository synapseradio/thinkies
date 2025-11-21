---
name: reversal
description: Flip problems, assumptions, and approaches upside down to discover insights hidden by conventional framing, often revealing solutions that forward thinking misses
---

# Reversal

Turn problems inside out and upside down to see what conventional thinking obscures.

## Instructions

Reversal works by deliberately inverting elements of your problem or solution space:

### 1. Reverse the goal
**Instead of solving the problem, solve the opposite**

If your goal is: "How do we increase user retention?"
Reverse it: "How could we drive users away?"

Then list everything that would achieve the reversed goal:
- Make the product confusing
- Ignore user feedback
- Add annoying friction
- Break things frequently
- Provide terrible support
- Make it slow and buggy

**Now flip the insights**: Do the opposite of each item to reveal your actual strategy. This often surfaces non-obvious solutions you'd miss asking the question normally.

Example: "Terrible support drives users away, so amazing support retains them - but 'amazing' might mean proactive help before they even ask, not just responsive tickets."

### 2. Reverse the sequence
**Do things in opposite order**

Normal order: Plan → Build → Test → Ship
Reversed: Ship → Test → Build → Plan

Ask: "What if we had to ship first? We'd need:
- Something that worked immediately
- Ability to iterate live
- Customer feedback driving design
- Minimal upfront planning"

This suggests: start with the smallest shippable thing and evolve it based on real usage.

Example: "We usually write code then documentation. What if we wrote documentation first? It would force us to think about the API from the user's perspective before implementing."

### 3. Reverse the relationship
**Flip who does what to whom**

Normal: "System serves user"
Reversed: "User serves system"

This sounds backwards, but asking "What if users had to serve the system?" reveals:
- Where we're making users do system work (captchas, form validation, manual data entry)
- Where we could flip it back (auto-fill, smart defaults, AI assistance)

Example: "We have the system validate user input. What if users validated system output? That's actually code review - developers check what the compiler produces. Could we apply that pattern? Let the system generate, users approve or reject."

### 4. Reverse the problem frame
**Change what you're optimizing for**

Instead of: "How do we make this faster?"
Try: "How do we make slowness acceptable or even beneficial?"

This reveals solutions like:
- Progress indicators that make waits feel shorter
- Using wait time for something valuable (preloading, tips, previews)
- Making deliberate slowness a feature (forced patience, thoughtfulness)

Example: "Instead of making deploy faster, what if we made it slower but safer? That reframes to focus on confidence over speed, suggesting better testing and gradual rollouts."

### 5. Reverse the user journey
**Start from the end and work backward**

Normal journey: Discover → Sign up → Onboard → Use → Retain
Reversed: Retain → Use → Onboard → Sign up → Discover

Working backward from retention:
- What keeps long-term users? Deep feature usage.
- What enables deep usage? Good onboarding.
- What makes onboarding work? Clear value from signup.
- What drives signup? Strong discovery experience.

This often reveals: we should design for long-term users first, then simplify that for new users, not build for new users and hope they become long-term.

### 6. Reverse the ownership
**Flip who's responsible**

Normal: "We're responsible for uptime"
Reversed: "Users are responsible for uptime"

Sounds wrong, but exploring it reveals:
- What if users could run it locally? (Offline-first design)
- What if users hosted their own? (Self-hosted option)
- What if users could mirror it? (Distributed architecture)

Even if you don't go full reversal, this reveals resilience opportunities.

### 7. Reverse the constraint
**Turn limitation into abundance, or vice versa**

If limited by time: "What if we had infinite time?"
Reveals: What would we build with no deadline? That's your ideal vision.

Then reverse: "What if we had zero time?"
Reveals: What's the absolute minimum? That's your MVP.

The tension between these reveals your real scope.

Example: "We have a small team. Reversing: What if we had 100 people? We'd specialize, have dedicated roles, build everything custom. But we can't, so we need: automation, good tools, focus on core value, buy don't build."

### 8. Reverse the perspective
**Look from the opposite side**

If you're the seller: Think like the buyer
If you're the platform: Think like the developer
If you're the system: Think like the data

Example: "We're building an API for developers. Reverse: we're developers using this API. What pisses us off? Complex auth, inconsistent naming, poor errors, missing examples. So we need the opposite: simple auth, consistent naming, clear errors, lots of examples."

## How to practice reversal

**Make it systematic**: Don't just reverse randomly. Pick one specific element (goal, sequence, relationship, etc.) and fully explore its reversal.

**Push through discomfort**: Reversals often feel wrong initially. That discomfort means you're breaking out of conventional thinking. Stay with it.

**Look for the kernel**: You won't implement most reversals directly, but they contain seeds of insight. Extract the useful part.

**Combine reversals**: Try reversing multiple elements at once. "What if users controlled the system, and we worked backward from their ideal end state?"

## Examples

### Product strategy:
"We want to grow our user base.

**Normal approach**: Marketing, SEO, ads, partnerships.

**Reversal - How could we shrink our user base?**
- Make it exclusive and invite-only
- Remove features people use
- Increase prices dramatically
- Make it harder to sign up
- Only serve a tiny niche

**Extracting insights**:
- Exclusive/invite-only actually creates demand (scarcity)
- Removing features forces focus on what matters most
- Higher price signals quality and filters for serious users
- Friction in signup ensures committed users
- Tiny niche means deep loyalty

**Result**: Maybe growth isn't about more users, but better users. What if we made it invite-only for the first year, positioned as exclusive, charged more, and owned a small niche completely? That might grow better long-term than chasing everyone."

### Technical architecture:
"Our microservices are too complex to manage.

**Normal thinking**: Better orchestration, service mesh, observability.

**Reversal - What if we had a monolith?**
- Simpler deployment
- Easier debugging
- No network calls
- Shared database
- Single codebase

**Insights from reversal**:
- We split too early or too finely
- Some services should be merged
- We're paying complexity cost for benefits we don't need
- Network overhead might not be worth it

**Action**: Merge related services back together. We went from 20 microservices to 6 larger services. Complexity dropped, performance improved."

### User experience:
"Users aren't completing our checkout flow.

**Normal optimization**: Fewer steps, clearer UI, progress bar, saved info.

**Reversal - How could we make checkout worse?**
- More steps and friction
- Confusing navigation
- Hidden costs revealed late
- Require account creation
- No guest checkout
- Complex forms

**Insight from reversal**:
- We're doing several of these! Hidden shipping costs, forced account, complex address form.

**Deeper reversal - What if we made friction intentional?**
- Show total cost upfront (friction becomes trust)
- Make account creation valuable (friction becomes benefit)
- Slow down impulse buys (friction becomes thoughtfulness)

**Result**: We redesigned not to remove all friction, but to make the right friction valuable. Show full price immediately, make account optional but beneficial, add a 'confirm your order' step that reduces buyer's remorse."

### Team process:
"Our code reviews take too long.

**Normal solution**: Review faster, fewer approvals, automated checks.

**Reversal - What if reviews took even longer?**
- More reviewers required
- Deeper analysis needed
- Mandatory discussion
- Multi-day waiting period

**Insight**:
- Maybe speed isn't the problem, quality is
- What if longer reviews but fewer PRs? (Batch changes)
- What if we front-load review in pairing? (Review before PR)
- What if some changes needed deep review, others auto-approved? (Categorize by risk)

**Result**: We split PRs into 'trivial' (auto-merge if tests pass) and 'significant' (deep review required). Average review time went up slightly, but important changes get proper attention and trivial ones don't block."

## When to use this skill

- When obvious solutions aren't working
- Breaking out of conventional thinking
- Finding non-obvious insights
- Challenging status quo or assumptions
- Reframing problems that feel stuck
- Discovering what you're missing in current approach
- Testing if you're solving the right problem
- Generating creative alternatives
- Understanding systems from new angles
