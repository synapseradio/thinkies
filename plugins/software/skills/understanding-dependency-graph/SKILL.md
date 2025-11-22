---
name: dependency-graph
description: Map coupling, boundaries, and architectural layers by systematically analyzing what depends on what
---

# Dependency Graph

Understand the structure of coupling in a codebase by mapping dependencies between modules, revealing architectural layers and boundaries.

## Instructions

When I need to understand how components depend on each other, I build a dependency graph that reveals coupling patterns, architectural layers, and change propagation paths.

1. **Start with imports and requires** - I use Grep to find import statements and require calls to identify the surface-level dependencies, noting what each module explicitly declares it needs, as these form the compile-time dependency skeleton of the system.

2. **Map the call graph** - I use Codanna's `find_callers` and `get_calls` tools to trace runtime dependencies, discovering not just what a module imports but what functions it actually invokes and what functions invoke it, revealing the dynamic coupling that matters when code executes.

3. **Analyze dependency direction** - I examine whether dependencies flow in one direction or create cycles, checking if lower-level modules depend on higher-level ones or vice versa, because unidirectional flow indicates clean layering while circular dependencies signal architectural debt that makes change difficult.

4. **Measure coupling density** - I count how many modules depend on each component versus how many dependencies it has, using Codanna's `analyze_impact` to understand whether something is a central hub with many dependents or a peripheral leaf with few connections, which tells me where change will ripple and where it stays contained.

5. **Identify architectural boundaries** - I look for clusters of tightly coupled modules separated by sparse connections, recognizing that true architectural boundaries have few dependencies crossing them while false boundaries leak dependencies across what should be isolated concerns.

6. **Distinguish dependency types** - I differentiate between direct dependencies and transitive ones, between compile-time imports and runtime instantiation, and between code dependencies and data dependencies through shared state, because each type of coupling has different implications for change and testing.

7. **Validate with change scenarios** - I ask "if I modify this module, what needs to recompile, what needs retesting, and what might break at runtime?" using the dependency map to predict impact, ensuring my understanding is actionable rather than merely documentary.

## Examples

### Analyzing a core utility module

I'm examining `utils/formatters.ts` which other developers call "critical" but I want evidence. Using Grep, I find it's imported by 47 files across the codebase. Using Codanna's `find_callers` on `formatCurrency`, I discover 23 different modules invoke it, spanning UI components, API responses, and PDF generation. The dependency graph reveals this is a central hub with many dependents but few dependencies of its own, making it high-impact for changes but relatively easy to test in isolation. When I check `analyze_impact`, I see changes here would affect three architectural layers: presentation, API, and reporting. This isn't opinion about importance, it's measured coupling showing that modifications require careful coordination and comprehensive testing across multiple system boundaries.

### Discovering circular dependencies

I'm investigating why builds are slow and tests are hard to write in a Python service. Using Grep for import statements, I trace that `models/user.py` imports from `services/auth.py` which imports from `models/session.py` which imports back to `models/user.py`, creating a circular dependency. Using Codanna's `get_calls` on each module, I discover the cycle exists at runtime too: `UserModel.validate()` calls `AuthService.checkPermissions()` which calls `SessionModel.getUserId()` which calls back to `UserModel.findById()`. This cycle explains why these modules can't be tested independently and why the build system struggles with import ordering. The dependency graph reveals that the auth service shouldn't be in the middle layer but should either be higher level or split into a pure permission checker that doesn't depend on models.

### Understanding layered architecture through dependencies

I'm working with a web application that claims to follow clean architecture. Using Codanna's `semantic_search_with_context` for "database" and "UI", I identify what should be the data layer and presentation layer. I then use `find_callers` on database modules and discover that UI components never directly call them, all calls route through service modules. Using Grep to map all imports systematically, I verify dependencies flow in one direction: UI depends on services, services depend on domain models, models depend on database adapters, and crucially, nothing in the lower layers imports from higher layers. When I check `analyze_impact` on a database module, the blast radius is contained to data layer concerns. This dependency flow is evidence of genuine layering, not just well-named folders. The architecture isn't claimed, it's demonstrated by dependency direction.

## When to use this skill

- I catch myself claiming code is "tightly coupled" or "loosely coupled" without having mapped actual dependencies
- I'm about to refactor or extract a module without understanding what depends on it or what it depends on
- I notice I'm making assumptions about blast radius before analyzing the dependency graph
- I'm proposing to move or change code without knowing what will need to recompile or retest
- I find myself reasoning about architectural layers based on directory structure rather than actual dependency flow
- I'm about to suggest breaking something apart without measuring how much coupling exists
- I realize I cannot explain which modules are central versus peripheral in the system's dependency structure
- I'm estimating change effort without understanding dependency chains and transitive impact

## Related Skills

- `codebase-cartography` - Establish the basic structure before mapping dependencies
- `trace-flow` - Follow specific execution paths to understand runtime dependencies
- `blast-radius` - Use the dependency graph to predict change impact
- `complexity-surface` - Identify where coupling creates complexity hotspots
