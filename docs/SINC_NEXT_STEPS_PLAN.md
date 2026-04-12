# Sinc — Next Steps Plan (from current notes)

## Why this plan exists

The current notes are unusually coherent on **principles** and broad **product direction**, but still leave execution ambiguity around:

1. which loop to prove first,
2. which assumptions to test before building social layers, and
3. what metrics define success vs. concept drift.

This document translates the existing memos into a practical sequence.

---

## What is already clear (do not re-debate)

From the product memo, working notes, UX notes, and synthesis docs, the non-negotiables are:

- **Finite, domain-bounded, finishable lists** are the core product object.
- **Completion** is a primary UX outcome, not a cosmetic state.
- **Search before recommendation** in v1.
- **Ledger-not-loop** behavior as default.
- **Borrowed Taste is explicit, narrow, and reversible** (one person, one domain).
- **Manual routing / Human API** is first-class signal capture.
- **Negative curation** (skip/pass/redundant/not-worth-it) should become a strong signal family.

Implication: v1 should focus on proving a tight personal loop with light trust overlays, not broad social mechanics.

---

## Key unresolved decisions to settle in the next 2–4 weeks

### Decision A — What exact v1 loop is “done enough”?

Working definition:

1. user selects domains,
2. receives non-empty initial lists,
3. processes items with explicit judgments,
4. reaches completion state,
5. adds/reroutes at least one item,
6. starts next list by explicit choice.

**Exit criterion:** users can complete this loop repeatedly without needing infinite fallback scrolling.

### Decision B — What minimum signal set ships in v1?

Recommended v1 signals:

- save
- dismiss
- wrong fit
- already seen
- finish/abandon
- re-rank move (implicit comparative signal)

Defer rich warrants to v1.1 unless implementation is trivial.

### Decision C — How strict is shelf cardinality at launch?

Recommended launch constraint:

- healthy: 4–7 active shelves,
- soft warning at 8,
- hard cap at 12.

This prevents read-later sprawl and forces ontology discipline.

---

## Suggested execution roadmap

## Phase 0 (Now): Product spec consolidation (1 week)

### Goals
- Collapse all active notes into one implementation-ready spec.
- Remove contradictory language across memos.

### Deliverables
- Canonical v1 PRD (scope, non-goals, acceptance criteria).
- State machine for item lifecycle:
  - incoming -> placed -> in-list -> processed -> archived/refill candidate.
- State machine for list lifecycle:
  - active -> stalled (optional) -> completed -> refill decision.
- Borrowed Taste v1 contract (one-hop, one-domain, on/off).

### Risks avoided
- Building aesthetic concepts (glyphs, communication layer) before core loop quality exists.

---

## Phase 1: Build and instrument the core loop (3–5 weeks)

### Build priority
1. Domain creation + anti-blank onboarding.
2. Finite list generation with visible cardinality/progress.
3. Item judgment actions + greying behavior.
4. Completion panel with explicit next-step choices.
5. Manual ingestion/routing (paste + basic share-in).
6. Basic public list pages discoverable via search only.

### Instrumentation to add from day 1
- list completion rate by domain,
- median time-to-first-completion,
- % users who add one item post-completion,
- % items left unresolved > 7 days,
- distribution of judgment actions (save vs dismiss vs wrong fit, etc.),
- borrowed taste activation rate and reversal rate.

### Success bar
- At least one domain where users repeatedly complete lists.
- Post-completion ownership action occurs in meaningful share of sessions.

---

## Phase 2: Introduce bounded “support under load” (2–4 weeks)

Only start after Phase 1 loop health is proven.

### Features
- Stalled-list detection (simple heuristic, transparent).
- Ask-for-triage mode (explicit user-invoked first).
- Pass/negative curation with short warrant templates.

### Constraints
- No mass broadcasting.
- No auto-routing into others’ attention.
- No generalized reputation scoring.

### Success bar
- stalled lists recover at higher rate than control,
- users report lower backlog anxiety,
- no emergence of feed-like compulsive behavior.

---

## Phase 3: Evaluate wedge adjacency (parallel discovery track)

Use lightweight prototypes/interviews to choose one strategic wedge to co-develop with Sinc:

- **Clerk-style inferred taste alignment** (best challenge/complement to explicit trust),
- **Circuit small-group loop** (highest buildability as social wedge),
- **Gutcheck extension** (lowest friction ambient utility).

Pick exactly one to avoid dilution.

---

## Experiments to run before committing to v1.5 surfaces

1. **Completion psychology test**
   - Does explicit completion + reflection increase return quality vs. silent list rollover?

2. **Negative curation utility test**
   - Are “pass/redundant/not-worth-it” signals more predictive of satisfaction than saves alone?

3. **Borrowed Taste trust test**
   - Does one-domain overlay improve perceived quality without reducing agency?

4. **No-unsorted-inbox enforcement test**
   - Does strict resolve/route/discard reduce guilt pile formation without unacceptable friction?

---

## Operating principles for roadmap decisions

Use these as hard filters for feature acceptance:

1. Does this preserve finishability?
2. Does it keep continuation user-chosen?
3. Does it keep domains semantically narrow?
4. Is borrowed influence always visible and reversible?
5. Does it avoid turning measurement into amplification?
6. Does it improve judgment quality (not just engagement volume)?

If a feature fails two or more filters, defer.

---

## What to explicitly defer (to prevent scope drift)

- Full guild/reputation systems,
- market/token/protocol mechanics,
- global trust scoring,
- heavy public messaging,
- whole-profile social growth surfaces,
- ornate identity layers (glyph doctrine) before core-loop retention is healthy.

---

## Recommended immediate next 5 actions (this week)

1. Draft canonical v1 PRD and lock non-goals.
2. Define core event taxonomy for analytics.
3. Design list + item lifecycle schemas.
4. Prototype completion panel and resolve-item flow in low-fidelity.
5. Recruit 10–15 design partners across two target segments:
   - taste-rich but platform-fatigued users,
   - users who already manually share links with friends.

