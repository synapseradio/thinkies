# Thinkies Marketplace Transformation

**Date**: 2025-01-21
**Status**: Approved

## Overview

Transform the thinkies repository from a single plugin into a marketplace/collection of Claude Code utilities that help Claude work better with users. Root everything in the philosophy of practical sincerity.

## Philosophy: Practical Sincerity

The core principle guiding all thinkies utilities:

**Practical over performative**: Focus on usefulness and truth-seeking rather than impressive-sounding output.

**Teaching approach**: Skills show Claude how to think, not what to conclude. They provide frameworks and questions rather than prescriptions and answers.

**Transparency**: Make reasoning processes visible. Acknowledge what is known versus assumed.

**Sincerity**: Acknowledge uncertainty and limitations honestly. Value truth over confidence.

## Architecture

### Layered Marketplace Structure

The repository will be organized into three layers:

**Layer 1: Plugins**
Individual plugins that provide collections of related skills. Each plugin focuses on a specific capability domain.

**Layer 2: Slash Commands**
User-invokable commands that trigger Claude to use specific skills systematically.

**Layer 3: Templates**
Reusable templates and contribution guidelines that enable community additions.

### Repository Structure

```
thinkies/
├── README.md                    # Overview and philosophy
├── marketplace.json             # Plugin registry
├── docs/
│   ├── philosophy.md           # Practical sincerity manifesto
│   ├── contribution-guide.md   # How to create thinkies-worthy utilities
│   ├── skill-writing-guide.md  # Patterns for writing skills
│   └── templates/
│       ├── plugin-template/    # Starter for new plugins
│       ├── skill-template.md   # Starter for new skills
│       └── command-template.md # Starter for slash commands
├── plugins/
│   ├── cognitive-skills/       # Existing 48 thinking skills
│   ├── code-quality/           # New: code assessment frameworks
│   ├── communication/          # New: expression and clarity
│   └── research-learning/      # New: understanding unfamiliar territory
└── commands/
    ├── review-quality.md       # /review-quality command
    ├── explain-concept.md      # /explain-concept command
    └── explore-unknown.md      # /explore-unknown command
```

## Initial Plugin Collection

### 1. Cognitive Skills Plugin

The existing 48 thinking skills reorganized as the first plugin in the marketplace.

**Status**: Existing content
**Action**: Reorganize into plugin structure and update documentation to reflect "tools for Claude" perspective

**Categories**:
- Exploration (7 skills)
- Analysis (8 skills)
- Creativity (6 skills)
- Synthesis (5 skills)
- Metacognitive (6 skills)
- Decision (5 skills)
- Dialogue (4 skills)
- Techniques (7 skills)

### 2. Code Quality Plugin

Guides Claude in assessing and discussing code health systematically.

**Skills**:

**architecture-review**
- Framework for evaluating system design
- Questions to ask about coupling and cohesion and boundaries
- Trade-off dimensions: performance vs maintainability and flexibility vs simplicity
- Pattern recognition: microservices vs monolith and sync vs async and SQL vs NoSQL
- Use cases: Before discussing refactoring or during design reviews or when performance issues emerge

**tech-debt-assessment**
- How to systematically evaluate technical debt
- Distinguishing debt from alternative choices
- Quantifying impact on velocity and bug rate and onboarding time
- Prioritizing based on blocking vs annoying
- What to look for: untested code and unclear abstractions and brittle dependencies
- Use cases: Sprint planning conversations or refactor vs rewrite discussions

**abstraction-review**
- Evaluating if abstractions help or hurt
- Detecting premature abstraction
- Detecting painful duplication
- Detecting leaky abstraction
- Guiding decisions about extracting vs inlining
- Use cases: Code review or discussing pain from duplication or rigidity

### 3. Communication Plugin

Helps Claude translate thought into clear expression.

**Skills**:

**intention-clarification**
- Getting clear on what to achieve before responding
- What change to create in user understanding
- What user should believe or do differently
- Minimum necessary to achieve change
- Use cases: Before writing responses or revising unclear drafts or when stuck starting

**structure-discovery**
- Finding natural structure of ideas to explain
- Identifying core insight
- Mapping concept dependencies
- Distinguishing essential from ornamental
- Determining optimal order for revealing understanding
- Use cases: Organizing complex explanations or outlining responses or untangling messy drafts

**precision-calibration**
- Matching precision to conversational purpose
- When vagueness serves early exploration
- When precision matters for commitments or accuracy
- How specific is specific enough
- Consequences of too vague or too precise
- Use cases: Editing responses or making proposals or giving feedback

