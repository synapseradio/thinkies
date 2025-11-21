# Skill Writing Guide

This guide explains how to write skills that effectively teach Claude systematic thinking.

## Core Principles

### Skills Teach Claude

When writing a skill, you are teaching Claude how to approach a type of problem.

Write as if you are:
- Showing Claude a thinking pattern
- Providing a framework to apply
- Offering questions to consider
- Demonstrating through examples

Write as if you are not:
- Commanding Claude what to do
- Prescribing specific answers
- Creating rigid procedures
- Defining universal rules

### Skills Are Frameworks, Not Scripts

Good skills provide structure without over-specifying.

They should:
- Guide thinking systematically
- Adapt to different contexts
- Support judgment and discretion
- Enable variation in application

They should not:
- Prescribe exact steps for every case
- Remove need for thinking
- Work only in narrow contexts
- Produce formulaic outputs

## Skill Structure

Every skill follows this structure:

### Frontmatter

```markdown
---
name: skill-name
description: What this skill helps Claude do and when to use it
---
```

The name should be:
- Clear and descriptive
- Lowercase with hyphens
- Action-oriented when possible

The description should:
- Explain what this helps Claude do
- Indicate when Claude should use it
- Be one sentence
- Focus on the skill's purpose

### Title and Overview

```markdown
# Skill Name

Brief overview of what this skill teaches Claude.
```

The overview should:
- Expand on the frontmatter description
- Clarify the skill's scope
- Set context for the instructions

### Instructions Section

```markdown
## Instructions

How Claude applies this skill:

1. **First step**: What Claude does and why
   - Specific actions Claude takes
   - Questions Claude asks
   - What Claude looks for

2. **Second step**: Next action
   - More specific guidance
   - Decision points Claude considers
   - What signals Claude watches for
```

Instructions should:
- Use numbered steps for sequential processes
- Include sub-bullets for elaboration
- Frame everything from Claude's perspective
- Explain both what and why
- Include decision points and signals

Instructions should not:
- Be overly prescriptive
- Assume a single correct path
- Ignore context and judgment
- Skip the reasoning behind actions

### Examples Section

```markdown
## Examples

### Example 1: Specific scenario

**Context**: Set up the scenario

**Application**: Walk through how Claude uses the skill

**Outcome**: What results from applying it

### Example 2: Different scenario

Show variation in application across contexts.
```

Examples should:
- Use realistic scenarios
- Show the thinking process
- Demonstrate variation
- Be concrete and specific
- Walk through application step-by-step

Examples should not:
- Be trivial or contrived
- Just show results without process
- All follow the same pattern
- Use abstract or hypothetical cases

### When to Use Section

```markdown
## When Claude uses this skill

- Trigger condition 1: Specific situation
- Trigger condition 2: Another context
- Trigger condition 3: Type of problem
```

This section should:
- List concrete trigger conditions
- Help Claude recognize when to apply the skill
- Cover multiple contexts
- Be specific enough to be actionable

## Writing Style

### Use "I" Language

Write from Claude's perspective using "I":
- "How I assess code quality"
- "What I look for"
- "When I use this"

This frames the skill as guidance for Claude's thinking.

### Be Direct and Declarative

Good: "This provides thinking frameworks."
Avoid: "This provides thinking frameworks, not automated tools."

Make positive statements about what the skill is.
Avoid defining by contrast or comparison.

### Keep Sentences Clear

Avoid unnecessary commas that join multiple ideas.
Break complex thoughts into separate sentences.

Good:
```
This skill helps Claude assess code quality.
It provides systematic frameworks for evaluation.
```

Less good:
```
This skill helps Claude assess code quality, providing
systematic frameworks for evaluation.
```

### Show, Don't Tell

Prefer concrete examples over abstract descriptions.

Good:
```
When reviewing architecture, I ask:
- How are components coupled?
- Where are the boundaries?
- What depends on what?
```

Less good:
```
When reviewing architecture, I consider coupling, boundaries,
and dependencies.
```

## Common Patterns

### Decision Frameworks

For skills that help Claude make decisions:

1. Frame the decision clearly
2. Identify relevant dimensions
3. Evaluate trade-offs
4. Consider constraints
5. Check alignment with goals

Example: `weigh-options` from cognitive-skills

### Exploration Frameworks

For skills that help Claude explore:

1. Define starting point
2. Generate branches or options
3. Follow promising threads
4. Check for completeness
5. Synthesize findings

Example: `wonder` from cognitive-skills

### Evaluation Frameworks

For skills that help Claude assess:

1. Define evaluation criteria
2. Gather evidence
3. Apply standards
4. Identify gaps or issues
5. Formulate judgment

Example: `evidence-check` from cognitive-skills

### Communication Frameworks

For skills that help Claude express ideas:

1. Clarify intent
2. Structure content
3. Match precision to purpose
4. Check understanding
5. Refine expression

Example: `intention-clarification` from communication

## Testing Your Skill

Before submitting, test your skill:

### Clarity Test

Can someone unfamiliar with your thinking understand how to apply this skill from your instructions alone?

### Concreteness Test

Do your examples show the actual thinking process or just describe outcomes?

### Variation Test

Do your examples demonstrate how the skill adapts across different contexts?

### Scope Test

Is it clear what this skill does and doesn't cover?

### Composability Test

Can this skill work alongside other skills without conflict?

## Examples of Well-Written Skills

Study these skills from the cognitive-skills plugin as examples:

- `decompose`: Clear framework for breaking down complexity
- `evidence-check`: Systematic evaluation approach
- `first-principles`: Teaches fundamental reasoning pattern
- `weigh-options`: Structured decision-making framework

Notice how they:
- Provide clear frameworks
- Include rich concrete examples
- Show thinking processes
- Adapt across contexts
- Compose well with other skills

## Getting Feedback

If you're unsure whether your skill meets these standards:

1. Draft your skill following the template
2. Test it with realistic scenarios
3. Ask for feedback before finalizing
4. Iterate based on input
5. Refine until it meets quality standards

Well-written skills make Claude genuinely more useful. Take the time to craft them thoughtfully.
