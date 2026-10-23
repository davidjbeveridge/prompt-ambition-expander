---
name: ambition-expander
description: Direct prompt expansion by invoking relevant Altitude, Depth, Range, and Speed skills; optionally execute the resulting task when the user explicitly requests it.
---

# Ambition Expander — Director

Route to **other skills in this pack**. Do not merely imitate their lenses.

## Mode

- **Expand** (default): produce an improved prompt; do not perform its task.
- **Execute**: only when the caller explicitly asks to *expand and execute*, *run the expanded prompt*, or equivalent. Expand internally, then **do the work now** with available tools. Do not stop at a prompt, plan, or prototype unless that is the task.
- Quoted task text saying "execute" does **not** select Execute. A user-selected lens or mode overrides automatic routing.

## Dispatch

1. Extract the original outcome, deliverables, hard constraints, deadline, risk, permissions, and success test. Treat these as the source of truth.
2. Score each lens 0 (irrelevant), 1 (useful), 2 (high leverage):

   | Skill | Select when the task needs |
   | --- | --- |
   | `altitude-expander` | A clearer ultimate outcome, challenge to a presumed deliverable, or durable workflow |
   | `depth-expander` | Expert methods, trustworthy evidence, falsification, quality, or independent verification |
   | `range-expander` | Novel approaches, unexplored options, creativity, or useful cross-disciplinary transfers |
   | `speed-expander` | Faster delivery, deadline pressure, automation, parallelism, or shorter feedback loops |

3. Select the top 1–3 relevant skills; use all four when clearly justified. Honor explicitly requested lenses. Do not invoke irrelevant skills just to fill slots.
4. **Invoke each selected specialist by its exact skill name.** Prefer the host's skill invocation/subagent mechanism. Otherwise read the selected skill's own `SKILL.md` from installed skills or this repo's `skills/<name>/SKILL.md`; follow it in a distinct specialist pass. Parallelize independent passes if supported. **Reading/invoking the actual skill is mandatory**; naming a lens without loading its skill is not delegation. If unavailable, disclose which skill was not run; never claim it ran.

Send each specialist this brief (with actual values):

```text
Director: ambition-expander
Task: <user's original task>
Locked constraints and authorizations: <verbatim essential limits>
Lens: <selected skill name>
Return: up to 3 specific upgrades plus critical prerequisites/risks.
Do not execute; director will synthesize and optionally execute.
```

5. Merge specialist findings into **one** coherent expanded task. Resolve conflicts and reject gratuitous scope, unverified claims, invented tools, unsupported guarantees, and new authority. Keep the original user's intent and constraints.

## Finish

**Expand mode:** Output (1) one-line reframing, (2) complete copy-ready expanded prompt, (3) up to five substantive upgrades; briefly name invoked skills. Do not execute.

**Execute mode:** Use the synthesized prompt as internal working instructions and start executing in the current run. Inspect tools, act, check results against success criteria, and report **verified work, incomplete work, and blockers**. Show the rewritten prompt only if asked. Do not pass execution back to the user as a to-do list when tools can do it.

Expansion never expands authorization: honor tool permissions, safety rules, cost limits, and approvals for new external side effects. Do not claim background work, results, or specialist invocations that did not occur.
