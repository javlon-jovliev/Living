# Experiment 002 — Shape → Function

**Status:** Working *research prototype*, not validated Living OS / final UI.  
**Date:** 2026-11-12  
**Branch:** `experiment/002-shape-function`  
**Purpose:** test one chain: **human action → object transformation → verifiable computation**.

## What is being tested?

An ordinary person should be able to create a new useful computation **inside the workspace**, with no editor, programming syntax, or mandatory AI chat.

One controlled real-world task: **analyse spending and add a spending-limit monitor**.

Two ways to interact with the **same state and computation engine**:

- **A — Spatial:** movable expense, time, and limit objects; object overlap causes a pre-defined composition; direct stretching changes time horizon.
- **B — Flat 2D:** predictable 2D workspace, standard range input and explicit actions for the same compositions.

**Important:** The 2D version is an interface comparison, **not** a conventional spreadsheet baseline. A separate spreadsheet baseline must be tested with real participants.

## Run

1. Download [demo.html](demo.html).
2. Open it in a modern desktop browser. No server, external scripts, AI API, camera or account required.
3. Start with the synthetic UZS sample dataset or use your own CSV.
4. Switch between “Fazoviy” and “Sodda 2D” on top.
5. Source code is a self-contained, dependency-free HTML demo so it can be opened offline.

**CSV format:** `date,category,amount`, e.g. `2026-11-03,Transport,250000`; positive amounts in UZS. Imported CSV **replaces** the previous transactions only after confirmation; undo remains available during the session. Invalid rows are rejected. Hard limit: 5000 rows, file ≤1 MB.

Browser stores data in `localStorage` for this prototype. On shared devices, other people using the same browser profile may access it. Use synthetic/non-sensitive data; local storage is not encrypted and is not suitable for banking, health or confidential work. Clearing browser site data removes saved state. Export JSON before doing so.

## Exact user journey

1. **Expenses + Time → Time-Based Analysis.** Drag the expenses object onto time in Spatial mode, or use “Birlashtir” (accessible alternative). The engine creates a new analysis object with totals by month.
2. **Stretch Time.** Drag the right edge handle of time to include more/fewer months. In Flat mode use the period slider. The total and chart **recompute from source transactions**.
3. **Limit + Analysis → Spending Guard.** Drag Limit onto Analysis or use “Chegarani bog‘la”. The resulting object now checks whether spending exceeds the specified **total period limit**, instead of merely showing a graph.
4. Change limit or category, inspect the explanation and lineage, export analysis JSON.
5. Add a transaction / import CSV, undo, reload, switch UI mode. Both modes share the same model.

The object composition rules here are explicit:
- `compose(Expenses, Time) -> Analysis`
- `compose(Limit, Analysis) -> SpendingGuard`

**No claim of universal semantic chemistry:** these two recipes are hard-coded rules in the prototype, not an open-ended capability generator.

## Implementation boundaries

- Local, deterministic calculations; sum, mean, monthly grouping, threshold checking.
- Sample data for July–November 2026, all UZS.
- No real banking/email service integrations.
- No freeform 3D clay deformation, skeletal hands, AR, voice, LLM, or generic behavior programming.
- Spatial canvas is a restrained 2.5D/CSS composition **experiment**, not a reproduction of Claude's v4 Ring Desk.
- No true OS-level functionality.
- Undo is stored in current page session; main state persists in browser storage.
- No team sync, audited permission boundary, encrypted local DB, or hardened security model.

These restrictions are intentional: isolate functional composition and inspect real computation before adding gesture/hardware complexity.

## Engineering smoke-test evidence (2026-11-12)

Automated interaction in Chromium/Playwright on the local HTML was executed using a DOM test harness:
- expenses dragged to time → composition state changed to `true`;
- 3-month sample total `10,380,000 UZS` (Sep–Nov 2026);
- stretching Time to 5 months → total `17,400,000 UZS` (Jul–Nov 2026);
- switching spatial ↔ flat → same computed total;
- adding Limit → threshold assessment recomputes;
- changing threshold → correct over/under behavior;
- re-opening document with a preserved local-storage payload → same saved model;
- adding sample transaction changed records 20 → 21; undo restored 20;
- valid CSV parsed; invalid date rejected;
- no JavaScript exceptions in final harness run.

**Qualification:** The managed test environment blocked normal file/HTTP browser navigation, so the test used `page.set_content()` with a simulated browser localStorage backend. This verifies serialization and restore logic under the harness, **not a real browser-origin persistence audit**. Pointer interaction and arithmetic ran in Chromium. Visual screenshots were inspected. User studies, real-world dataset tests, performance, accessibility and independent browsers remain untested.

Detailed protocol: [evaluation-protocol.md](evaluation-protocol.md).

## What would count as real evidence?

A controlled task study with actual users, not just an impressive visual effect:
- can participants finish a genuinely useful spending task?
- do they understand where numbers came from?
- does physical manipulation improve time, error rate and confidence versus the 2D control?
- are objects reused after a week?
- do participants prefer shape/function mapping or find it confusing?

**Negative results must be recorded.** If Spatial adds complexity without benefit, the result supports revising the interaction metaphor—not hiding the finding.

## Relation to Living vision

- [Living Vision](../../VISION.md)
- [Conceptual Framework v0.1](../../concepts/conceptual-framework-v0.1.md)
- [Living Object Model](../../concepts/living-object-model.md)
- [Interaction Principles](../../design/interaction-principles.md)
- [Experiment 001](../001-object-composition.md)

*This is a falsifiable test artifact. It does not establish Living's market demand, future hardware implications or universal feasibility.*
