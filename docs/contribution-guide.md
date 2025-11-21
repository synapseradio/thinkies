# Contributing to Thinkies

Thank you for your interest in contributing utilities that help Claude work better with users.

## Before You Start

Read the [philosophy document](philosophy.md) to understand what makes a good thinkie.

Ask yourself:
- Does this help Claude work better with users?
- Does it teach systematic thinking rather than prescribe answers?
- Does it include concrete realistic examples?
- Does it compose well with existing thinkies?
- Is the scope clear and well-defined?

If yes to all, proceed with creating your contribution.

## Types of Contributions

### Adding a Skill to an Existing Plugin

If your skill fits naturally within an existing plugin's scope:

1. Check the plugin's README to understand its purpose
2. Use the [skill template](templates/skill-template.md) as your starting point
3. Write your skill following the [skill writing guide](skill-writing-guide.md)
4. Add your skill to the plugin's `skills/` directory
5. Update the plugin's `plugin.json` to include your skill
6. Update the plugin's README to document your skill

### Creating a New Plugin

If your skills represent a new capability domain:

1. Use the [plugin template](templates/plugin-template/) as your starting point
2. Create your plugin directory under `plugins/`
3. Write your skills using the [skill template](templates/skill-template.md)
4. Create a comprehensive README explaining your plugin's purpose
5. Add your plugin to `marketplace.json`

### Adding a Slash Command

If you want to create a user-invokable command:

1. Use the [command template](templates/command-template.md) as your starting point
2. Identify which skills your command will trigger
3. Document clearly what the command does and when to use it
4. Add your command file to the `commands/` directory

## Quality Standards

All contributions must meet these standards:

### Clear Purpose

- State explicitly what this helps Claude do
- Define when Claude should use it
- Explain what problem it solves

### Systematic Framework

- Provide step-by-step guidance
- Include decision points
- Explain what signals to watch for

### Concrete Examples

- Show realistic scenarios
- Walk through the thinking process
- Demonstrate variation across contexts
- Use examples from actual work situations

### Proper Structure

- Follow the template format exactly
- Use frontmatter for metadata
- Include all required sections
- Match the established writing style

## Writing Style Guidelines

### Use Direct Sentences

Good: "This provides thinking frameworks."
Avoid: "This provides thinking frameworks, not automated tools."

Write declaratively. Avoid defining things by contrast.

### Write for Claude

Use "I" language when describing how Claude uses skills:
- "How I assess code quality"
- "What I look for"
- "When I use this"

### Avoid Unnecessary Commas

Keep sentences clear and direct. Break complex ideas into multiple simple sentences instead of using commas to join them.

### Be Concrete

Prefer specific examples over abstract descriptions.
Show the application rather than just describing it.

## Submission Process

1. Fork the thinkies repository
2. Create a branch for your contribution
3. Add your skill, plugin, or command
4. Test that it loads correctly in Claude Code
5. Submit a pull request with:
   - Clear description of what you're adding
   - Why it belongs in thinkies
   - Examples of how Claude will use it

## Review Criteria

Your contribution will be evaluated on:

### Alignment with Philosophy

- Does it embody practical sincerity?
- Does it teach rather than prescribe?
- Does it promote transparency and honest

ness?

### Quality of Examples

- Are examples realistic and concrete?
- Do they demonstrate the thinking process?
- Do they show variation across contexts?

### Clarity of Writing

- Is the purpose immediately clear?
- Are instructions actionable?
- Is the structure easy to follow?

### Scope and Composability

- Is the scope well-defined?
- Does it overlap unnecessarily with existing utilities?
- Does it work well alongside other thinkies?

## Getting Help

If you're unsure whether your idea fits or how to implement it:

1. Open an issue describing your proposed contribution
2. Explain what problem it solves
3. Share draft examples of how it would work
4. Get feedback before investing time in full implementation

We're happy to help refine ideas and provide guidance on implementation.

## License

By contributing to thinkies, you agree that your contributions will be licensed under the same license as the project.
