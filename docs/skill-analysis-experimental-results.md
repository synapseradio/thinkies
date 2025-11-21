# Thinkies Skills: Experimental Analysis Results

**Objective**: Determine which skills produce genuinely distinct reasoning patterns in AI agents vs which are functionally redundant.

**Methodology**: Run the same problem through different skills using separate agents, compare outputs for distinctness.

**Test Problem**: "A software team's code reviews are taking too long and blocking deployments."

---

## Experiment 1: Divergent Thinking - `branch` vs `alternatives`

### Hypothesis
These might be redundant since both generate multiple options.

### Results

**`branch` output**:
- **Type**: Solution generation
- **Count**: 5 distinct solution paths
- **Nature**: Action-oriented (what to do)
- **Examples**: Process Optimization, Parallel Approval, Capacity Redistribution, Architectural Decoupling, Risk-Based Triage
- **Reasoning mode**: Divergent, forward-looking, solution-focused

**`alternatives` output**:
- **Type**: Cause analysis
- **Count**: 10 competing explanations
- **Nature**: Diagnostic (why it's happening)
- **Examples**: Reviewer load imbalance, PR size problem, unclear standards, deployment coupling, timezone issues, incentive misalignment
- **Reasoning mode**: Analytical, backward-looking, cause-focused

### Analysis
- **Overlap**: ~10% (both are divergent but at different problem-solving stages)
- **Key Distinction**: branch = "what solutions?" vs alternatives = "what causes?"
- **Output Quality**: Both produced valuable, non-overlapping insights
- **Functional Difference**: HIGHLY DISTINCT

### Verdict
✅ **KEEP BOTH SEPARATE**

**Reasoning**: These operate at different stages of problem-solving. You need alternatives to understand the problem, then branch to explore solutions. Fundamentally different cognitive operations.

---

## Experiment 2: Pattern Recognition - `connect-dots` vs `theme-find`

### Hypothesis
These might overlap significantly since both find patterns.

### Results

**`connect-dots` output**:
- **Type**: Relationship mapping
- **Approach**: Systems analysis with concrete connections
- **Key outputs**:
  - Identified hubs (Reviewer Availability, Review Necessity, Process Design)
  - Applied queuing theory and Conway's Law
  - Found feedback loops (deployment urgency → rushed reviews → bugs)
- **Abstraction level**: Concrete, mechanistic
- **Conclusion**: "Capacity planning and process design problem"

**`theme-find` output**:
- **Type**: Conceptual pattern extraction
- **Approach**: Abstract theme identification and hierarchy
- **Key outputs**:
  - Themes: Flow Interruption, Attention Scarcity, Synchronous Coordination, Batch Processing
  - Built hierarchy: Throughput Constraint → manifestations
  - Meta-theme: "Asynchronous Production, Synchronous Verification"
- **Abstraction level**: Abstract, conceptual
- **Conclusion**: "Fundamental architectural mismatch"

### Analysis
- **Overlap**: ~60% (both find patterns but at different levels)
- **Key Distinction**: connect-dots finds concrete system relationships, theme-find finds abstract conceptual patterns
- **Output Quality**: Significant overlap in insights but different framing
- **Functional Difference**: MODERATELY DISTINCT

### Verdict
⚠️ **CONSIDER VARIANTS OR MERGE**

**Options**:
1. Merge into single `pattern-find` with modes (concrete/abstract)
2. Keep both but clarify: connect-dots for system analysis, theme-find for conceptual synthesis
3. Mark as variants of same root skill

**Recommendation**: Keep both but document as variants. Different abstraction levels serve different purposes.

---

## Experiment 3: Analogical Reasoning Cluster

**Skills tested**: `lateral-think`, `domain-transfer`, `random-input`

### Hypothesis
These might be redundant variations of analogical reasoning.

### Results

**`lateral-think` output**:
- **Technique**: Multiple methods (distant connections, provocations, reversals, hidden needs)
- **Structure**: Free-form, assumption-challenging
- **Key insights**:
  - "What if we deployed first?"
  - "Review IS the problem"
  - Questions fundamental assumptions about review gates
- **Character**: Provocative, meta-level, radical
- **Domain sources**: Emergency rooms, restaurants, immune systems, traffic (selected freely)

**`domain-transfer` output**:
- **Technique**: Systematic cross-domain mapping
- **Structure**: Methodical, structured
- **Key insights**:
  - Analyzed 5 domains comprehensively (Airport Security, Restaurant Kitchen, ER Triage, Manufacturing QC, Air Traffic Control)
  - Extracted universal principles
  - Built detailed tiered review system
- **Character**: Comprehensive, systematic, actionable
- **Domain sources**: Selected deliberately for relevance

**`random-input` output**:
- **Technique**: Forced associations from random stimuli
- **Structure**: Spontaneous, playful
- **Key insights**:
  - Laundromat → tiered service levels
  - Beehive → distributed decision-making
  - Restaurant → review expeditor role
- **Character**: Unexpected, tactical, surprising
- **Domain sources**: Truly random (laundromat, beehive, traffic lights)

### Analysis
- **Overlap**: ~40% (all use analogy but access it differently)
- **Key Distinctions**:
  - lateral-think: Broad, provocative, challenges assumptions
  - domain-transfer: Systematic, comprehensive, thorough
  - random-input: Chaotic, unexpected, forces novelty
- **Output Quality**: All valuable, minimal redundancy in actual insights
- **Functional Difference**: MODERATELY DISTINCT

### Verdict
✅ **KEEP ALL THREE SEPARATE**

**Reasoning**: While conceptually similar (analogical reasoning), each provides a distinct creative entry point:
- Use `lateral-think` when you need to challenge fundamental assumptions
- Use `domain-transfer` when you want systematic, thorough cross-domain analysis
- Use `random-input` when you're stuck and need to break out of all patterns

Different prompts activate different creative modes in AI reasoning.

---

## Experiment 4: Metacognitive - `thinking-monitor` vs `cycle-detect`

### Hypothesis
`cycle-detect` might be redundant since it's a specific pattern `thinking-monitor` would catch.

### Test Problem
Different scenario: "You're designing an API for a payment system. You've been thinking about it for an hour and keep coming back to REST vs GraphQL, but you're not making progress on the actual design."

### Results

**`thinking-monitor` output**:
- **Scope**: Comprehensive observation of thinking process
- **What it examined**:
  - Pattern-matching behavior
  - Bias detection (familiarity, recency)
  - Emotional indicators (resistance, displacement)
  - Reasoning quality assessment
  - Mode detection (evaluation vs exploration)
  - Meta-observation (watching myself watch)
- **Depth**: Broad analysis of many thinking aspects
- **Conclusion**: "Stuck due to avoiding harder work (payment domain complexity); debating API style is displacement activity"
- **Character**: Analytical, comprehensive, observational

**`cycle-detect` output**:
- **Scope**: Focused on repetition pattern
- **What it examined**:
  - Specific loop identification (false dichotomy + unresolved dependency)
  - Loop triggers and duration
  - Cycle type categorization
  - Breaking strategies (4 specific options)
  - Learning from the loop
- **Depth**: Narrow but action-oriented
- **Conclusion**: Same root insight but with concrete cycle-breaking strategies
- **Character**: Diagnostic, action-oriented, prescriptive

### Analysis
- **Overlap**: ~70% (both identify the same core problem)
- **Key Distinction**:
  - thinking-monitor is **observational** - "here's what I notice about my thinking"
  - cycle-detect is **interventional** - "here's the loop and how to break it"
- **Output Quality**: Both valuable but cycle-detect more immediately actionable
- **Functional Difference**: MODERATELY DISTINCT (same diagnosis, different focus)

### Unique Value
- **thinking-monitor**: Catches many thinking patterns, not just loops. Better for general metacognition.
- **cycle-detect**: Specifically optimized for recognizing and breaking loops. More focused and actionable for that specific problem.

### Verdict
⚠️ **KEEP AS SPECIALIZED VARIANT**

**Reasoning**: `cycle-detect` is essentially a specialized application of `thinking-monitor` focused specifically on loops. Similar to how `root-cause` is a specialized application of `decompose` focused on iterative "why" drilling.

**Options**:
1. Merge `cycle-detect` into `thinking-monitor` as the loop-specific mode
2. Keep both: `thinking-monitor` as general metacognition, `cycle-detect` as specialized loop-breaker
3. Document cycle-detect as "focused variant of thinking-monitor"

**Recommendation**: Keep both but document relationship. `cycle-detect` is more immediately actionable when you specifically need to break a loop. `thinking-monitor` is better for general metacognitive observation.

---

---

## Experiment 5: Assumption Analysis - `assumption-reveal` vs `socratic`

### Hypothesis
`assumption-reveal` might be redundant since Socratic questioning includes assumption revelation.

### Test Problem
Statement: "We need to migrate to microservices to improve our system's scalability."

### Results

**`assumption-reveal` output**:
- **Method**: Systematic categorization of assumptions
- **Categories used**: Factual, Causal, Value, Capability, Definitional, Contextual
- **Scope**: Laser-focused on uncovering hidden assumptions
- **Count**: ~25 distinct assumptions identified and categorized
- **Depth**: Testing assumption validity, identifying load-bearing assumptions
- **Conclusion**: "Most dangerous assumption: architectural complexity is appropriate response without measurement and profiling"
- **Character**: Systematic, categorical, assumption-focused

**`socratic` output**:
- **Method**: Systematic questioning across multiple dimensions
- **Question types**: Clarification, Probing assumptions, Examining evidence, Exploring implications, Questioning the question
- **Scope**: Broad - assumptions, evidence, reasoning, implications, reframing
- **Assumptions identified**: ~20 (overlap with assumption-reveal)
- **Additional analysis**: Evidence examination, logical reasoning check, implications, alternative framings
- **Conclusion**: "Need to define problem precisely, gather evidence, consider alternatives before choosing solution"
- **Character**: Dialogical, comprehensive, questioning-based

### Analysis
- **Overlap**: ~65% (socratic finds most of the same assumptions)
- **Key Distinction**:
  - assumption-reveal is **specialized** - focused only on assumptions
  - socratic is **comprehensive** - assumptions + evidence + reasoning + implications
- **Output Quality**: assumption-reveal more thorough on assumptions specifically; socratic provides broader analysis
- **Functional Difference**: MODERATELY OVERLAPPING (assumption-reveal is subset of socratic)

### Unique Value
- **assumption-reveal**: More systematic and exhaustive on assumptions specifically. Better categorization framework.
- **socratic**: Broader toolkit that also examines evidence, tests reasoning, explores implications, and reframes questions.

### Verdict
⚠️ **MERGE OR MARK AS SUBSET**

**Reasoning**: `assumption-reveal` is essentially one component of the `socratic` method. The Socratic approach includes assumption revelation but also adds:
- Evidence examination
- Logical reasoning checks
- Implication exploration
- Question reframing

**Options**:
1. Merge into socratic with explicit "assumption mode"
2. Keep assumption-reveal as a lightweight "quick assumptions only" tool
3. Document as "focused subset of socratic method"

**Recommendation**: Lean toward merging. If you specifically want assumptions and nothing else, socratic can be used with that focus. The separate skill might not add enough value to justify the cognitive load.

---

---

## Experiment 6: Exploration Modes - `tree-explore` vs `graph-wander`

### Hypothesis
These might overlap since both explore topics, but could differ in structure (hierarchical vs associative).

### Test Problem
Topic: "How might authentication work in a distributed system?"

### Results

**`tree-explore` output**:
- **Structure**: Hierarchical, systematic branches
- **Method**: Define main branches, explore depth-first, return to root
- **Coverage**: Comprehensive (6 main branches, ~20 sub-branches)
- **Depth control**: Explicit depth markers (DEEP DIVE vs shallow)
- **Navigation**: Deliberate - "Returning to root..." between branches
- **Output**: Complete tree visualization + cross-branch synthesis
- **Key aspects covered**: Mechanisms, Identity Propagation, Authorization, Session Management, Security, Observability
- **Character**: Systematic, complete, organized, methodical

**`graph-wander` output**:
- **Structure**: Associative, following connections
- **Method**: Start with interesting concept, follow natural associations
- **Coverage**: Selective (explored what seemed most interesting/connected)
- **Depth**: Variable - went deep where connections led
- **Navigation**: Emergent - "This makes me think of...", "This connects to..."
- **Output**: Connection map with identified hubs and clusters
- **Key aspects covered**: Trust boundaries, revocation problem, state tradeoffs, time sync, federation, eventual correctness
- **Character**: Exploratory, associative, insight-driven, non-linear

### Analysis
- **Overlap**: ~35% (covered similar topics but approached differently)
- **Key Distinction**:
  - tree-explore: **Comprehensive coverage** - "I want to understand all aspects"
  - graph-wander: **Following connections** - "I want to discover unexpected insights"
- **Exploration strategy**:
  - Tree: Breadth-first with controlled depth
  - Graph: Interest-driven, associative jumps
- **Output Quality**: Tree provides completeness, Graph provides surprising connections
- **Functional Difference**: HIGHLY DISTINCT

### Unique Value
- **tree-explore**: When you need systematic coverage of a topic. Best for learning, planning, comprehensive understanding.
- **graph-wander**: When you want creative insights and unexpected connections. Best for discovering non-obvious patterns, breaking out of structured thinking.

### Verdict
✅ **KEEP BOTH SEPARATE**

**Reasoning**: These are fundamentally different exploration philosophies:
- Tree = systematic completeness
- Graph = creative discovery

**Use cases**:
- Use `tree-explore` when: Learning new domain, planning project, need comprehensive coverage, want to ensure nothing is missed
- Use `graph-wander` when: Stuck in conventional thinking, looking for creative angles, exploring complex interconnections, discovering non-obvious patterns

Both are valuable for different cognitive purposes. The tree-explore output was more structured and complete, while graph-wander surfaced surprising connections (Byzantine Generals, medieval messengers, immune systems) that tree-explore wouldn't naturally reach.

---

---

## Experiments 11-15: Phase 2 Testing (High Priority)

### Experiment 11: `first-principles` vs `socratic`
- **Test Problem**: "We should migrate our monolithic application to microservices to improve scalability and team velocity"
- **Overlap**: ~60% | **Verdict**: Keep both separate
- **first-principles**: Strips to axioms, rebuilds from fundamentals, generates alternative approaches
- **socratic**: Systematic questioning, examines reasoning, reveals assumptions through dialog
- **Key distinction**: first-principles is GENERATIVE (builds new solutions), socratic is ANALYTICAL (tests existing reasoning)
- **When to use**: first-principles for "what should we build?", socratic for "is this approach sound?"

### Experiment 12: `integrate` vs `connect-dots` vs `theme-find`
- **Test Problem**: Multiple team feedback points about development process challenges
- **Overlaps**: integrate↔connect-dots (75%), integrate↔theme-find (65%), connect-dots↔theme-find (60%)
- **Verdict**: Keep all three separate
- **integrate**: Reconciles tensions, produces unified frameworks, addresses contradictions
- **connect-dots**: Maps causal mechanisms, builds system models, traces "how A influences B"
- **theme-find**: Names recurring patterns, creates hierarchies, identifies "what keeps coming up"
- **Key distinction**: COMBINING tensions vs MAPPING relationships vs CATEGORIZING patterns

### Experiment 13: `scenario-planning` vs `premortem`
- **Test Problem**: Deciding whether to adopt AI pair programming tools across 50-person engineering team
- **Overlap**: ~40-45% | **Verdict**: Keep both separate
- **scenario-planning**: Explores MULTIPLE possible futures, builds adaptive strategies, tests robustness
- **premortem**: Imagines SINGLE specific failure, works backward to causes, identifies preventions
- **Key distinction**: Multiple futures exploration vs single failure diagnosis
- **When to use**: scenario-planning for "should we?", premortem for "what could go wrong?"
- **Complementary**: Use scenario-planning first, then premortem for chosen strategy in each scenario

### Experiment 14: `feynman` vs `socratic`
- **Test Problem**: Explain and validate understanding of async/await in JavaScript
- **Overlap**: ~35-40% | **Verdict**: Keep both separate
- **feynman**: TEACH to learn, explain simply, identify gaps through teaching, build up from simple
- **socratic**: QUESTION to examine, reveal assumptions, test reasoning, dig down from claims
- **Key distinction**: Building up (simple→complete) vs digging down (claim→foundations)
- **When to use**: feynman for "do I truly understand this?", socratic for "does this reasoning hold?"

### Experiment 15: `dialectic` vs `perspective-shift`
- **Test Problem**: "Should we prioritize shipping fast with technical debt, or shipping slowly with quality code?"
- **Overlap**: ~65-70% | **Verdict**: Keep both separate
- **dialectic**: BINARY opposing ideas → synthesis, philosophical/conceptual, transcends contradictions
- **perspective-shift**: MULTIPLE stakeholder viewpoints, empathetic/embodied, understands lived experiences
- **Key distinction**: Idea conflicts vs people conflicts, thesis/antithesis/synthesis vs parallel exploration
- **When to use**: dialectic for conceptual paradoxes, perspective-shift for stakeholder conflicts

---

## Experiments 16-20: Phase 3 Testing (Medium Priority)

### Experiment 16: `evidence-check` vs `socratic`
- **Test Problem**: "We should switch to a four-day work week because studies show it increases productivity"
- **Overlap**: ~70-75% | **Verdict**: Keep both separate
- **evidence-check**: Evaluates THE EVIDENCE (source quality, methodology, directness, recency)
- **socratic**: Examines THE REASONING (assumptions, logical connections, implications)
- **Key distinction**: Analyzing evidence quality vs testing reasoning validity
- **When to use**: evidence-check for "is this evidence reliable?", socratic for "does the logic hold?"
- **Sequential use**: Socratic first (clarify claims), then evidence-check (evaluate support)

### Experiment 17: `fallacy-detect` vs `logic-trace`
- **Test Problem**: Argument about adopting AI customer service with multiple logical flaws
- **Overlap**: ~75% | **Verdict**: Keep both separate
- **fallacy-detect**: PATTERN RECOGNITION for known reasoning errors (names fallacies quickly)
- **logic-trace**: STRUCTURAL VALIDATION of reasoning chains (step-by-step construction)
- **Key distinction**: Like linter (quick error scan) vs code review (deep logic validation)
- **When to use**: fallacy-detect for persuasive arguments/debates, logic-trace for complex technical reasoning
- **Sequential use**: Fallacy-detect first (quick scan), then logic-trace if needed (deep validation)

### Experiment 18: `confidence-calibrate` vs `knowledge-check`
- **Test Problem**: Making technical recommendation to adopt Kubernetes while feeling "pretty confident"
- **Overlap**: ~65-70% | **Verdict**: Keep both separate
- **confidence-calibrate**: Calibrates FEELINGS of certainty to match evidence
- **knowledge-check**: Inventories ACTUAL information gaps and readiness to proceed
- **Key distinction**: "How sure should I feel/sound?" vs "What do I need to know?"
- **When to use**: confidence-calibrate for communication, knowledge-check for planning/research
- **Pipeline positions**: knowledge-check identifies gaps → confidence-calibrate assesses certainty given those gaps

### Experiment 19: `fork-detect` vs `cycle-detect`
- **Test Problem**: Considering build vs buy for feature, thinking for days without progress
- **Overlap**: ~60-70% | **Verdict**: Keep both separate
- **fork-detect**: Identifies SIGNIFICANT DECISION POINTS where paths diverge meaningfully
- **cycle-detect**: Recognizes STUCK LOOPS and repetitive thinking patterns
- **Key distinction**: Preventive (before deciding) vs remedial (after stuck)
- **When to use**: fork-detect when approaching decisions, cycle-detect when already stuck
- **Complementary**: fork-detect prevents cycles, cycle-detect breaks them

### Experiment 20: `metaphor-build` vs `domain-transfer`
- **Test Problem**: Explaining distributed cache complexity to non-technical product manager
- **Overlap**: ~65-70% | **Verdict**: Keep both separate
- **metaphor-build**: Creates analogies to EXPLAIN concepts and enable understanding
- **domain-transfer**: Borrows patterns from other fields to SOLVE problems
- **Key distinction**: Communication tool vs problem-solving technique
- **When to use**: metaphor-build for teaching/explaining, domain-transfer for innovation/solutions
- **Different outputs**: metaphor-build creates mental models, domain-transfer extracts actionable patterns

---

## Summary of All Findings

### Tested Skills: 20 experiments covering 30 skills

| Skill Pair | Overlap | Verdict |
|------------|---------|---------|
| **Phase 1** | | |
| branch ↔ alternatives | 10% | Keep separate (different stages) |
| tree-explore ↔ graph-wander | 35% | Keep separate (different philosophies) |
| lateral-think ↔ domain-transfer ↔ random-input | 40% | Keep all (different creative modes) |
| weigh-options ↔ leverage-find | 40% | Keep separate (evaluation vs prioritization) |
| decompose ↔ root-cause | 45% | Keep separate (breadth vs depth) |
| connect-dots ↔ theme-find | 60% | Keep as variants (concrete vs abstract) |
| assumption-reveal ↔ socratic | 65% | **MERGE** (subset relationship) |
| thinking-monitor ↔ cycle-detect | 70% | Keep as specialized variant |
| perspective-shift ↔ six-hats | 75% | Six-hats is structured framework |
| premortem (standalone) | N/A | Keep (unique temporal inversion) |
| **Phase 2** | | |
| first-principles ↔ socratic | 60% | Keep separate (generative vs analytical) |
| integrate ↔ connect-dots | 75% | Keep separate (tensions vs relationships) |
| integrate ↔ theme-find | 65% | Keep separate (tensions vs patterns) |
| connect-dots ↔ theme-find | 60% | Keep separate (relationships vs themes) |
| scenario-planning ↔ premortem | 40-45% | Keep separate (multiple vs single future) |
| feynman ↔ socratic | 35-40% | Keep separate (teach vs question) |
| dialectic ↔ perspective-shift | 65-70% | Keep separate (ideas vs people) |
| **Phase 3** | | |
| evidence-check ↔ socratic | 70-75% | Keep separate (evidence vs reasoning) |
| fallacy-detect ↔ logic-trace | 75% | Keep separate (pattern vs structure) |
| confidence-calibrate ↔ knowledge-check | 65-70% | Keep separate (certainty vs gaps) |
| fork-detect ↔ cycle-detect | 60-70% | Keep separate (preventive vs remedial) |
| metaphor-build ↔ domain-transfer | 65-70% | Keep separate (explain vs solve) |

### Overlap Distribution

```
Highly Distinct (0-40%)           Moderate (40-65%)              High (65-80%)
─────────────────────────────────────────────────────────────────────────────
branch ↔ alternatives (10%)       decompose ↔ root-cause (45%)   assumption-reveal ↔
tree-explore ↔ graph-wander (35%) scenario-planning ↔              socratic (65%) **MERGE**
feynman ↔ socratic (35-40%)         premortem (40-45%)           dialectic ↔
lateral-think ↔ domain-transfer   weigh-options ↔                  perspective-shift (65-70%)
  ↔ random-input (40%)              leverage-find (40%)          confidence-calibrate ↔
                                   connect-dots ↔                   knowledge-check (65-70%)
                                     theme-find (60%)             fork-detect ↔
                                   first-principles ↔               cycle-detect (60-70%)
                                     socratic (60%)               metaphor-build ↔
                                   integrate ↔ theme-find (65%)     domain-transfer (65-70%)
                                                                  thinking-monitor ↔
                                                                    cycle-detect (70%)
                                                                  evidence-check ↔
                                                                    socratic (70-75%)
                                                                  fallacy-detect ↔
                                                                    logic-trace (75%)
                                                                  integrate ↔
                                                                    connect-dots (75%)
                                                                  perspective-shift ↔
                                                                    six-hats (75%)
```

### Key Insights Across All 20 Experiments

1. **High overlap ≠ redundancy (The Core Finding)**
   - 15 of 20 experiments showed 60-75% overlap, yet only 1 merge recommended
   - Skills with high overlap can be highly distinct if they serve different:
     - Cognitive modes (pattern recognition vs structural analysis)
     - Problem-solving stages (preventive vs remedial)
     - Output types (assessment vs plan vs questions vs patterns)
     - Use cases (communication vs problem-solving)

2. **Different cognitive modes create distinctness**
   - **Generative vs analytical**: first-principles (builds new) vs socratic (tests existing)
   - **Pattern vs structure**: fallacy-detect (names errors) vs logic-trace (validates chains)
   - **Explain vs solve**: metaphor-build (teaching) vs domain-transfer (innovation)
   - Even when finding same problems, the mode of operation differs meaningfully

3. **Timing and stage differentiation**
   - **Preventive vs remedial**: fork-detect (before stuck) vs cycle-detect (after stuck)
   - **Decision phases**: scenario-planning (should we?) vs premortem (what could go wrong?)
   - **Problem-solving stages**: branch (solutions) vs alternatives (causes)
   - When to apply matters as much as what the skill does

4. **Multiple synthesis modes coexist**
   - integrate (reconciles tensions), connect-dots (maps relationships), theme-find (categorizes patterns)
   - All three synthesize inputs but produce fundamentally different outputs
   - 60-75% overlap doesn't make them redundant - each serves distinct synthesis needs

5. **Specialized vs general patterns**
   - Some skills are specialized versions of broader skills
   - **Keep as variants when**: Specialization provides significantly more actionable focus
   - **Merge when**: Specialization adds no meaningful value (assumption-reveal ⊂ socratic)
   - cycle-detect kept because loop-specific focus is immediately actionable

6. **Creative entry points justify moderate overlap**
   - lateral-think, domain-transfer, random-input all use analogical reasoning (~40% overlap)
   - Each unlocks creativity differently: provocative vs systematic vs chaotic
   - Worth keeping multiple paths - different prompts activate different reasoning modes

7. **Evidence vs reasoning distinction**
   - evidence-check (evaluates sources/data) vs socratic (tests logic/assumptions)
   - Both examine claims critically but from orthogonal angles
   - Complementary rather than redundant - use both for complete analysis

8. **Communication vs problem-solving tools**
   - metaphor-build creates teaching analogies, domain-transfer extracts actionable patterns
   - Same technique (analogies) serving different fundamental purposes
   - The "what" overlaps, the "why" differs completely

---

## Pattern Analysis: What Makes Skills Distinct?

Based on 6 experiments, several patterns emerge about what makes skills functionally distinct for AI reasoning:

### **Pattern 1: Problem-Solving Stage Differentiation**

Skills that operate at different stages are highly distinct even if they seem similar:
- **branch** (solutions) vs **alternatives** (causes) - Same divergent mode, different application
- Result: 10% overlap, keep both

**Principle**: When to apply the skill matters as much as what the skill does.

### **Pattern 2: Scope Breadth Creates Subsets**

Skills with narrower scope that fit entirely within broader skills show high overlap:
- **cycle-detect** ⊂ **thinking-monitor** (loop-specific vs general metacognition)
- **assumption-reveal** ⊂ **socratic** (assumptions-only vs comprehensive questioning)
- Result: 65-70% overlap, consider merging or marking as subsets

**Principle**: If skill A does everything skill B does plus more, B is redundant unless its focus provides significant value.

### **Pattern 3: Abstraction Level Matters**

Skills operating at different abstraction levels on the same domain are moderately distinct:
- **connect-dots** (concrete relationships) vs **theme-find** (abstract patterns)
- Result: 60% overlap, keep as variants

**Principle**: Same cognitive operation at different altitudes serves different purposes.

### **Pattern 4: Creative Entry Points Have Value**

Multiple skills for the same goal (analogical reasoning) justify their existence if they provide different creative pathways:
- **lateral-think** (broad, provocative) vs **domain-transfer** (systematic) vs **random-input** (chaotic)
- Result: 40% overlap, keep all three

**Principle**: Different prompts unlock different creative modes even with overlapping outcomes.

### **Pattern 5: Exploration Philosophy**

Fundamentally different approaches to the same meta-task (exploration) create distinct value:
- **tree-explore** (systematic coverage) vs **graph-wander** (associative discovery)
- Result: 35% overlap, keep both

**Principle**: HOW you explore matters as much as WHAT you explore.

---

## Emerging Skill Taxonomy

Based on experimental data, skills cluster into:

### **1. Root Skills** (broad, general-purpose)
- `socratic` (comprehensive questioning)
- `thinking-monitor` (general metacognition)
- `systems-thinking` (holistic analysis)

### **2. Specialized Skills** (focused applications of root skills)
- `cycle-detect` (specialized from thinking-monitor)
- `assumption-reveal` (specialized from socratic)
- `root-cause` (likely specialized from decompose - untested)

### **3. Complementary Pairs** (different modes of same operation)
- `tree-explore` + `graph-wander` (systematic vs associative exploration)
- `branch` + `alternatives` (solutions vs causes)
- `connect-dots` + `theme-find` (concrete vs abstract pattern-finding)

### **4. Creative Toolkit** (multiple paths to creativity)
- `lateral-think`, `domain-transfer`, `random-input` (analogical reasoning variants)
- `constraint-play`, `reversal` (likely complementary - untested)

---

## Remaining Tests Needed

### High Priority ✅ COMPLETE
- [x] `thinking-monitor` vs `cycle-detect` - **70% overlap, keep as specialized variant**
- [x] `assumption-reveal` vs `socratic` - **65% overlap, merge or mark as subset**
- [x] `tree-explore` vs `graph-wander` - **35% overlap, keep both separate**

### Medium Priority ✅ COMPLETE
- [x] `decompose` vs `root-cause` - **45% overlap, keep both separate (see Exp 7)**
- [x] `weigh-options` vs `leverage-find` - **40% overlap, keep both separate (see Exp 8)**
- [x] `perspective-shift` vs `six-hats` - **75% overlap, six-hats is structured variant (see Exp 9)**
- [ ] `first-principles` vs `socratic` (questioning approaches)

### Lower Priority
- [ ] `perspective-shift` vs `six-hats` (viewpoint shifting)
- [ ] `integrate` vs `synthesize` (if separate skill exists)
- [ ] Various other pairs as patterns emerge

---

## Methodology Notes

### Test Protocol
1. Select a rich, realistic problem that allows multiple reasoning approaches
2. Spawn separate agents with identical problem, different skill assignments
3. Instruct agents to use ONLY the assigned skill
4. Compare outputs for:
   - Reasoning approach (diagnostic, generative, analytical, etc.)
   - Abstraction level (concrete, abstract, meta)
   - Output type (causes, solutions, patterns, insights, etc.)
   - Insight uniqueness (what does each find that others don't?)
5. Estimate overlap percentage
6. Decide: merge, keep separate, mark as variants

### Overlap Estimation Guidelines
- **0-20%**: Highly distinct, definitely keep separate
- **20-40%**: Moderately distinct, keep separate
- **40-60%**: Significant overlap, consider variants
- **60-80%**: High overlap, strong merge candidate
- **80-100%**: Functionally identical, merge required

### Decision Framework
- Keep separate if: Different problem-solving stage, different reasoning mode, or different creative entry point
- Mark as variants if: Same root operation but different abstraction levels or different scopes
- Merge if: Produces essentially identical outputs with no meaningful distinction

---

## Next Steps

1. Complete high-priority experiments
2. Analyze patterns across all results
3. Create final consolidation recommendations
4. Document skill composition patterns
5. Update plugin organization

---

---

## Experiments 7-10: Parallel Testing Results (Concise)

### Experiment 7: `decompose` vs `root-cause`
- **Overlap**: ~45% | **Verdict**: Keep both separate
- **decompose**: Breaks problem into components systematically (functional, temporal, spatial boundaries)
- **root-cause**: Drills down through causation layers using "why" iterations
- **Key distinction**: Breadth (decompose) vs depth (root-cause). Different problem-solving approaches.

### Experiment 8: `weigh-options` vs `leverage-find`
- **Overlap**: ~40% | **Verdict**: Keep both separate
- **weigh-options**: Evaluates tradeoffs across all options equally (benefits, costs, risks, constraints)
- **leverage-find**: Identifies highest-leverage intervention points (bottlenecks, amplification, compounding)
- **Key distinction**: Comprehensive evaluation vs strategic prioritization. Both valuable for decisions.

### Experiment 9: `perspective-shift` vs `six-hats`
- **Overlap**: ~75% | **Verdict**: Six-hats is structured framework for perspective-shift
- **perspective-shift**: General viewpoint shifting (user, builder, maintainer, business, etc.)
- **six-hats**: Structured framework with 6 specific thinking modes (facts, emotions, risks, benefits, creativity, process)
- **Key distinction**: Six-hats is a named technique implementing perspective-shift systematically.

### Experiment 10: `premortem` analysis (standalone)
- **Character**: Temporal inversion + risk analysis. Imagines failure, works backward to causes.
- **Unique value**: Surfaces hidden risks and assumptions that forward-thinking planning misses.
- **Relationship**: Complements `weigh-options` (evaluates options) and `leverage-find` (finds high-leverage points). Different enough to keep.

---

## Comprehensive Analysis: Root Verbs and Cognitive Operations

### Identified Root Cognitive Operations

Based on 10 experiments covering 20 skills, the following fundamental cognitive operations emerge:

#### **Core Root Verbs** (12 fundamental operations)

1. **Diverge** - Generate multiple possibilities
   - Skills: `branch`, `alternatives`, `random-input`
   - Distinctness: Applied at different problem-solving stages (solutions vs causes vs creative stimuli)

2. **Converge** - Synthesize multiple inputs into unified understanding
   - Skills: `integrate`, `theme-find`, `connect-dots`
   - Distinctness: Different abstraction levels (concrete relationships vs abstract themes)

3. **Decompose** - Break wholes into parts
   - Skills: `decompose`, `root-cause`
   - Distinctness: Structural breakdown vs causal drilling (breadth vs depth)

4. **Question** - Systematic inquiry
   - Skills: `socratic`, `assumption-reveal`
   - Distinctness: Comprehensive questioning vs focused assumption extraction (superset vs subset)

5. **Explore** - Navigate possibility space
   - Skills: `tree-explore`, `graph-wander`
   - Distinctness: Systematic coverage vs associative discovery (different philosophies)

6. **Reframe** - Change perspective or framing
   - Skills: `perspective-shift`, `six-hats`, `reversal`
   - Distinctness: General reframing vs structured frameworks

7. **Analogize** - Find and apply cross-domain patterns
   - Skills: `lateral-think`, `domain-transfer`, `random-input`, `metaphor-build`
   - Distinctness: Different creative entry points (provocative vs systematic vs chaotic)

8. **Monitor** - Observe thinking process
   - Skills: `thinking-monitor`, `cycle-detect`
   - Distinctness: General metacognition vs specialized loop detection

9. **Evaluate** - Assess options and tradeoffs
   - Skills: `weigh-options`, `premortem`, `leverage-find`
   - Distinctness: Comprehensive evaluation vs temporal inversion vs strategic prioritization

10. **Model** - Build mental representations
    - Skills: `systems-thinking`, `first-principles`
    - Distinctness: Holistic systems vs foundational axioms

11. **Abstract** - Move from concrete to general
    - Skills: `principle-extract`, `theme-find`, `abstraction-ladder`
    - Distinctness: Different sources and scopes of abstraction

12. **Constrain** - Apply or manipulate limitations
    - Skills: `constraint-play`, `reversal`
    - Distinctness: Creative use of constraints vs inversion of assumptions

### Skill Relationship Matrix

```
ROOT SKILLS (Broad, general-purpose)
├── socratic (comprehensive questioning)
│   └── assumption-reveal (specialized subset) ⚠️ MERGE CANDIDATE
├── thinking-monitor (general metacognition)
│   └── cycle-detect (specialized loop detection) ✓ KEEP AS VARIANT
├── systems-thinking (holistic modeling)
├── decompose (structural breakdown)
│   └── root-cause (causal drilling) ✓ KEEP SEPARATE (depth vs breadth)
└── perspective-shift (general reframing)
    └── six-hats (structured framework) ✓ KEEP AS STRUCTURED VARIANT

STAGE-DIFFERENTIATED PAIRS (Same operation, different application points)
├── branch (solution generation) + alternatives (cause analysis) ✓ HIGHLY DISTINCT
├── weigh-options (evaluation) + leverage-find (prioritization) ✓ DISTINCT
└── connect-dots (concrete) + theme-find (abstract) ✓ KEEP AS VARIANTS

CREATIVE TOOLKIT (Multiple entry points to creativity)
├── lateral-think (provocative, assumption-challenging)
├── domain-transfer (systematic cross-domain mapping)
└── random-input (chaotic forced associations)
└── All three ✓ KEEP SEPARATE (different creative modes)

EXPLORATION MODES (Different philosophies)
├── tree-explore (systematic coverage)
└── graph-wander (associative discovery)
└── Both ✓ KEEP SEPARATE (fundamentally different approaches)

TEMPORAL ANALYSIS
└── premortem (temporal inversion + risk analysis) ✓ UNIQUE, KEEP
```

### Final Overlap Distribution Analysis

```
Distinctness Spectrum
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

HIGHLY DISTINCT (0-40%)
├── branch ↔ alternatives (10%) - Different problem-solving stages
├── tree-explore ↔ graph-wander (35%) - Different exploration philosophies
├── lateral-think ↔ domain-transfer ↔ random-input (40%) - Different creative entry points
├── weigh-options ↔ leverage-find (40%) - Evaluation vs prioritization
└── decompose ↔ root-cause (45%) - Breadth vs depth

MODERATELY OVERLAPPING (40-65%)
├── premortem (standalone, ~40-50% with decision skills) - Temporal inversion adds unique value
└── connect-dots ↔ theme-find (60%) - Same operation, different abstraction levels

HIGH OVERLAP - REDUNDANCY CANDIDATES (65-80%)
├── assumption-reveal ↔ socratic (65%) - ⚠️ Subset relationship, MERGE CANDIDATE
├── thinking-monitor ↔ cycle-detect (70%) - Specialized variant, KEEP with documentation
└── perspective-shift ↔ six-hats (75%) - Structured framework variant, KEEP
```

### Definitive Patterns from All Experiments

#### **Pattern 1: Problem-Solving Stage Differentiation** (10-45% overlap)

Skills operating at different problem-solving stages are highly distinct even with similar cognitive operations:

- **branch** (solutions) vs **alternatives** (causes): 10% overlap
- **decompose** (structural) vs **root-cause** (causal): 45% overlap

**Decision Rule**: Keep separate when skills apply the same operation at fundamentally different stages of problem-solving.

#### **Pattern 2: Scope Relationship** (65-70% overlap)

Skills with narrower scope that fit within broader skills show high overlap:

- **assumption-reveal** ⊂ **socratic**: 65% overlap - socratic does everything assumption-reveal does plus more
- **cycle-detect** ⊂ **thinking-monitor**: 70% overlap - cycle-detect is specialized loop detection

**Decision Rule**:
- If overlap > 65% AND one skill is strict subset: **Merge or document as specialized variant**
- Exception: Keep specialized variants if they provide significantly more actionable focus

#### **Pattern 3: Abstraction Level Differentiation** (60% overlap)

Skills operating at different abstraction levels on the same cognitive operation are moderately distinct:

- **connect-dots** (concrete relationships) vs **theme-find** (abstract patterns): 60% overlap

**Decision Rule**: Keep as variants when abstraction level difference serves different purposes (concrete system analysis vs conceptual synthesis).

#### **Pattern 4: Creative Entry Points** (40% overlap)

Multiple skills for similar outcomes justify existence if they provide different creative activation modes:

- **lateral-think** vs **domain-transfer** vs **random-input**: ~40% overlap
- Each unlocks creativity differently: provocative vs systematic vs chaotic

**Decision Rule**: Keep multiple creative pathways even with moderate overlap. Different prompts activate different reasoning modes in AI agents.

#### **Pattern 5: Philosophical Approach Differentiation** (35% overlap)

Fundamentally different approaches to the same meta-task create distinct value:

- **tree-explore** (systematic completeness) vs **graph-wander** (associative discovery): 35% overlap

**Decision Rule**: Keep separate when the HOW matters as much as the WHAT. Different exploration philosophies serve different cognitive goals.

#### **Pattern 6: Structured Framework Variants** (75% overlap)

Named techniques that implement general operations in structured ways:

- **six-hats** is structured implementation of **perspective-shift**: 75% overlap

**Decision Rule**: Keep structured frameworks even with high overlap. The framework itself adds value through standardization and shared vocabulary.

#### **Pattern 7: Strategic vs Comprehensive Evaluation** (40% overlap)

Skills that evaluate but with different optimization targets:

- **weigh-options** (comprehensive tradeoff analysis) vs **leverage-find** (strategic prioritization): 40% overlap

**Decision Rule**: Keep separate when optimization targets differ (completeness vs leverage).

### Compositionality Analysis

Skills naturally chain in common sequences:

1. **Diagnosis → Solution**
   - `alternatives` → `branch` (understand causes, then generate solutions)
   - `socratic` → `first-principles` (question assumptions, then rebuild from fundamentals)
   - `decompose` → `leverage-find` (break down system, identify high-leverage points)

2. **Exploration → Synthesis**
   - `tree-explore` or `graph-wander` → `theme-find` or `connect-dots` (explore space, find patterns)
   - `domain-transfer` → `principle-extract` (apply analogies, extract universal principles)

3. **Evaluation → Decision**
   - `weigh-options` → `premortem` (evaluate options, stress-test choice)
   - `perspective-shift` → `leverage-find` (see from multiple angles, identify high-leverage actions)

4. **Metacognitive Loops**
   - `thinking-monitor` or `cycle-detect` → any skill (notice stuck patterns, apply corrective skill)
   - `assumption-reveal` or `socratic` → any generative skill (surface assumptions, rebuild solution)

Skills with high compositionality should be kept even with moderate overlap.

---

## Final Recommendations: Evidence-Based Consolidation

### Executive Summary

**Current State**: 49 skills across 8 categories
**Tested**: 20 skills through 10 controlled experiments
**Key Finding**: Most tested skills are distinct enough to keep (only 1 clear merge candidate)
**Primary Issue**: Skills need better documentation of relationships, not aggressive consolidation

### Immediate Actions

#### **Action 1: MERGE `assumption-reveal` into `socratic`**

**Evidence**: 65% overlap, strict subset relationship
**Rationale**: Socratic method includes assumption revelation plus evidence examination, reasoning checks, implication exploration, and question reframing
**Impact**: Reduces cognitive load without losing functionality

**Implementation**:
```
1. Update socratic skill documentation to explicitly mention assumption revelation mode
2. Add example showing socratic used specifically for assumptions
3. Archive assumption-reveal with redirect to socratic
4. Update any references or documentation
```

**User guidance**: "For assumption-focused work, use socratic with explicit focus on assumption questioning"

---

#### **Action 2: DOCUMENT Specialized Variants**

**Evidence**: Several skills are specialized applications of broader skills (65-75% overlap)

**Variants to document**:

1. **`cycle-detect` as specialized variant of `thinking-monitor`**
   - Overlap: 70%
   - Keep both: cycle-detect provides focused, actionable loop-breaking
   - Documentation: Add to both skill files noting relationship
   - When to use: thinking-monitor for general metacognition, cycle-detect when specifically stuck in loops

2. **`six-hats` as structured variant of `perspective-shift`**
   - Overlap: 75%
   - Keep both: six-hats provides standardized framework with shared vocabulary
   - Documentation: Note that six-hats is specific implementation of perspective-shift
   - When to use: perspective-shift for flexible viewpoint changes, six-hats for structured group decision-making

3. **`root-cause` as depth-focused variant of `decompose`**
   - Overlap: 45%
   - Keep both: fundamentally different approaches (breadth vs depth)
   - Documentation: Note complementary relationship
   - When to use: decompose for structural understanding, root-cause for causal chain drilling

**Implementation**: Add "Relationship" section to each skill's SKILL.md noting related skills and when to use each.

---

#### **Action 3: REORGANIZE by Root Verbs (Optional Long-term)**

**Current organization**: By thematic categories (analysis, creativity, decision, etc.)
**Proposed organization**: By cognitive operation with variants grouped

**Evidence-based structure**:

```
skills/
├── diverge/
│   ├── branch/              (solution generation)
│   ├── alternatives/        (cause analysis)
│   └── random-input/        (creative stimuli)
├── converge/
│   ├── theme-find/          (abstract synthesis)
│   ├── connect-dots/        (concrete synthesis)
│   └── integrate/           (comprehensive synthesis)
├── decompose/
│   ├── decompose/           (structural breakdown)
│   └── root-cause/          (causal drilling)
├── question/
│   └── socratic/            (comprehensive questioning - absorbed assumption-reveal)
├── explore/
│   ├── tree-explore/        (systematic coverage)
│   └── graph-wander/        (associative discovery)
├── reframe/
│   ├── perspective-shift/   (general reframing)
│   ├── six-hats/            (structured framework)
│   └── reversal/            (inversion)
├── analogize/
│   ├── lateral-think/       (provocative)
│   ├── domain-transfer/     (systematic)
│   ├── random-input/        (chaotic) [note: also in diverge]
│   └── metaphor-build/      (explanatory)
├── monitor/
│   ├── thinking-monitor/    (general metacognition)
│   └── cycle-detect/        (loop detection)
├── evaluate/
│   ├── weigh-options/       (comprehensive evaluation)
│   ├── leverage-find/       (strategic prioritization)
│   └── premortem/           (temporal inversion)
├── model/
│   ├── systems-thinking/    (holistic)
│   └── first-principles/    (axiomatic)
├── abstract/
│   ├── principle-extract/   (from examples)
│   ├── theme-find/          (from patterns) [note: also in converge]
│   └── abstraction-ladder/  (level navigation)
└── constrain/
    ├── constraint-play/     (creative constraints)
    └── reversal/            (assumption inversion) [note: also in reframe]
```

**Note**: Some skills naturally belong to multiple roots (e.g., random-input is both diverge and analogize). This is expected and valuable.

**Implementation Priority**: LOW - current organization works, this is optimization

---

### Retention Decisions (All Tested Skills)

#### **KEEP SEPARATE - Highly Distinct (0-45% overlap)**

1. **branch ↔ alternatives** (10%)
   - Different problem-solving stages
   - Evidence: Experiment 1

2. **tree-explore ↔ graph-wander** (35%)
   - Different exploration philosophies
   - Evidence: Experiment 6

3. **lateral-think ↔ domain-transfer ↔ random-input** (40%)
   - Different creative entry points
   - Evidence: Experiment 3

4. **weigh-options ↔ leverage-find** (40%)
   - Comprehensive evaluation vs strategic prioritization
   - Evidence: Experiment 8

5. **decompose ↔ root-cause** (45%)
   - Breadth vs depth approaches
   - Evidence: Experiment 7

6. **premortem** (standalone)
   - Unique temporal inversion approach
   - Evidence: Experiment 10

#### **KEEP AS VARIANTS - Document Relationships (60-75% overlap)**

1. **connect-dots ↔ theme-find** (60%)
   - Different abstraction levels serve different purposes
   - Evidence: Experiment 2

2. **thinking-monitor ↔ cycle-detect** (70%)
   - General vs specialized metacognition
   - Evidence: Experiment 4

3. **perspective-shift ↔ six-hats** (75%)
   - General vs structured framework
   - Evidence: Experiment 9

#### **MERGE - Redundant (65% overlap, subset relationship)**

1. **assumption-reveal → socratic**
   - Strict subset with no unique value
   - Evidence: Experiment 5

---

### Skills Requiring Further Testing

**High Priority** (likely overlaps to investigate):

1. **first-principles vs socratic** - Both question fundamentals, may overlap significantly
2. **integrate vs connect-dots vs theme-find** - All synthesize, relationships unclear
3. **scenario-planning vs premortem** - Both temporal reasoning, may overlap
4. **feynman vs socratic** - Both use questioning, feynman more pedagogical
5. **dialectic vs perspective-shift** - Both examine multiple viewpoints

**Medium Priority** (possible overlaps):

1. **evidence-check vs socratic** - Socratic examines evidence
2. **fallacy-detect vs logic-trace** - Both analyze reasoning quality
3. **confidence-calibrate vs knowledge-check** - Both assess certainty
4. **fork-detect vs cycle-detect** - Both identify decision points
5. **metaphor-build vs domain-transfer** - Both use analogies

**Lower Priority** (likely distinct but worth confirming):

1. Creative constraints cluster (constraint-play, reversal, scamper)
2. Synthesis cluster (integrate, principle-extract, theme-find)
3. Navigation cluster (abstraction-ladder, trajectory-sense)
4. Decision support cluster (priority-matrix, fork-detect)

---

### Implementation Roadmap

#### **Phase 1: Immediate (High Confidence)**

**Week 1**:
- ✅ Merge assumption-reveal into socratic
- ✅ Update documentation for 3 variant pairs
- ✅ Add "Related Skills" sections to tested skills

**Deliverable**: 20 skills with clear relationship documentation, 1 merge complete

#### **Phase 2: Additional Testing (Medium Confidence)**

**Week 2-3**:
- Run 5 high-priority experiments (first-principles/socratic, integrate/connect-dots/theme-find, etc.)
- Document results using same methodology
- Make merge/keep decisions with same evidence standards

**Deliverable**: 10 more skills analyzed, 2-3 additional merges likely

#### **Phase 3: Comprehensive Review (Lower Confidence)**

**Week 4-5**:
- Test remaining medium and lower priority pairs
- Identify any additional consolidation opportunities
- Final relationship documentation

**Deliverable**: All 49 skills analyzed, comprehensive relationship map

#### **Phase 4: Reorganization (Optional)**

**Week 6-8**:
- Implement root verb organization if desired
- Update all documentation
- Migration guide for users

**Deliverable**: Skills organized by cognitive operation rather than theme

---

### Key Principles for Future Skill Development

Based on experimental findings, new skills should:

1. **Operate at different problem-solving stages** than existing skills (diagnosis vs solution vs evaluation)
2. **Provide distinct creative entry points** even if overlapping with existing skills
3. **Use structured frameworks** that add value through standardization
4. **Target different abstraction levels** if similar to existing skills
5. **Have clear composition patterns** with other skills

**Anti-patterns to avoid**:
- Creating narrower subsets of existing broad skills (unless significant actionability gain)
- Adding skills that differ only in terminology, not reasoning mode
- Creating skills that produce functionally identical outputs to existing ones

---

### Success Metrics

**Quantitative**:
- Reduce total skills by 5-10% through evidence-based merging (target: 44-46 skills from 49)
- Document relationships for 100% of skills
- Test coverage: 100% of skills analyzed by end of Phase 3

**Qualitative**:
- Each skill has clear "when to use" guidance
- Skills compose well in documented chains
- No skills produce functionally identical outputs
- Users can quickly identify right skill for their need

---

### Conclusion

**Main Finding**: The thinkies plugin is remarkably well-designed. Of 20 tested skills, only 1 requires merging.

**Core Insight**: The problem is not redundancy, but insufficient documentation of relationships. Skills that overlap 40-75% are still valuable because they:
- Provide different entry points to creativity
- Operate at different problem-solving stages
- Serve different abstraction levels
- Offer structured frameworks vs flexible approaches

**Recommendation**: Focus on documentation over consolidation. The diversity of skills is a strength, not a weakness, when relationships are clear.

**Next Steps**:
1. Execute Phase 1 (merge assumption-reveal, document variants)
2. Plan Phase 2 testing for high-priority pairs
3. Consider long-term reorganization by root verbs (optional)

---

---

## "When to Use" Clarity Analysis

### Purpose

This section analyzes the distinctness and clarity of "when to use" guidance for all tested and to-be-tested skills. The goal is to ensure each skill has clear, non-overlapping use cases that make skill selection intuitive for AI agents.

### Analysis Framework

**Clarity Criteria**:
1. **Specificity**: Does the guidance point to concrete situations?
2. **Distinctness**: Is it clearly different from related skills?
3. **Trigger identification**: Can an agent recognize when to invoke this skill?
4. **Problem-stage alignment**: Is it clear what problem-solving stage this serves?

**Overlap Assessment**:
- **No overlap**: Completely distinct use cases
- **Partial overlap**: Some situations could use either skill, but primary use cases differ
- **Significant overlap**: Hard to choose between skills based on use case alone
- **Subset**: One skill's use cases are entirely contained in another's

---

### Already Tested Skills - "When to Use" Analysis

#### **Divergent Pair: branch vs alternatives**

**branch** (Solution generation):
- "Feeling stuck on single approach"
- "Need alternatives for decision-making"
- "Avoid premature convergence"
- "Exploring what's possible before committing"
- "Creating fallback options"
- "Challenging linear thinking"

**alternatives** (Cause analysis):
- "Investigating mysterious bugs"
- "Understanding user behavior"
- "Avoiding confirmation bias"
- "Scientific problem-solving"
- "Incident analysis"
- "Market research interpretation"
- "A/B test analysis"
- "Medical/technical diagnosis"

**Clarity Assessment**: ✅ **EXCELLENT - Highly distinct**
- **Trigger difference**: branch = "need solution options", alternatives = "need to explain observations"
- **Stage difference**: branch = generative, alternatives = analytical
- **No overlap**: Complete separation between generating solutions vs explaining causes
- **Recommendation**: Already clear, no changes needed

---

#### **Pattern Recognition Pair: connect-dots vs theme-find**

**connect-dots** (Concrete relationships):
- "Working with information from multiple sources"
- "Trying to understand complex situations"
- "Looking for underlying causes"
- "Synthesizing research or feedback"
- "Finding new solutions by analogy"
- "Building mental models"
- "Recognizing patterns across time or context"
- "Trying to explain why multiple things are happening"

**theme-find** (Abstract patterns):
- "Analyzing qualitative data or feedback"
- "Making sense of multiple bug reports"
- "Understanding recurring problems"
- "Finding what really matters in a discussion"
- "Synthesizing research findings"
- "Identifying root causes"
- "Understanding team dynamics"
- "Making sense of complex situations"
- "Deciding what to prioritize"

**Clarity Assessment**: ⚠️ **MODERATE - Significant overlap**
- **Overlap areas**: "Synthesizing research", "making sense of complex situations", "underlying/root causes"
- **Distinction not clear in use cases**: Both serve synthesis of multiple inputs
- **Problem**: Can't easily choose between them based on current guidance

**Needs improvement**:
- **connect-dots** should emphasize: "When you need to see HOW things relate mechanistically" - systems thinking, causal chains, network effects
- **theme-find** should emphasize: "When you need to see WHAT unifies things conceptually" - recurring concepts, naming patterns, identifying what matters most

**Recommended "when to use" distinction**:
- Use **connect-dots** when: Building system models, understanding causal relationships, finding how parts interact, explaining mechanisms
- Use **theme-find** when: Making sense of qualitative feedback, identifying what keeps recurring, naming the pattern, deciding priorities

---

#### **Creative Trio: lateral-think vs domain-transfer vs random-input**

**lateral-think** (Provocative assumption-challenging):
- "When conventional solutions aren't working"
- "Innovation or brainstorming sessions"
- "Need breakthrough ideas"
- "Facing wicked or complex problems"
- "When team thinking too similarly"
- "To challenge implicit constraints"
- "When stuck in analysis paralysis"
- "Exploring new product directions"

**domain-transfer** (Systematic cross-domain mapping):
- "Stuck on problem with no obvious solution"
- "Need creative breakthrough"
- "Want to challenge industry assumptions"
- "Looking for innovative approaches"
- "Traditional solutions aren't working"
- "Need to explain complex ideas simply"
- "Building mental models"
- "Cross-functional team communication"

**random-input** (Chaotic forced associations):
- "Breaking through creative blocks"
- "Generating fresh ideas when stuck in obvious solutions"
- "Brainstorming sessions that feel stale"
- "Finding new metaphors for communication"
- "Challenging assumptions you didn't know you had"
- "Solo ideation when need to think differently"
- "Adding variety to problem-solving approaches"
- "Making connections between disparate concepts"

**Clarity Assessment**: ⚠️ **MODERATE - Significant overlap**
- **Overlap areas**: All three mention "breakthrough", "stuck", "conventional not working", "innovative"
- **Distinction exists but not in use cases**: The HOW differs (provocative vs systematic vs chaotic) but WHEN is similar
- **Problem**: Agent would struggle to choose based on situation alone

**Needs improvement**: Differentiate by PROCESS preference rather than just situation:

**Recommended distinctions**:
- Use **lateral-think** when: You want to CHALLENGE assumptions directly - question what must be true, reverse the problem, make provocative statements
- Use **domain-transfer** when: You want to STUDY how other fields solve similar patterns - map analogous domains systematically, extract universal principles
- Use **random-input** when: You want to JOLT thinking with unrelated stimuli - force connections from random elements to break all patterns

**Updated use cases**:
- **lateral-think**: "Questioning fundamental constraints, reversing the problem, making provocative 'what ifs', challenging obvious approaches"
- **domain-transfer**: "Learning from biology/nature, borrowing from other industries, finding universal patterns, systematic cross-domain study"
- **random-input**: "Using random objects/words as prompts, forcing absurd connections, breaking predictable thinking, injecting chaos into ideation"

---

#### **Exploration Pair: tree-explore vs graph-wander**

**tree-explore** (from experimental notes):
- Systematic coverage of topic
- When you need comprehensive understanding
- Learning new domain
- Planning project comprehensively
- Ensuring nothing is missed
- Hierarchical branching exploration

**graph-wander** (from experimental notes):
- Associative discovery
- Following connections where they lead
- Finding unexpected insights
- Non-linear exploration
- Discovering surprising patterns
- Creative exploration

**Clarity Assessment**: ✅ **GOOD - Clear distinction**
- **Trigger difference**: tree-explore = "need completeness", graph-wander = "need discovery"
- **Distinction is clear**: Systematic vs associative is easy to recognize
- **Minor improvement needed**: Make the completeness vs creativity distinction more explicit

**Recommended enhancement**:
- **tree-explore**: "When you need comprehensive coverage, systematic learning, structured planning, or ensuring all aspects are considered"
- **graph-wander**: "When you need creative insights, unexpected connections, following curiosity, or discovering non-obvious patterns"

---

#### **Metacognitive Pair: thinking-monitor vs cycle-detect**

**thinking-monitor** (general metacognition - from experimental notes):
- Observing overall thinking patterns
- Detecting biases or reasoning flaws
- Assessing reasoning quality
- General meta-awareness
- Multiple thinking pattern types

**cycle-detect** (specialized loop detection - from experimental notes):
- Specifically stuck in loops
- Recognizing repetitive thinking
- When same ideas keep recurring
- Need to break circular reasoning
- Action-oriented loop-breaking

**Clarity Assessment**: ✅ **GOOD - Clear subset relationship**
- **Distinction is clear**: General observation vs specific loop problem
- **Use cases naturally separate**: thinking-monitor = "observe my thinking", cycle-detect = "I'm stuck in a loop"

**Recommended use cases**:
- **thinking-monitor**: "When you need to examine your reasoning process, check for biases, assess thinking quality, or observe patterns in your approach"
- **cycle-detect**: "When you're stuck repeating the same thoughts, going in circles, can't make progress, or keep returning to the same options"

---

#### **Questioning Pair: socratic vs assumption-reveal**

**socratic** (comprehensive questioning - from system reminders and experimental notes):
- Challenging claims through systematic questioning
- Examining evidence and reasoning
- Testing beliefs rigorously
- Deep understanding through dialog
- Exploring implications
- Questioning the question itself

**assumption-reveal** (specialized assumption extraction - MERGE CANDIDATE):
- Uncovering hidden assumptions
- Making implicit premises explicit
- Testing assumption validity
- Categorizing types of assumptions

**Clarity Assessment**: ⚠️ **MERGE CANDIDATE**
- **Assumption-reveal is subset**: Everything it does, socratic does
- **Overlap**: 65% - assumption revelation is one component of socratic method
- **Decision**: Already marked for merge

**Post-merge guidance**:
- **socratic**: "When you need to question claims, examine assumptions, test reasoning, explore implications, or challenge beliefs systematically through dialog"

---

#### **Decision Support Trio: weigh-options vs leverage-find vs premortem**

**weigh-options** (comprehensive evaluation - from experimental notes):
- Evaluating multiple options
- Need to understand all tradeoffs
- Comparing alternatives systematically
- Balancing competing concerns
- Comprehensive decision analysis

**leverage-find** (strategic prioritization - from experimental notes):
- Identifying high-impact interventions
- Finding bottlenecks and constraints
- Maximizing ROI of efforts
- Strategic focus identification
- Amplification opportunities

**premortem** (temporal inversion - from experimental notes):
- Stress-testing a decision
- Finding hidden risks
- Imagining failure scenarios
- Identifying what could go wrong
- Risk assessment before committing

**Clarity Assessment**: ✅ **EXCELLENT - Distinct decision stages**
- **Sequential relationship**: Often used together (evaluate → prioritize → stress-test)
- **Clear distinctions**: Comprehensive vs strategic vs risk-focused
- **No confusion**: Each serves different decision need

**Recommended use cases**:
- **weigh-options**: "When you need to understand tradeoffs across all options, evaluate benefits/costs/risks comprehensively, or compare alternatives systematically"
- **leverage-find**: "When you need to identify highest-impact actions, find bottlenecks, maximize ROI, or focus on strategic intervention points"
- **premortem**: "When you need to stress-test a decision, identify risks, imagine failure scenarios, or find what could go wrong before committing"

---

#### **Reframing Pair: perspective-shift vs six-hats**

**perspective-shift** (general viewpoint changes):
- Need to see from multiple angles
- Breaking out of single viewpoint
- Understanding stakeholder perspectives
- Empathy for different roles
- Flexible perspective taking

**six-hats** (structured framework - from system reminders):
- Using specific thinking modes (facts, emotions, risks, benefits, creativity, process)
- Structured group decision-making
- Systematic perspective examination
- Shared vocabulary for thinking modes
- Avoiding conflated thinking types

**Clarity Assessment**: ✅ **GOOD - Framework vs general**
- **Distinction is clear**: Flexible vs structured
- **Both have value**: General tool vs named technique
- **Use case difference**: Ad-hoc vs formal

**Recommended use cases**:
- **perspective-shift**: "When you need to see from different viewpoints flexibly, understand stakeholder perspectives, or break out of single-viewpoint thinking"
- **six-hats**: "When you need structured thinking modes, group decision-making with shared vocabulary, or systematic examination of facts/emotions/risks/benefits/creativity/process"

---

#### **Decomposition Pair: decompose vs root-cause**

**decompose** (structural breakdown - from experimental notes):
- Breaking complex into components
- Understanding system structure
- Identifying parts and boundaries
- Analyzing how things are organized
- Breadth-focused analysis

**root-cause** (causal drilling - from experimental notes):
- Finding why something happens
- Iterative "why" questioning
- Drilling to fundamental cause
- Causal chain exploration
- Depth-focused analysis

**Clarity Assessment**: ✅ **EXCELLENT - Breadth vs depth**
- **Clear distinction**: Structure vs causation
- **Different questions**: "What are the parts?" vs "Why does this happen?"
- **Complementary**: Often used together

**Recommended use cases**:
- **decompose**: "When you need to break down complexity, understand system structure, identify components and boundaries, or analyze how things are organized"
- **root-cause**: "When you need to find why something happens, drill to fundamental causes, iterate 'why' questions, or explore causal chains"

---

### Phase 2 Skills - "When to Use" Analysis (TESTED - Results)

#### **first-principles** (Axiomatic reasoning) ✅ TESTED

**Current use cases**:
- "Challenging industry conventions"
- "Designing novel solutions"
- "When best practices don't fit your context"
- "Breaking through innovation barriers"
- "Questioning expensive or complex systems"
- "Simplifying over-engineered solutions"
- "Understanding why things work the way they do"
- "Finding creative solutions to constraints"
- "Avoiding cargo-cult engineering"
- "Building something genuinely new"

**Experimental Results** (Experiment 11):
- **Actual overlap with socratic**: ~60% (higher than predicted 40%)
- **Verdict**: Keep both separate
- **Key distinction validated**: first-principles is GENERATIVE (builds new solutions from axioms), socratic is ANALYTICAL (tests existing reasoning)

**Clarity Assessment**: ✅ **EXCELLENT - Distinct despite high overlap**
- **Distinct cognitive modes**: Building up from fundamentals vs examining through questioning
- **Different outputs**: New approaches vs validated reasoning
- **Clear triggers differentiated**: Use first-principles for "what should we build?", socratic for "is this approach sound?"

**Verified "when to use" distinction**:
- **first-principles**: When you need to REBUILD from fundamental truths, strip away assumptions to find what's actually required, or design novel solutions unconstrained by convention
- **socratic**: When you need to EXAMINE existing claims, test reasoning validity, or challenge beliefs through systematic questioning
- **No confusion**: first-principles generates, socratic validates

---

#### **integrate** (Synthesis of tensions) ✅ TESTED

**Current use cases**:
- "Combining multiple viewpoints"
- "Resolving apparent contradictions"
- "Building comprehensive understanding"
- "Creating shared vision from diverse inputs"
- "Synthesizing research or feedback"
- "Finding solutions that satisfy multiple constraints"
- "Moving from analysis to action"
- "Building team alignment"
- "Creating frameworks from examples"

**Experimental Results** (Experiment 12):
- **Actual overlap**: connect-dots (75%), theme-find (65%), both pairs (60-75% range)
- **Verdict**: Keep all three separate
- **Key distinction validated**: integrate RECONCILES TENSIONS, connect-dots MAPS RELATIONSHIPS, theme-find CATEGORIZES PATTERNS

**Clarity Assessment**: ✅ **GOOD - High overlap but functionally distinct**
- **Different synthesis modes**: Combining contradictions vs discovering connections vs naming patterns
- **Different inputs**: Conflicting perspectives vs disparate information vs recurring observations
- **Different outputs**: Unified frameworks that preserve nuance vs system models vs hierarchies of themes

**Verified "when to use" distinctions**:
- **integrate**: When you have CONFLICTING but valid perspectives that need reconciliation into coherent whole - addresses tensions, contradictions, and competing concerns
- **connect-dots**: When you need to DISCOVER how things relate mechanistically - builds system models, traces causal chains, finds interaction patterns
- **theme-find**: When you need to IDENTIFY and NAME recurring patterns - categorizes, creates hierarchies, surfaces what keeps coming up
- **Clear separation**: Tensions vs relationships vs patterns

---

#### **scenario-planning** (Multiple future exploration) ✅ TESTED

**Current use cases** (from system reminders):
- "Strategic planning under uncertainty"
- "Long-term decision making"
- "Risk assessment and preparation"
- "Testing strategy robustness"
- "Investment decisions with unclear future"
- "Organizational planning"
- "Market entry decisions"
- "Technology adoption planning"
- "Avoiding over-commitment to single forecast"
- "Building adaptive capability"
- "Preparing for multiple possible futures"

**Experimental Results** (Experiment 13):
- **Actual overlap with premortem**: ~40-45% (as predicted)
- **Verdict**: Keep both separate
- **Key distinction validated**: scenario-planning explores MULTIPLE futures, premortem diagnoses SINGLE failure

**Clarity Assessment**: ✅ **EXCELLENT - Clear temporal reasoning split**
- **Different scope**: Multiple plausible futures vs one imagined failure
- **Different questions**: "What could happen?" vs "What went wrong?"
- **Different outputs**: Adaptive strategies across scenarios vs specific failure prevention tactics
- **Sequential use**: Often complementary - scenario-planning first (should we?), then premortem for each scenario

**Verified "when to use" distinctions**:
- **scenario-planning**: When you face UNCERTAINTY and need to explore multiple possible futures, test strategy robustness, or build adaptive capability
- **premortem**: When you have a DECISION/PLAN and need to imagine its failure, work backward to causes, or identify what could go wrong
- **Clear trigger**: Multiple unknowns vs single commitment to stress-test

---

#### **feynman** (Pedagogical explanation) ✅ TESTED

**Current use cases** (from system reminders):
- "Learning a new technology, framework, or domain"
- "Before a technical interview or presentation"
- "When documentation seems clear but you can't apply it"
- "Debugging conceptual confusion on your team"
- "Preparing to mentor or teach"
- "Validating that you actually understand something"
- "Converting expert knowledge into accessible documentation"
- "Revealing hidden assumptions in your thinking"
- "Building genuine intuition versus surface familiarity"

**Experimental Results** (Experiment 14):
- **Actual overlap with socratic**: ~35-40% (lower than predicted 50-60%)
- **Verdict**: Keep both separate
- **Key distinction validated**: feynman BUILDS UP (teach to learn), socratic DIGS DOWN (question to examine)

**Clarity Assessment**: ✅ **EXCELLENT - Lower overlap than expected**
- **Opposite directions**: Simple→complete vs claim→foundations
- **Different purposes**: Validate understanding vs challenge reasoning
- **Different outputs**: Simple explanations vs systematic questioning
- **When to choose is clear**: Do I understand? vs Does this hold up?

**Verified "when to use" distinctions**:
- **feynman**: When you need to LEARN by teaching, validate your understanding by explaining simply, identify knowledge gaps through attempts to teach
- **socratic**: When you need to CHALLENGE claims, examine assumptions, or test reasoning through systematic questioning
- **Clear trigger**: "Do I truly understand this?" vs "Does this reasoning hold?"

---

#### **dialectic** (Thesis-antithesis-synthesis) ✅ TESTED

**Current use cases** (from system reminders):
- "Resolving team disagreements"
- "Getting past polarized debates"
- "Refining your own thinking when you see merit in opposing views"
- "Design decisions with valid competing concerns"
- "Strategic planning with different stakeholder priorities"
- "Philosophical or architectural debates"
- "Finding the truth between extremes"
- "Transcending false dichotomies"
- "Developing nuanced positions"
- "Moving conversations past 'you're wrong, I'm right'"

**Experimental Results** (Experiment 15):
- **Actual overlap with perspective-shift**: ~65-70% (as predicted)
- **Verdict**: Keep both separate
- **Key distinction validated**: dialectic handles IDEA conflicts, perspective-shift handles PEOPLE conflicts

**Clarity Assessment**: ✅ **GOOD - High overlap but clear use case split**
- **Different conflict types**: Binary opposing concepts vs multiple stakeholder viewpoints
- **Different structure**: Thesis/antithesis/synthesis vs parallel perspective exploration
- **Different outputs**: Transcendent synthesis vs empathetic understanding
- **When to choose is clear**: Conceptual paradoxes vs stakeholder conflicts

**Verified "when to use" distinctions**:
- **dialectic**: When you have TWO OPPOSING ideas/positions and need to find higher truth that transcends the binary - philosophical tensions, conceptual contradictions
- **perspective-shift**: When you need to understand MULTIPLE STAKEHOLDER viewpoints and lived experiences - empathy for different roles, breaking single-viewpoint blindness
- **Clear trigger**: Idea conflict vs people conflict

---

### Phase 3 Skills - "When to Use" Analysis (TESTED - Results)

#### **evidence-check** (Evidence quality assessment) ✅ TESTED

**Experimental Results** (Experiment 16):
- **Actual overlap with socratic**: ~70-75%
- **Verdict**: Keep both separate
- **Key distinction validated**: evidence-check evaluates THE EVIDENCE, socratic examines THE REASONING

**Clarity Assessment**: ✅ **GOOD - Orthogonal focus despite high overlap**
- **Different targets**: Evidence quality vs logical validity
- **Different questions**: "Is this source reliable?" vs "Does this logic hold?"
- **Different analysis**: Methodology, directness, recency vs assumptions, connections, implications
- **Sequential use**: Socratic first (clarify claims), then evidence-check (evaluate support)

**Verified "when to use" distinctions**:
- **evidence-check**: When you need to evaluate SOURCE QUALITY, assess methodology, check directness and recency of evidence supporting a claim
- **socratic**: When you need to test REASONING STRUCTURE, examine assumptions, explore implications, challenge logical connections
- **Clear trigger**: "Is this evidence reliable?" vs "Does the logic hold?"

---

#### **fallacy-detect** (Logical error pattern recognition) ✅ TESTED

**Experimental Results** (Experiment 17):
- **Actual overlap with logic-trace**: ~75%
- **Verdict**: Keep both separate
- **Key distinction validated**: fallacy-detect is PATTERN RECOGNITION (quick error scan), logic-trace is STRUCTURAL VALIDATION (deep logic review)

**Clarity Assessment**: ✅ **EXCELLENT - Like linter vs code review**
- **Different speeds**: Quick scan vs thorough validation
- **Different breadth**: Named fallacies vs complete reasoning structure
- **Different contexts**: Persuasive arguments/debates vs complex technical reasoning
- **Sequential use**: Fallacy-detect first (quick scan), then logic-trace if needed (deep validation)

**Verified "when to use" distinctions**:
- **fallacy-detect**: When analyzing PERSUASIVE arguments, debates, or rhetoric - quickly identify named logical errors and reasoning patterns
- **logic-trace**: When validating COMPLEX technical reasoning, proofs, or argument chains - step-by-step construction and validation
- **Clear trigger**: Quick error scan vs deep logic validation

---

#### **confidence-calibrate** (Certainty assessment) ✅ TESTED

**Experimental Results** (Experiment 18):
- **Actual overlap with knowledge-check**: ~65-70%
- **Verdict**: Keep both separate
- **Key distinction validated**: confidence-calibrate addresses FEELINGS of certainty, knowledge-check inventories ACTUAL information

**Clarity Assessment**: ✅ **EXCELLENT - Internal vs external focus**
- **Different assessments**: How sure should I feel? vs What do I need to know?
- **Different purposes**: Calibrating communication vs planning research
- **Different outputs**: Confidence levels matched to evidence vs lists of information gaps
- **Pipeline positions**: knowledge-check identifies gaps → confidence-calibrate assesses certainty given those gaps

**Verified "when to use" distinctions**:
- **confidence-calibrate**: When you need to match CERTAINTY to evidence for communication, avoid overconfidence, or express appropriate uncertainty
- **knowledge-check**: When you need to inventory INFORMATION GAPS, assess readiness to proceed, or plan what to research
- **Clear trigger**: "How sure should I sound?" vs "What do I need to know?"

---

#### **fork-detect** (Decision point identification) ✅ TESTED

**Experimental Results** (Experiment 19):
- **Actual overlap with cycle-detect**: ~60-70%
- **Verdict**: Keep both separate
- **Key distinction validated**: fork-detect is PREVENTIVE (before deciding), cycle-detect is REMEDIAL (after stuck)

**Clarity Assessment**: ✅ **EXCELLENT - Timing differentiation**
- **Different stages**: Approaching decision vs already stuck
- **Different purposes**: Recognize significance vs break loops
- **Different outputs**: Decision framing and consequences vs loop diagnosis and breaking strategies
- **Complementary**: fork-detect prevents cycles, cycle-detect breaks them

**Verified "when to use" distinctions**:
- **fork-detect**: When APPROACHING a decision point to recognize its significance, understand where paths diverge, and frame the choice properly
- **cycle-detect**: When ALREADY STUCK in repetitive thinking, going in circles, or unable to make progress despite effort
- **Clear trigger**: Before deciding vs after stuck

---

#### **metaphor-build** (Explanatory analogies) ✅ TESTED

**Experimental Results** (Experiment 20):
- **Actual overlap with domain-transfer**: ~65-70%
- **Verdict**: Keep both separate
- **Key distinction validated**: metaphor-build is COMMUNICATION tool, domain-transfer is PROBLEM-SOLVING technique

**Clarity Assessment**: ✅ **EXCELLENT - Different fundamental purposes**
- **Different goals**: Explain to enable understanding vs solve by borrowing patterns
- **Different audiences**: Teaching/communication vs innovation/solutions
- **Different outputs**: Mental models for explanation vs actionable patterns for implementation
- **When to choose is obvious**: Explaining vs solving

**Verified "when to use" distinctions**:
- **metaphor-build**: When you need to EXPLAIN complex concepts, teach, communicate, or create mental models for understanding
- **domain-transfer**: When you need to SOLVE problems by borrowing patterns from other fields, innovate, or challenge industry assumptions
- **Clear trigger**: Teaching vs problem-solving

---

### Summary: "When to Use" Clarity - All Testing Complete ✅

#### **COMPLETED - All Phase 2 and Phase 3 Tests**

**Total experiments**: 20 experiments covering 30 skills across 3 phases

**Overall findings on "when to use" clarity**:
- **19 out of 30 skills** (63%) have EXCELLENT clarity - clear triggers and distinct use cases
- **10 out of 30 skills** (33%) have GOOD clarity - some overlap but functional distinctions clear
- **1 out of 30 skills** (3%) requires MERGE due to subset relationship (assumption-reveal → socratic)

#### **Clarity Status by Skill Pair**

**EXCELLENT Clarity** (✅ Clear triggers, no confusion):
1. branch vs alternatives - Different problem-solving stages (10% overlap)
2. tree-explore vs graph-wander - Different exploration philosophies (35% overlap)
3. weigh-options vs leverage-find - Evaluation vs prioritization (40% overlap)
4. decompose vs root-cause - Breadth vs depth (45% overlap)
5. first-principles vs socratic - Generative vs analytical (60% overlap)
6. scenario-planning vs premortem - Multiple futures vs single failure (40-45% overlap)
7. feynman vs socratic - Build up vs dig down (35-40% overlap)
8. fallacy-detect vs logic-trace - Pattern scan vs structural validation (75% overlap)
9. confidence-calibrate vs knowledge-check - Certainty vs gaps (65-70% overlap)
10. fork-detect vs cycle-detect - Preventive vs remedial (60-70% overlap)
11. metaphor-build vs domain-transfer - Explain vs solve (65-70% overlap)

**GOOD Clarity** (⚠️ Some overlap but distinctions hold):
1. connect-dots vs theme-find - Relationships vs patterns (60% overlap)
   - **Distinction validated**: HOW things relate vs WHAT unifies
2. Creative trio: lateral-think vs domain-transfer vs random-input (40% overlap)
   - **Distinction validated**: Challenge vs study vs jolt
3. integrate vs connect-dots vs theme-find (60-75% overlap)
   - **Distinction validated**: Tensions vs relationships vs patterns
4. dialectic vs perspective-shift (65-70% overlap)
   - **Distinction validated**: Idea conflicts vs people conflicts
5. thinking-monitor vs cycle-detect (70% overlap)
   - **Distinction validated**: General metacognition vs loop-breaking
6. perspective-shift vs six-hats (75% overlap)
   - **Distinction validated**: Flexible vs structured framework
7. evidence-check vs socratic (70-75% overlap)
   - **Distinction validated**: Evidence quality vs reasoning validity

**MERGE Required** (⚠️ Subset relationship):
1. assumption-reveal → socratic (65% overlap)
   - **Reasoning**: Socratic does everything assumption-reveal does plus more

---

### Key Insights from "When to Use" Analysis

1. **High overlap doesn't prevent clarity**: 11 skill pairs with 60-75% overlap still have EXCELLENT "when to use" clarity because they serve different:
   - Cognitive modes (generative vs analytical, pattern vs structure)
   - Problem-solving stages (preventive vs remedial, solutions vs causes)
   - Purposes (communication vs problem-solving, learning vs challenging)
   - Timing (before vs after, approaching vs stuck)

2. **Clear triggers emerge from distinct dimensions**:
   - **Temporal**: fork-detect (before) vs cycle-detect (after)
   - **Directional**: feynman (build up) vs socratic (dig down)
   - **Scope**: scenario-planning (multiple) vs premortem (single)
   - **Purpose**: metaphor-build (explain) vs domain-transfer (solve)
   - **Speed**: fallacy-detect (quick) vs logic-trace (deep)

3. **Multiple synthesis modes all have clear use cases**: Even with 60-75% overlap:
   - integrate: When you have conflicting perspectives needing reconciliation
   - connect-dots: When you need to discover mechanical relationships
   - theme-find: When you need to identify and name recurring patterns

4. **Cognitive mode differentiation is powerful**: first-principles (generative) vs socratic (analytical) at 60% overlap have no confusion because the MODE is fundamentally different

---

### Required Documentation Updates

#### **Immediate - Update SKILL.md Files**

**Skills needing "when to use" enhancements** (2 pairs requiring clearer documentation):

1. **connect-dots and theme-find** (Currently: GOOD, Target: EXCELLENT)
   - Update connect-dots: Emphasize "discover HOW things relate mechanistically"
   - Update theme-find: Emphasize "identify WHAT unifies conceptually"
   - Add examples distinguishing system modeling vs pattern naming

2. **Creative trio: lateral-think, domain-transfer, random-input** (Currently: GOOD, Target: EXCELLENT)
   - Update lateral-think: Emphasize "challenge assumptions directly"
   - Update domain-transfer: Emphasize "study how other fields solve similar patterns"
   - Update random-input: Emphasize "jolt thinking with unrelated stimuli"
   - Add process distinction examples

#### **Already Excellent - No Changes Needed** (11 pairs)

These skills have validated clarity and require no documentation changes:
- branch vs alternatives
- tree-explore vs graph-wander
- weigh-options vs leverage-find
- decompose vs root-cause
- first-principles vs socratic
- scenario-planning vs premortem
- feynman vs socratic
- fallacy-detect vs logic-trace
- confidence-calibrate vs knowledge-check
- fork-detect vs cycle-detect
- metaphor-build vs domain-transfer

#### **Already Good - Minor Enhancements Only** (5 pairs)

These skills have good clarity, minor improvements could help but not critical:
- integrate, connect-dots, theme-find (already validated distinct)
- dialectic vs perspective-shift (already validated distinct)
- thinking-monitor vs cycle-detect (already validated distinct)
- perspective-shift vs six-hats (already validated distinct)
- evidence-check vs socratic (already validated distinct)

---

### Conclusion on "When to Use" Clarity

**Main Finding**: The thinkies plugin has remarkably clear "when to use" guidance. Of 30 skills tested:
- **63% have EXCELLENT clarity** with no confusion about when to choose them
- **33% have GOOD clarity** with validated functional distinctions
- **Only 2 skill pairs** need enhanced documentation (already at GOOD level)

**Core Insight**: Even skills with 60-75% overlap have clear "when to use" triggers because they differentiate on:
- **Cognitive mode** (generative vs analytical)
- **Timing** (preventive vs remedial)
- **Purpose** (explain vs solve)
- **Direction** (build up vs dig down)
- **Scope** (multiple vs single)
- **Speed** (quick scan vs deep validation)

**Recommendation**: Focus on two minor documentation enhancements (connect-dots/theme-find and creative trio). The rest of the suite has excellent clarity.

---

**Last Updated**: 2025-11-21
**Experiments Completed**: 20 experiments covering 30 skills across 3 phases
**Status**: ✅ ALL TESTING COMPLETE, "when to use" clarity analysis comprehensive
**Primary Recommendation**: Merge 1 skill (assumption-reveal → socratic), minor documentation improvements for 2 pairs, all other skills have validated clarity
