---
name: decompose
description: Break complex problems into manageable components for systematic analysis, useful for large projects, complex systems, or any situation that benefits from structural division
---

# Decompose

Break complex problems into smaller, manageable pieces that can be understood and solved independently.

## Instructions

When decomposing:

1. **Define the whole and why it needs decomposition** - State the problem completely, identifying what makes it feel overwhelming or too complex to grasp as a single unit.

2. **Find natural boundaries using multiple lenses** - Create components by examining what different functions it performs, what sequence things happen in (temporal), where activities occur (spatial), what concepts are logically independent, or what matters most versus least (risk-based). Each component should be understandable alone with minimal dependencies, aiming for 3-7 components per level.

3. **Verify completeness and connections** - Check that components cover everything without gaps or unwanted overlaps, and ensure you can explain how the pieces connect together to form the whole.

4. **Recurse into complex components and map dependencies** - Take any component still too complex and break it down further until pieces are manageable, while mapping which components depend on others.

5. **Identify starting points and sequencing** - Determine which component is most critical, what constitutes the minimum viable subset, and what work can proceed in parallel versus what must happen sequentially.

## Examples

### Emergency response protocol

"**Complex problem**: Hospital needs coordinated response plan for mass casualty events

**Functional decomposition**:
- Triage and patient assessment
- Resource allocation and staffing
- Communication with external agencies
- Supply chain and equipment management
- Family notification and support
- Documentation and legal compliance

**Temporal decomposition**:
- Alert phase (0-15 minutes): Activate staff, prepare spaces
- Intake phase (15-60 minutes): Receive patients, initial triage
- Stabilization phase (1-6 hours): Treat critical cases, transfer patients
- Recovery phase (6+ hours): Return to normal operations, debrief

**Risk-based prioritization**:
- Life-threatening: Airway, bleeding control, shock
- Urgent: Fractures, moderate injuries
- Delayed: Minor injuries, walking wounded
- Expectant: Survivability assessment

**Dependency mapping**:
- Communication system must work before coordinating anything else
- Triage determines resource needs
- Staffing affects all other functions
- Documentation happens throughout but can't block treatment

**Starting point**: Test communication systems first, train triage teams, establish supply staging areas as minimum viable protocol

**Key insight**: Temporal and functional views together reveal that communication infrastructure enables everything else, while risk-based view ensures resources go to highest impact."

### Career transition planning

"**Complex problem**: Switching from teaching to corporate training requires multiple simultaneous changes

**Functional decomposition**:
- Skill development (instructional design, corporate tools)
- Network building (industry connections, informational interviews)
- Financial management (savings buffer, income transition)
- Portfolio creation (work samples, case studies)
- Job search execution (applications, interviews)

**Temporal decomposition**:
- Foundation (months 1-3): Build savings, start skill courses
- Development (months 4-6): Complete certifications, create portfolio pieces
- Networking (months 4-9): Attend conferences, join professional groups
- Active search (months 7-12): Apply to roles, interview, negotiate
- Transition (month 12+): Gradual or immediate switch

**Logical independence**:
- Skill building and networking can proceed in parallel
- Financial buffer is independent but enables risk-taking
- Portfolio creation requires some skills first
- Job search requires network and portfolio ready

**Risk-based focus**:
- Financial runway (determines how long you can search)
- Transferable skills (determines role level you can target)
- Network strength (determines opportunity access)
- Portfolio quality (determines competitive positioning)

**Key insight**: Financial buffer determines timeline for everything else, while skill development and networking can happen simultaneously to accelerate the transition."

### Policy implementation analysis

"**Complex problem**: City implementing new recycling program across diverse neighborhoods

**Spatial decomposition**:
- High-density apartments
- Single-family residential
- Commercial districts
- Industrial areas
- Rural outskirts

**Functional decomposition**:
- Collection logistics and scheduling
- Public education and outreach
- Infrastructure (bins, trucks, processing)
- Compliance monitoring and enforcement
- Contamination management
- Performance metrics and reporting

**Temporal decomposition**:
- Planning (months 1-6): Route design, procurement, stakeholder input
- Pilot (months 7-9): Test in one neighborhood type
- Rollout (months 10-18): Phased expansion across zones
- Optimization (months 19-24): Adjust based on participation data
- Maintenance (ongoing): Sustained operations

**Dependency mapping**:
- Infrastructure procurement must complete before collection starts
- Education should precede rollout by 4-6 weeks
- Pilot results inform rollout adjustments
- Metrics guide optimization decisions

**Starting point**: Pilot in high-density area first (highest volume, easiest logistics), measure participation and contamination rates, refine education approach before expanding

**Key insight**: Spatial decomposition reveals that different neighborhood types need different strategies, while pilot-first approach reduces risk of system-wide failures."

## When to use this skill

- When you notice yourself feeling overwhelmed by a problem's complexity and unsure where to start
- Before explaining a complex system to the user, to structure your explanation around clear components
- When you find yourself trying to solve everything at once instead of identifying manageable pieces
- Before estimating effort or timelines, to ensure you've accounted for all components and dependencies
- When planning implementation work, to identify what can proceed in parallel versus what must be sequential
- Before delegating or distributing work, to create clear boundaries between components
- When debugging complex issues where the problem space feels too large to reason about effectively
- Before writing documentation for complex systems, to organize information around natural component boundaries

## Related Skills

**root-cause** - For drilling down to fundamental causes through iterative "why" questioning. Use root-cause when you need to find why problems happen or understand causal chains. decompose focuses on breaking things into structural components and understanding organization, while root-cause focuses on drilling through layers of causation to reach fundamental explanations.