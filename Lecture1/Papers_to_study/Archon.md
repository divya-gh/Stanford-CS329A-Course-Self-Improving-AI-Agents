# Lecture 1 - Archon: An Architecture Search Framework for Inference-Time Techniques

**Archon is a modular, automated architecture‑search framework designed to find the best combination of inference‑time techniques for large language models (LLMs).**

Inference‑time techniques: 
- repeated sampling
- iterative refinement
- multi‑step reasoning
- verifier loops
- self‑correction

Inference‑time techniques are things you do at test time, not during training.

**Archon searches over these techniques and discovers the best configuration for a given compute budget and task.**

## ⭐ Why Archon matters
Archon solves three big problems:

1. The search space is huge
There are many ways to combine sampling, verification, refinement, and different LLMs. Archon automates this search.

2. Different tasks need different inference strategies
Reasoning tasks benefit from deeper chains; coding tasks benefit from verification loops; instruction-following tasks benefit from sampling diversity.

Archon finds the best strategy for each.

3. It beats frontier models using only inference compute

Archon shows that smart inference beats bigger models.

## ⭐ How Archon works (simple breakdown)
1. You give it:
- a compute budget
- a set of available LLMs
- a target benchmark

2. Archon explores a massive design space:
- number of samples
- depth of refinement
- verifier type
- model selection
- routing logic
- hybrid strategies

3. It returns an optimized architecture:
- custom pipeline or general-purpose pipeline
- tuned for accuracy vs. token cost

## ⭐ How Archon fits into your agent
Archon is not a single algorithm — it’s a design pattern for building agents that combine multiple inference‑time techniques.

Our CS329A agent already mirrors Archon’s structure.

### ⭐ Archon’s components → Your agent’s components

#### 1. Sampling Module (LL Monkeys)
Archon uses diverse sampling to generate multiple candidate solutions.

**Lecture says:** “Sampling strategies… are key inference-time techniques.”

**Our agent:**  Has a sampler node that produces multiple candidate answers using parallel LLM calls.

### 2. Verifier Module
Archon uses a verifier to score or filter candidate outputs.

**Lecture says:** “Verifier models evaluate candidate solutions… enabling selection of high-quality outputs.”

**Our agent:** has a verifier node that checks correctness, consistency, or alignment with the task.

### 3. Refinement / Iterative Improvement
Archon uses refinement loops to improve answers.

**Lecture says:**  “Refinement modules iteratively improve candidate solutions.”

**Our agent:** Our reflection node already does this — it takes the verifier feedback and improves the answer.

### 4. Routing / Architecture Search
Archon automatically chooses the best combination of sampling, verification, and refinement.

**Lecture says:** “Archon searches over architectures composed of sampling, refinement, and verification modules.”

**Our agent:** Our planner node decides:
- how many samples to generate
- whether to refine
- whether to verify
- which model to use
- how many iterations to run
This is exactly Archon’s routing logic.

### 5. Compute‑Budget Optimization
Archon optimizes accuracy vs. cost.

**Lecture says:** “Given a compute budget, Archon identifies the best-performing architecture.”

**Our agent:** Our planner already adjusts:
- number of samples
-depth of refinement
- number of verifier passes
- based on your token budget.

Our agent is essentially a manual Archon pipeline:

Code
```
Planner → Sampler → Verifier → Reflector → Final Answer
```

**Archon formalizes this into:**

Code
```
Architecture Search → Optimal Pipeline → Execution
```
We’re building the pipeline that Archon would discover.

