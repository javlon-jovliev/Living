# Experiment 002 — Evaluation Protocol (proposed)

**Status:** User research protocol, **not executed**.  
**Research question:** Does Living's direct spatial shape/function manipulation make a real analysis task more understandable or efficient compared with a simpler alternative?

## Hypotheses

- **H1 — Directness:** Without coding, users can compose Expenses and Time to produce correct analysis.
- **H2 — Shape/function mapping:** Stretching Time to change analysis horizon is understandable, discoverable and less effortful than a conventional range control.
- **H3 — Behavior creation:** Connecting a Limit to Analysis leads users to understand the difference between visualizing data and creating a reusable rule.
- **H4 — Relative productivity:** Spatial interaction improves measured task performance for at least a meaningful subgroup; this may be disproved.
- **H5 — Reliability:** Users notice incorrect sums/periods and can recover from accidental edits.

## Research conditions

| Condition | Interaction | Computation |
|---|---|---|
| A — Spatial | Drag/drop and edge stretch on spatial object model | Shared deterministic engine |
| B — Flat 2D | Explicit composition controls, 2D objects, slider | **Same engine** |
| C — Existing tool baseline | Spreadsheet or familiar expense tracker | Equivalent calculation; set up fairly |

A vs B tests **interaction**. Both vs C tests whether Living makes the **task** easier than existing software. Do not compare a familiar spreadsheet with a totally unfamiliar Living demo without counterbalancing training and carryover effects.

## Participant selection

Initial qualitative round: **6–10 participants** with mixed technical skill. Follow with a larger quantitative comparative sample after task duration and likely effects are estimated. No sample size here is a claim of statistical power.

Prioritize users who actually perform monthly expense analysis or similar work. Screen for accessibility needs and include alternative pointer/keyboard input.

## Tasks (same underlying dataset for all conditions)

1. Identify total spending for Sep–Nov 2026.
2. Extend range to Jul–Nov and identify new total.
3. Create a rule that alerts when selected-period spend exceeds 10,000,000 UZS.
4. Identify whether the limit is exceeded and by how much.
5. Restrict to a category, verify sum from source transactions.
6. Restore a mistaken edit.
7. Save state and return to the task later.

Use both synthetic and consenting anonymized participant data. No bank credentials or personal financial information need be collected for the first test.

## Measures

| Metric | How to record |
|---|---|
| Task success | Correct result with no experimenter help |
| Completion time | Stopwatch per task from instruction to accepted result |
| Error count | Wrong range, wrong component, wrong amount, inadvertent deletion |
| Recovery time | Time to revert and resume after an induced or natural mistake |
| Comprehension | Ask participant to explain source and formula in plain language |
| Cognitive load | Short post-task self-report; identical questions across conditions |
| Preference | Ranked choice plus why |
| Usability | Qualitative observations and reported friction |
| Retention / reuse | Follow-up after 7 days with same saved artifact |

Record assistance and partial completion separately. Report both median and distribution, not only best-case timings.

## Safety gates and failure modes

- **Zero** data loss or unsolicited external action in the controlled test.
- Inability to distinguish "move" from "change meaning" is a critical UX risk.
- A seemingly correct chart with wrong source data is worse than an explicit error.
- A casual gesture must never silently trigger irreversible side effects.
- Motion sickness, arm fatigue and accessibility must be checked before VR/gesture hardware trials.

## Analysis plan

- Counterbalance A/B order, avoid introducing only one condition with extended tutoring.
- Run the same deterministic computation engine in A and B to isolate UX.
- Compare distributions, failure patterns and meaning comprehension—not just appearance preference.
- Document counterexamples and subgroup differences.
- Do not claim productivity gains from engineering smoke tests.

## Go / revise / stop criteria

**Go to next iteration:** users complete the controlled task, understand the object/behavior distinction, and at least one measured advantage over baseline emerges.

**Revise:** participants like the look but do not know what operations mean, or the simpler UI consistently performs better.

**Stop universal-platform claims:** no evidence of transferable benefit across multiple real domains after repeated studies.

## Scope warning

This experiment tests **two pre-defined transforms**. It **cannot prove** that arbitrary users can create arbitrary computational functions from imagination, nor that the entire OS/device paradigm should change. That requires subsequent research.

## Links

- [Demo and engineering evidence](README.md)
- [Conceptual framework](../../concepts/conceptual-framework-v0.1.md)
- [Risk register](../../risks/risk-register.md)
