# Prompt Ambition Expander

Five installable [Agent Skills](https://agentskills.io/). `ambition-expander` is a **director**: it selects and invokes the relevant specialist skills, synthesizes one prompt, and optionally **executes** the expanded task.

| Skill | Purpose |
| --- | --- |
| `ambition-expander` | Route to specialists, merge improvements, optionally execute. |
| `altitude-expander` | Target the underlying outcome, not just a deliverable. |
| `depth-expander` | Expert methods, primary evidence, independent verification. |
| `range-expander` | Transfer methods from unexpected disciplines. |
| `speed-expander` | Cut elapsed time through automation, parallelism, and early tests. |

## Install

Install **all five skills** so the director can delegate:

```sh
npx skills add davidjbeveridge/prompt-ambition-expander
```

Select all five when the installer asks which skills to install. A director-only installation cannot invoke missing specialists. Individual skills also work standalone.

## Usage

**Expand only (default):**

> Use ambition-expander to expand: "Build a dashboard showing monthly customer churn."

**Expand and execute (opt in):**

> Use ambition-expander to expand **and execute**: "Research the churn drivers, build the dashboard, and verify the metrics."

**Override routing:**

> Use ambition-expander with **depth** and **speed** only, then execute: "Fix our flaky CI tests."

The director scores each dimension against the task, invokes the relevant installed skill(s), and merges their recommendations. It normally calls 1–3 specialists; a broad task may warrant all four. The specialists return concise upgrades in director mode and never execute the user's task themselves.

Default mode outputs a copy-ready prompt. Execute mode **expands internally and carries out the task using available tools**, then reports what was verified and what remains blocked. It does not claim work was completed merely because a plan was produced.

**Host compatibility:** Skill-to-skill invocation differs across agents. The director uses native skill/subagent calls when available. Otherwise it reads the selected specialist's actual `SKILL.md` and applies it in a separate pass. It must disclose missing skills or unsupported invocation rather than pretending delegation succeeded. Execute mode still obeys tool access, permissions, safety requirements, and user-defined constraints. Reframing a goal never grants new authority.

## Sources and attribution

**Original framework:** Felix Rieseberg, **["How to be more ambitious: A tutorial for humans with models"](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/)**. The article describes **Speed, Altitude, Depth, Range** and supplies a free **Depth** expansion prompt. These skills are condensed independent adaptations, not verbatim reproductions. The Speed skill expands on an idea Rieseberg leaves unexplored.

**Compression inspiration:** Julius Brussee, [Caveman](https://github.com/JuliusBrussee/caveman). The wording follows Caveman-style concision; these skills were manually written, not produced or benchmarked by Caveman's CLI. No affiliation or endorsement implied.
