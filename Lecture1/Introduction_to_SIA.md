# Lecture 1 introduces the major building blocks to learn:
## core idea:
**AI agents that continuously improve themselves through interaction with themselves and the environment.**
#### This means:
- They evaluate their own outputs
- They correct their mistakes
- They learn from feedback
- They improve without retraining
- They use tools, memory, and planning
- They operate over long tasks
This is the foundation of your agent.

## The major categories of self‑improvement

### A. Self‑Improvement Techniques
- Constitutional AI
- Verifiers
- Scaling test‑time compute
- Search + LLMs
- RL-based training improvements or train-time scaling

### B. Agent Capabilities
- Tool use
- Code execution
- Memory augmentation
- Multimodal interaction
- Planning
- Long-horizon reasoning and planning (Multi-step reasoning, Planning workflows)


### C. Evaluation Frameworks :Robust evaluation frameworks and Long-horizon task measurement
- How to measure agent improvement
- How to test long tasks
- How to benchmark reasoning
These are the exact components we will build in our GitHub project.


## 🧩 3. The Agent Loop (The Most Important Part)
Lecture 1 implicitly defines the agent loop we’ll implement:
- Plan
- Act / Use Tools
- Verify
- Reflect
- Improve
- Store Memory
- Repeat
This loop is the backbone of every self‑improving agent.