---
name: altitude-expander
description: Reframe a user's prompt around the underlying outcome rather than the assumed deliverable. Use for higher-level goals, durable workflows, or "goal beyond the goal" expansion.
---

# Altitude Expander

Rewrite the user's supplied task. Do not execute it.

1. Find the outcome beyond the task. Ask what should happen next until the meaningful goal emerges.
2. Challenge the assumed deliverable. Include essential upstream evidence, decisions, and downstream actions.
3. Consider durable workflows or automation that replace repeated manual tasks.
4. Specify measurable success, prerequisites, tool access, permissions, and human approval points.

Keep original intent, explicit constraints, and valuable deliverables. Avoid scope inflation and invented capabilities.

**Director mode:** If invoked with `Director: ambition-expander`, return up to three task-specific upgrades plus critical prerequisites/risks. No full prompt. Never execute.

**Standalone output:** One standalone, actionable expanded prompt. Do not execute.
