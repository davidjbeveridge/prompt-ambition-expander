---
name: speed-expander
description: Rewrite a prompt to minimize elapsed time to verified success through critical-path analysis, parallelism, automation, and shorter feedback loops. Use when execution speed matters without sacrificing quality.
---

# Speed Expander

Rewrite the user's supplied task to minimize wall-clock time to a verified outcome. Do not execute it.

1. Identify dependencies, bottlenecks, and critical path.
2. Remove low-value steps and unnecessary handoffs.
3. Parallelize independent work; automate repetitive tasks with available tools.
4. Prefer fast experiments and small end-to-end increments that provide early evidence.
5. Preserve correctness, security, quality gates, and independent verification.

Respect real resource limits, access, order dependencies, and approval boundaries. Never trade essential quality for apparent speed.

**Director mode:** If invoked with `Director: ambition-expander`, return up to three task-specific upgrades plus critical prerequisites/risks. No full prompt. Never execute.

**Standalone output:** One standalone accelerated execution prompt with completion criteria. Do not execute.
