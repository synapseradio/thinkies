---
name: blast-radius
description: Map impact radius of code changes by systematically tracing dependencies, callers, and type propagation to understand what breaks when you change something
---

# Blast Radius

Understand the full scope of what a code change affects before proposing or implementing it.

## Instructions

When I propose changing code, I systematically map everything that depends on it to avoid breaking changes and missing affected areas.

1. **Identify the change target** - I pinpoint exactly what I'm proposing to modify, whether it's a function signature, type definition, component interface, or exported value, because vague change descriptions lead to incomplete impact analysis.

2. **Analyze direct dependencies** - I use `analyze_impact` to get the complete dependency graph showing what calls this code, what uses it as a type, and what composes it, establishing the immediate blast radius with confidence that AST analysis catches structural relationships.

3. **Find all callers** - I use `find_callers` to discover every function that invokes the target, which reveals runtime dependencies and helps me understand usage patterns that might constrain how I can safely change the code.

4. **Search for indirect references** - I use grep to find string-based references like dynamic imports, configuration files, documentation, and comments that mention the target, since these won't appear in AST analysis but still represent coupling that makes changes risky.

5. **Trace type propagation** - I examine what uses the target as a type parameter, return type, or property type, following the chain of type dependencies to find distant code that will fail type checking if I change the signature, even if it never calls the code directly.

6. **Check test coverage** - I search for tests that reference the target to understand what behavior is explicitly verified and what changes would require test updates, using test files as documentation of expected behavior that must be preserved or consciously changed.

7. **Validate with the type checker** - I mentally simulate the proposed change and predict what type errors would emerge, or actually make the change in a hypothetical scenario to see what breaks, turning the compiler into a tool for discovering hidden dependencies.

8. **Document the radius** - I summarize the complete impact with confidence levels, distinguishing between certain effects I've verified through tools, likely effects based on patterns, and possible effects I should manually check, so the user understands both what will definitely break and what might break.

## Examples

### Changing a service function signature

I'm proposing to change `UserService.findById(id: string)` to accept an options object instead. I use `analyze_impact` on the `findById` symbol and discover it's called in 12 locations across 8 files. Running `find_callers` shows these are in route handlers, middleware, and other services. I grep for "findById" and find it's also mentioned in API documentation and a migration script. Examining the callers, I see some pass the result to functions expecting a `User | null` return type, which means changing the return type would cascade. I search tests and find 15 test cases that call this function with just an ID. The blast radius is: 12 call sites need updates, 15 tests need changes, 1 documentation file needs revision, and 1 migration script should be reviewed. I note high confidence in the call sites (verified by AST), medium confidence in type propagation (requires examining each caller), and low confidence the migration script actually needs changes (depends on whether it's still used).

### Renaming a React component

I want to rename `UserCard` to `ProfileCard` to better reflect its purpose. I use `find_symbol` to locate the component definition, then `analyze_impact` to see it's rendered in 6 parent components and imported in 8 files. Using grep for "UserCard", I find references in Storybook stories, CSS module filenames (`UserCard.module.css`), test files using `getByTestId('user-card')`, and a comment explaining why this component exists. I also find it's exported from an index file that re-exports many components. The blast radius includes: 8 import statements, 6 JSX usages, 3 test files with test IDs and component references, 2 Storybook files, 1 CSS module filename, 1 barrel export, and 1 comment. I recognize that just renaming the component file will break imports, CSS module references, and make tests fail on test IDs, so I need to coordinate changes across multiple file types, not just TypeScript files.

### Modifying a shared type definition

I'm considering adding a required field to the `ApiResponse<T>` interface that's used throughout the codebase. I use `analyze_impact` and discover this type is used in 45 locations as a return type, type parameter, or property type. I examine a sample of usages and see functions that construct this type, functions that consume it, and functions that just pass it through. Using grep, I find the type is also referenced in OpenAPI schema definitions and technical documentation. I trace type propagation and realize that adding a required field means every location that constructs an `ApiResponse` must provide the new field, but locations that only consume it are unaffected. Checking tests, I find mock factories that create `ApiResponse` objects for testing. The blast radius has three severity levels: critical impact on approximately 15 constructor sites that must be updated immediately or code won't compile, moderate impact on 8 test factories that need the new field, and documentation impact on API specs and docs. I conclude this change requires a migration strategy, possibly making the field optional initially, rather than adding it as required all at once.

## When to use this skill

- I'm about to propose changes to code without having analyzed what depends on it
- I catch myself suggesting refactoring, renaming, or signature changes based on local code inspection alone
- I'm answering "this should be safe to change" without having actually checked callers and dependencies
- I notice I'm making assumptions about usage patterns rather than verifying them with tools
- I'm about to modify exported functions, public APIs, shared types, or reusable components
- I find myself saying "just update the callers" without knowing how many callers exist or where they are
- I'm proposing breaking changes without quantifying what breaks or estimating migration effort
- I realize I cannot list specific files and locations that will be affected by a proposed change

## Related Skills

- `dependency-graph` - Understand overall coupling patterns before analyzing specific change impact
- `codebase-cartography` - Build mental model of system structure that informs impact prediction
- `trace-flow` - Follow execution paths that cross the code I'm changing to understand runtime effects
- `migration-path` - Design safe change strategy once I've mapped the blast radius
