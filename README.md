# Prompt Ambition Expander

Five concise, installable [Agent Skills](https://agentskills.io/) for rewriting ordinary tasks into more ambitious, executable prompts. They **expand prompts; they do not execute the task**.

| Skill | Purpose |
| --- | --- |
| `ambition-expander` | Combine the highest-leverage improvements from all four dimensions. |
| `altitude-expander` | Aim at the underlying outcome instead of the assumed deliverable. |
| `depth-expander` | Demand expert methods, primary evidence, and independent verification. |
| `range-expander` | Apply useful methods from unexpected disciplines. |
| `speed-expander` | Reduce elapsed time by redesigning execution, not lowering quality. |

## Install

Install interactively and choose skills/agents:

```sh
npx skills add davidjbeveridge/prompt-ambition-expander
```

Install the combined skill only:

```sh
npx skills add davidjbeveridge/prompt-ambition-expander --skill ambition-expander
```

List available skills without installing:

```sh
npx skills add davidjbeveridge/prompt-ambition-expander --list
```

## Use

Ask your skill-aware agent, for example:

> Use the ambition-expander to rewrite: "Build a dashboard for monthly customer churn."

Or choose a dimension:

> Use depth-expander to rewrite this task with expert-grade methods: "Investigate why users churn."

Each skill produces a standalone, copy-ready prompt. It preserves the user's intent, explicit constraints, and authorization boundaries. It must not invent available tools, data, permissions, or verified conclusions. Expansion is **not** synonymous with adding scope or length.

The combined skill adds a short reframing and up to five key upgrades; individual skills output only the expanded prompt.

## Sources and attribution

**Original framework:** Felix Rieseberg, **["How to be more ambitious: A tutorial for humans with models"](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/)** (October 13, 2026). The article introduces the four dimensions—**Speed, Altitude, Depth, Range**—and publishes an example **Depth** expansion prompt. These skills are independent, condensed adaptations of the ideas, **not** verbatim reproductions of that prompt. Rieseberg intentionally does not develop Speed; this repository's Speed skill is an extrapolation.

**Compression inspiration:** Julius Brussee, [Caveman](https://github.com/JuliusBrussee/caveman). The concise wording follows Caveman-style principles; the prompts were manually written, not generated or validated by Caveman's CLI. No affiliation or endorsement is implied.
