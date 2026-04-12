# Sinc — Next Steps Plan v0.2

## Why this plan exists
The current Sinc notes are coherent on principles and direction, but still leave practical ambiguity around:

1. which loop to prove first,
2. which assumptions to test before adding social complexity,
3. what success looks like before the product starts drifting into concept theater.

This document converts the existing memos into a practical sequence.

---

## What is already clear (do not re-debate)
These points appear stable across the current memo set and should be treated as working constraints for v1.

- Finite, domain-bounded, finishable lists are the core product object.
- Completion is a primary UX outcome, not a cosmetic state.
- Search before recommendation in v1.
- Ledger-not-loop behavior as default.
- Borrowed Taste, if present in v1, must be explicit, narrow, reversible, and secondary to proving the personal loop.
- Manual routing / Human API is first-class signal capture.
- Negative curation (skip / pass / redundant / not-worth-it) is likely a high-value signal family.

Implication:
v1 should prove a tight personal loop with light, optional trust overlays — not broad social mechanics.

---

## Main decisions to settle in the next 2–4 weeks

### Decision A — What exact v1 loop counts as “done enough”?
Working definition:

1. user selects domains,
2. receives non-empty initial lists,
3. processes items with explicit judgments,
4. reaches a completion state,
5. adds or reroutes at least one item,
6. starts the next list by explicit choice.

Exit criterion:
users can repeat this loop without needing infinite fallback browsing.

### Decision B — What minimum signal set ships in v1?
Recommended v1 signals:

- save
- dismiss
- wrong fit
- already seen
- finish / abandon
- re-rank move (implicit comparative signal)

Defer richer warrants to v1.1 unless implementation is trivial.

### Decision C — How strict is shelf cardinality at launch?
Recommended stance:
launch with limits strong enough to prevent read-later sprawl.

A working constraint may look like:
- healthy range: 4–7 active shelves
- soft warning beyond that
- hard cap before the product turns into backlog storage

Exact numbers should be finalized through onboarding and usability testing, not treated as sacred in advance.

---

## Suggested execution roadmap

## Phase 0 — Consolidate the spec (1 week)
### Goals
- Collapse active notes into one implementation-ready spec.
- Remove contradictory language across memos.
- lock the product around one loop before building symbolic or social excess.

### Deliverables
- canonical v1 PRD (scope, non-goals, acceptance criteria)
- item lifecycle state machine:
  - incoming -> placed -> in-list -> processed -> archived / refill candidate
- list lifecycle state machine:
  - active -> stalled (optional) -> completed -> refill decision
- Borrowed Taste v1 contract:
  - one person
  - one domain
  - explicit on/off
  - easy reversal

### Risks avoided
- building ornamental identity/social layers before loop quality exists
- confusing product philosophy with implementation readiness

---

## Phase 1 — Build and instrument the core loop (3–5 weeks)
### Build priority
1. domain creation + anti-blank onboarding
2. finite list generation with visible cardinality/progress
3. item judgment actions + greying behavior
4. completion panel with explicit next-step choices
5. manual ingestion / routing (paste + basic share-in)
6. optionally, basic public list pages discoverable by search only if they do not slow the core loop

### Instrumentation from day 1
- list completion rate by domain
- median time to first completion
- % of users who complete a list in the same domain more than once
- % of users who add one item after completion
- % of items unresolved after 7 days
- distribution of judgment actions
- borrowed taste activation and reversal rate (if shipped)

### Phase 1 north star
Repeat completion rate.

If users are not completing lists and then voluntarily starting another, the product is not yet working.

### Success bar
- at least one domain where users repeatedly complete lists
- meaningful share of sessions include a post-completion ownership action
- no obvious drift toward backlog-hoarding behavior

---

## Phase 2 — Add bounded support under load (2–4 weeks)
Only begin after Phase 1 loop health is clearly proven.

### Features
- user-invoked ask-for-triage mode
- simple stalled-list support
- pass / negative curation with short warrant templates

### Important sequencing note
User-invoked support should come before heuristic “you seem stalled” behavior.

The product should first help users ask for relief.
Only later should it infer that help may be needed.

### Constraints
- no mass broadcasting
- no auto-routing into others’ attention without clear consent
- no generalized reputation scoring
- no feed-like replenishment dynamics

### Success bar
- stalled lists recover at higher rates than baseline
- users report lower backlog anxiety
- support features do not produce compulsive checking behavior

---

## Phase 3 — Choose one strategic wedge (parallel discovery track)
Use lightweight prototypes/interviews to choose one adjacent wedge to develop alongside Sinc.

Candidates:
- Clerk-style inferred taste alignment
- Circuit small-group loop
- Gutcheck extension

Rule:
pick exactly one.

Do not turn the product into a bundle of half-proven sidecars.

---

## Experiments to run before v1.5 surfaces
### 1. Completion psychology test
Question:
does explicit completion + reflection improve return quality versus silent rollover?

### 2. Negative curation utility test
Question:
are pass / redundant / not-worth-it signals more predictive of satisfaction than saves alone?

### 3. Borrowed Taste trust test
Question:
does one-domain borrowed taste improve perceived quality without reducing agency?

### 4. No-unsorted-inbox enforcement test
Question:
does strict resolve / route / discard behavior reduce guilt-pile formation without creating unacceptable friction?

---

## Operating principles for roadmap decisions
Use these as hard filters for feature acceptance.

1. Does this preserve finishability?
2. Does it keep continuation user-chosen?
3. Does it keep domains semantically narrow?
4. Is borrowed influence always visible and reversible?
5. Does it avoid turning measurement into amplification?
6. Does it improve judgment quality rather than just engagement volume?

If a feature fails two or more of these filters, defer it.

---

## What to explicitly defer
These are conceptually seductive and operationally dangerous if introduced too early.

- full guild / reputation systems
- market / token / protocol mechanics
- global trust scoring
- heavy public messaging
- whole-profile social growth surfaces
- ornate identity layers before core-loop retention is healthy
- any public discovery surface that becomes more important than list completion

---

## Recommended immediate next 5 actions
1. Draft the canonical v1 PRD and lock non-goals.
2. Define the core event taxonomy for analytics.
3. Design list + item lifecycle schemas.
4. Prototype the completion panel and resolve-item flow in low fidelity.
5. Recruit 10–15 design partners across two segments:
   - taste-rich but platform-fatigued users
   - users who already manually route links to friends

Important:
include at least some users who are not already concept-sympathetic, so the product is tested against real behavior rather than philosophical agreement.

---

## Compressed conclusion
The immediate job is not to prove the whole Sinc universe.
It is to prove that a user can repeatedly complete a finite domain list, feel better rather than more burdened, and explicitly choose what comes next.

Everything else is secondary until that works.
