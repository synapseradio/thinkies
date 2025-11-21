# Code Quality Plugin

Skills that guide Claude in assessing and discussing code health systematically.

## Overview

This plugin provides Claude with frameworks for evaluating design decisions and code quality. It focuses on systematic assessment rather than automated linting.

These skills help Claude:
- Evaluate architecture decisions objectively
- Assess technical debt systematically
- Review abstractions fairly

## Skills

### architecture-review

Framework for how Claude evaluates system design decisions.

Guides Claude through questions about coupling, cohesion, and boundaries. Helps analyze trade-offs between performance and maintainability and flexibility and simplicity.

**When Claude uses this**: Before discussing refactoring or during design review conversations or when performance issues emerge.

### tech-debt-assessment

How Claude systematically evaluates technical debt.

Helps Claude distinguish debt from alternative choices and quantify impact on velocity. Guides prioritization based on whether debt blocks work or just annoys.

**When Claude uses this**: During sprint planning conversations or refactor vs rewrite discussions.

### abstraction-review

How Claude evaluates if abstractions help or hurt.

Guides Claude in detecting premature abstraction, painful duplication, and leaky abstractions. Helps make decisions about extracting functions versus inlining.

**When Claude uses this**: During code review or when discussing pain from duplication or rigid abstractions.

## Philosophy

This plugin embodies practical sincerity by:
- Providing systematic frameworks over subjective opinions
- Teaching evaluation methods rather than prescribing answers
- Making assessment criteria transparent
- Acknowledging trade-offs honestly

## Examples

### Evaluating an Architecture Decision

User asks: "Should we use microservices or keep the monolith?"

Claude applies `architecture-review` to systematically evaluate:
- Coupling and scaling needs
- Team size and operational capabilities
- Trade-offs between complexity and flexibility
- Current constraints vs future needs

### Assessing Technical Debt

User mentions: "We have a lot of untested code"

Claude uses `tech-debt-assessment` to:
- Distinguish between debt and intentional choices
- Quantify impact on development velocity
- Prioritize which debt to address first
- Weigh refactor vs rewrite trade-offs

### Reviewing Abstractions

User says: "This code feels too complex"

Claude applies `abstraction-review` to:
- Identify if abstraction is premature or appropriate
- Check if abstractions are at the right level
- Evaluate if duplication would be simpler
- Guide extraction or inlining decisions

## Version

Current version: 1.0.0

## Author

Created by Nick
