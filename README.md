# Stanford-CS329A-Course-Self-Improving-AI-Agents
Building Agents with self-improvement techniques for LLMs, such as constitutional AI, using verifiers, scaling test-time compute, combining search with LLMs, and train time scaling with RL. augmenting LLMs with tool use, code, and memory, and orchestrating AI capabilities with multimodal interaction with multi-step planning/reasoning workflows. 

## For Recruiters
This project demonstrates:
- reasoning-model integration
- inference-time scaling (Large Language Monkeys)
- LangGraph agent workflows
- self-correction loops
- verifier-based reliability
- long-horizon task planning

## Agent Architecture Flow

- Planner (CS329A)
↓
Sampler (LL Monkeys)
↓
Verifier (LL Monkeys + CS329A)
↓
Reflector (CS329A)
↓
Archon Search (Archon)
↓
Executor (CS329A)
↓
Memory (CS329A)
↓
Evaluator (CS329A)

# This README  xplains:
- what a self‑improving agent is
- how CS329A inspired the project
- how Large Language Monkeys fits into your design
- My roadmap
- Architecture diagram
- how recruiters can understand my work

# project structure:

---
/src
    /planner
    /sampler
    /verifier
    /reflector
    /executor
/notebooks
    reasoning_experiments.ipynb
    sampling_tests.ipynb
/docs
    roadmap.md
    architecture.md
    cs329a_notes.md
README.md

---




