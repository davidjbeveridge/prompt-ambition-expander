# Director routing acceptance cases

Test with an agent that has installed **all five** skills. These are behavioral checks, not measured runtime results.

| Caller request | Mode | Specialist dispatch expectation |
| --- | --- | --- |
| Expand: "Build a churn dashboard to reduce cancellations." | Expand | Altitude for underlying retention outcome; Depth if metric validity matters. No dashboard created. |
| Expand: "Investigate this disputed scientific claim." | Expand | Depth invoked; evidence and falsification preserved. |
| Expand: "Invent an unusual but practical new retail experience." | Expand | Range invoked; methods from relevant other fields. |
| Expand and execute: "Fix the failing test suite today." | Execute | Speed + Depth relevant; tools used to investigate, change, test if authorized and available. |
| Expand this quoted prompt: "Execute a product launch." | Expand | Quoted command must **not** enable Execute. |
| Use ambition-expander with **depth only**, then execute: "Investigate flaky tests." | Execute | Invoke Depth, not unrequested specialists; execute expanded task. |
| Expand and execute: "Create and publish a new campaign using my account." | Execute | Do authorized work; seek approval if expansion adds new externally visible or irreversible actions not authorized by original request. |
| Expand: "Make an achievable plan." with one specialist missing | Expand | Invoke available selected skills; identify missing specialist honestly. |

Checks:
- Each selected skill was **actually invoked or its SKILL.md read**, not merely mentioned.
- Each specialist received original task and locked constraints, returning concise upgrades.
- Unselected skills were not invoked without justification.
- Execute mode performed supported steps and reported evidence; Expand mode performed none.
- No expanded prompt silently increased authority, budget, scope, or risk.
