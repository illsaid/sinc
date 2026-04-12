# CIRCUIT — Product Memo v0.1

## One-line
CIRCUIT is a small-group reading utility that helps 3–7 trusted people triage difficult long-form material together, one item at a time.

## What it is
CIRCUIT is a closed, asynchronous reading loop for people who want to engage with serious material without relying on feeds, algorithms, or individual willpower alone.

It does not summarize the internet or replace reading. It lowers the activation energy required to read dense, ambiguous, or important material by letting people borrow trusted judgment from a few other humans.

The unit of value is not endless discovery. It is a bounded act of shared attention.

## The problem
The current content environment makes serious reading harder than it should be.

Users face three recurring problems:
- activation friction: “I know I should read this, but can’t make myself start.”
- epistemic overload: too much material, too little confidence about what deserves attention
- isolated interpretation: even when people finish something substantial, they process it alone and lose the chance for calibration

Read-later tools usually become guilt piles.
Feeds optimize for recurrence, not comprehension.
Group chats make discussion shallow and diffuse.

## Product thesis
People are more willing to read difficult material when:
- it arrives through a trusted human filter
- it is framed with a short opinionated reason to care
- the experience is bounded
- finishing produces a structured social return rather than more noise

Serious reading becomes easier when it feels less like private homework and more like participation in a trusted loop.

## Core product
A CIRCUIT is a private group of 3–7 people.

Each member has a Hold:
- a small queue of items they think may be worth attention
- max capacity: 5 items
- adding a sixth requires deleting one
- this enforces pre-selection and prevents backlog sprawl

Each held item includes:
- URL or document
- title
- source
- optional 50-word Case

The Case is not a summary. It is a stance.

Examples:
- “Strong reporting, but the thesis is too clean. Read for the facts, not the framing.”
- “This complicates the easy story we’ve all been telling ourselves.”
- “Dense, but worth it for section 3 alone.”

When a member is ready, they hit Draw.

Draw serves one item at a time:
- from their own Hold
- or from another member’s Hold
- ideally weighted toward items that have not yet circulated

No infinite scroll.
No browsing maze.
One item, one decision.

Possible actions:
- Read now
- Defer
- Release

After reading, the member sends a Return.

Returns are short, structured reactions:
- Strengthens
  - this holds up and adds to my model
- Complicates
  - this contains signal but destabilizes the easy version
- Breaks
  - this does not hold; flaw noted

Optional note:
- max 100 words
- enough to clarify the judgment without turning into essay theater

The Return closes the loop.
The original seeder gets feedback.
The reader gets closure.
A private micro-thread accumulates around the item.

## Emotional job to be done
CIRCUIT should make users feel:
- less alone in processing difficult material
- less guilty about unread backlog
- less exposed to discovery sludge
- more willing to engage with serious reading because someone they trust already did the first layer of triage

This is not just a reading tool.
It is a cognitive relief utility.

## Design principles
### 1. Boundedness over abundance
Every container has visible limits.
Nothing should quietly grow into another guilt warehouse.

### 2. Trusted human filtering over algorithmic ranking
The system does not decide what matters.
Members do.

### 3. One-item focus
The experience should collapse choice overload into a single moment of attention.

### 4. Structured interpretation over social sprawl
Responses should be richer than likes but lighter than essays.

### 5. Private by default
No public performance layer.
No follower graph.
No engagement theater.

## Why it could work
### Lowered activation energy
A trusted person’s Case helps convert “I should read this someday” into “I can read this now.”

### Social accountability without performance
The Return creates reciprocity and closure without dragging people into a public-comment ecosystem.

### Scarcity as quality control
A five-item Hold keeps the system from turning into another dumping ground.

## MVP
Must have:
- private circuits for 3–7 users
- browser/share extension for capture
- 5-item Hold limit per member
- item metadata + 50-word Case
- Draw flow
- Read / Defer / Release actions
- Return flow with 3 structured reactions + note
- per-item thread/history visible to the circuit
- simple notifications when a Return lands

Good later additions:
- weighted Draw logic
- topic tags
- lightweight highlight capture
- digest of unresolved items
- archive/export

Do not build yet:
- public discovery
- creator profiles
- recommendation engine
- likes/reactions beyond Return types
- large-group communities
- AI summary layer as default interface

## Business model
Subscription billed per circuit.

Possible price band:
- $4–8/month per circuit

This should feel like paying for a shared utility, not joining a media platform.

## Relationship to the broader hole
CIRCUIT is one answer to the judgment problem at intimate scale.
It does not solve public trust or universal curation.
It gives a few people a better way to process important things together without recreating the feed.

## Summary
CIRCUIT is strongest as a wedge: a small trusted loop for reading difficult material with less friction, less isolation, and more closure.

If it works, users should feel that serious reading has become more manageable because it arrives pre-loaded with trusted human judgment and ends in bounded, meaningful response.
