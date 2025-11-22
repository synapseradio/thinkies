---
name: codebase-cartography
description: Map unfamiliar codebases by identifying landmarks, boundaries, and flows to build a navigable mental model
---

# Codebase Cartography

Build a mental map of unfamiliar code by systematically identifying structure, flows, and patterns.

## Instructions

When I need to understand an unfamiliar codebase, I map it like territory by establishing landmarks and tracing the paths between them.

1. **Find entry points** - I locate where execution begins, whether that's a main function, server bootstrap, API routes, or CLI commands, as these serve as fixed landmarks I can always return to.

2. **Identify major territories** - I examine top-level directories and modules to understand what each area handles, using names and structure to build a rough map of responsibilities like authentication, data access, UI, or external integrations.

3. **Trace representative flows** - I pick one important operation and follow it completely through the system from entry to exit, noting which territories it crosses and in what sequence to establish the primary navigation paths.

4. **Map boundaries and interfaces** - I identify where major components connect to each other, observing what data or calls cross these boundaries and whether the boundaries are clean or tangled, which reveals the intended architecture.

5. **Recognize patterns and conventions** - I look for repeated structures in how similar things are organized, noting naming patterns and framework conventions that let me predict where to find things rather than searching blindly.

6. **Note the exceptional** - I mark anything that doesn't fit the established patterns, including legacy code, workarounds, or complex sections, as these exceptions are important landmarks that signal areas requiring extra care.

7. **Validate the mental model** - I test whether I can explain the system's shape to someone else and predict where new features would go, ensuring my map actually guides navigation rather than just documenting what I've seen.

## Examples

### Mapping a web API service

I'm exploring a Node.js API I haven't worked with before. I start at `src/index.ts` where the server bootstraps, then examine the `src/routes/` directory to see the available endpoints. I trace a login request from its route definition through `AuthService.login()` to `UserModel.findByEmail()` and back, which reveals a clean three-layer architecture: routes handle HTTP concerns, services contain business logic, and models manage data access. I notice all routes follow the same pattern of extracting parameters, calling a service, and returning JSON, while services validate input and return results or throw errors. The exception is `services/legacy-migration.ts` which breaks the pattern by querying the database directly, marking it as an area I should be careful with. Now I can predict that adding a feature means defining a route, implementing service logic, and adding model methods if needed.

### Mapping a React frontend

I examine a large React application starting from `src/App.tsx` to understand the routing structure, then explore how pages compose components and manage state. Tracing how product details are displayed, I see the page uses a `useProduct(id)` hook which calls `ProductService.getById()` which stores data in Redux. I recognize the pattern that pages orchestrate but don't implement logic, components are presentational, services handle API communication, and Redux provides centralized state. I note that `components/Dashboard/` has inline API calls unlike the rest of the codebase, marking it as legacy code predating the service layer. This map tells me that to add a feature, I create a page component, extract API logic into a service, manage state with hooks or Redux, and compose existing components.

### Mapping a data pipeline

I'm working with a Python data processing system and discover it uses Airflow for orchestration by examining `main.py` and finding DAG definitions in `pipelines/`. Tracing the daily user data processing, I follow how the DAG orchestrates extract, transform, and load tasks using connectors for I/O and processors for business logic. The pattern is clear: DAGs define what and when, processors contain pure transformation functions, and connectors abstract external system interactions. I find that `processors/legacy_reports.py` violates this by writing directly to the database instead of using a connector, which I mark as technical debt. Now I understand that adding a pipeline means defining a DAG to orchestrate tasks, implementing processors for logic, and using connectors for I/O.

## When to use this skill

- I catch myself making claims about code organization or architecture without having examined the actual structure
- I'm about to answer questions about "where things are" or "how the system is organized" based on assumptions rather than observation
- I notice I'm using tools (Grep, Glob, Read) reactively to find specific files rather than proactively to understand the system
- I'm forming opinions about how code should be changed before I've mapped what currently exists and why
- I find myself reaching for patterns from my training data instead of discovering the actual patterns in this specific codebase
- I'm about to estimate impact, propose changes, or suggest refactoring without having traced how components actually connect
- I realize I cannot explain the codebase structure to someone else with specifics, only generalities

## Related Skills

- `trace-flow` - Follow specific execution paths in detail after establishing the initial map
- `dependency-graph` - Analyze coupling and dependencies once I understand the basic structure
- `blast-radius` - Use the mental map to predict impact of proposed changes
- `complexity-surface` - Identify areas of high complexity while mapping the codebase