**inference-mapping**
- Understanding what Claude asks user to infer
- What remains implicit in responses
- What cognitive burden placed on user
- Where to be more explicit
- What context provides implicitly
- Use cases: Making arguments or writing about unfamiliar topics or reducing confusion

### 4. Research and Learning Plugin

Guides Claude in building understanding of unfamiliar territory.

**Skills**:

**mental-model-building**
- Constructing understanding of complex systems
- Mapping key entities and relationships
- Identifying boundaries and interfaces
- Finding helpful patterns or metaphors
- Making testable predictions
- Use cases: Learning new codebases or technologies or domains

**uncertainty-navigation**
- Working productively with incomplete understanding
- Distinguishing certainty from assumption
- Identifying gaps that matter most
- Knowing what to safely ignore
- Testing assumptions quickly
- Use cases: Starting in unfamiliar code or debugging mysteries or evaluating new tools

**question-formulation**
- Generating questions that reveal understanding
- What would falsify current theory
- What edge cases test understanding
- What analogies help or mislead
- What questions deepen understanding
- Use cases: Code review or debugging or learning

**knowledge-integration**
- Connecting new information to existing understanding
- How this relates to what already known
- What mental models need updating
- What contradictions reveal gaps
- What new capabilities this knowledge enables
- Use cases: After reading docs or exploring code or learning from conversations

## Slash Commands

**`/review-quality`**
Triggers Claude to use code-quality skills systematically for comprehensive code health assessment.

**`/explain-concept`**
Triggers Claude to use communication skills when user needs clear explanation.

**`/explore-unknown`**
Triggers Claude to use research-learning skills systematically when exploring unfamiliar territory.

## Templates

### Plugin Template Structure

```
plugins/plugin-name/
├── plugin.json           # Metadata and skill registry
├── README.md            # Plugin overview and philosophy
└── skills/
    └── skill-name/
        └── SKILL.md     # Skill implementation
```

### Skill Template Structure

Every SKILL.md follows this format:

```markdown
---
name: skill-name
description: What this skill helps Claude do and when to use it
---

# Skill Name

Brief overview of what this skill teaches Claude.

## Instructions

How Claude applies this skill:

1. **First step**: What to do and why
   - Specific actions
   - Questions to ask
   - What to look for

2. **Second step**: Next action
   - More specific guidance
   - Decision points
   - What signals to watch for

## Examples

### Example 1: Specific scenario
Concrete demonstration of using this skill in context.
Shows thinking process and outcome.

### Example 2: Different scenario
Another realistic application showing variation.

## When to use this skill

- Trigger condition 1
- Trigger condition 2
- Situation type where this applies
```

### Slash Command Template

```markdown
---
name: command-name
description: What this command helps user request from Claude
---

# /command-name

When you invoke this command, it triggers Claude to:
1. Use skill X systematically
2. Apply framework Y
3. Produce output Z

This helps Claude give more consistent and thorough responses for this type of request.
```

## Documentation

### philosophy.md

Articulates the core principles:
- Practical over performative: Focus on usefulness and truth-seeking
- Teaching approach: Skills show how to think, not what to conclude
- Transparency: Make reasoning processes visible
- Sincerity: Acknowledge uncertainty and limitations honestly

### contribution-guide.md

Guidelines for creating new utilities:
- Help Claude work better with users
- Teach systematic approaches to common tasks
- Include concrete examples of application
- Follow established template structure

### skill-writing-guide.md

Writing patterns and best practices:
- Structure: frontmatter, instructions, examples, when-to-use
- Writing style: direct sentences, declarative statements, no commas for comments
- Example quality: concrete and realistic
- Teaching approach: show how to think, not what to do

## Implementation Approach

### Phase 1: Foundation
1. Create directory structure
2. Write philosophy and contribution documentation
3. Create templates
4. Update marketplace.json

### Phase 2: Reorganize Existing
1. Move cognitive-skills into plugins/ directory
2. Update plugin.json structure
3. Maintain all existing skills unchanged

### Phase 3: New Plugins
1. Create code-quality plugin with three skills
2. Create communication plugin with four skills
3. Create research-learning plugin with four skills

### Phase 4: Slash Commands
1. Implement /review-quality command
2. Implement /explain-concept command
3. Implement /explore-unknown command

### Phase 5: Polish
1. Update main README with new structure
2. Verify all links and references
3. Test plugin loading in Claude Code

## Success Criteria

- Repository restructured into marketplace format
- Four plugins available: cognitive-skills, code-quality, communication, research-learning
- Three slash commands working
- Complete templates and documentation
- Philosophy clearly articulated
- All existing cognitive skills preserved and functional
