# TRUSTFALL — Product Memo v0.1

## One-line
TRUSTFALL is a portable attestation layer that lets people issue signed, revocable, domain-specific vouches for other people, with visible provenance and without reducing trust to a single institutional score.

## What it is
TRUSTFALL explores whether human trust can be made more portable, inspectable, and user-owned on the internet.

It is not a universal reputation score and not a replacement for all institutions. Its more interesting function is narrower: a way for people to make explicit, signed attestations about another person in a particular domain, and for third parties to inspect the provenance of those attestations when deciding whether trust is warranted.

The useful primitive is not “reputation” in the abstract. It is the attestation.

Examples:
- “I have worked with Maya as a Python engineer and would trust her technical judgment on production systems.”
- “Eli repaid a personal loan promptly and communicated clearly throughout.”
- “I trust Nina’s judgment on independent film programming.”

These are not likes, endorsements, or profile fluff. They are scoped, legible trust receipts.

## The problem
Most online trust is currently trapped inside institutions and platforms:
- LinkedIn endorsements
- internal references
- marketplace reviews
- credit reports
- platform-specific trust badges

These systems share three problems:
- they are non-portable
- they are often context-poor
- they reduce nuanced human trust into rigid or opaque surfaces

At the same time, fully open reputation systems tend to become dystopian or gameable:
- permanent records
- shallow global scores
- collusive rings
- influencer effects
- sybil attacks

TRUSTFALL is an attempt to isolate the useful layer without importing the whole pathology.

## Product thesis
The internet lacks a good native primitive for portable, revocable, domain-specific human attestation.

The answer is not a universal trust score.
The answer is signed, scoped, inspectable vouching.

A good trust system should support:
- provenance
- context
- revocability
- selective disclosure
- domain specificity
- anti-collusion pressure

## Core product
### 1. Signed attestations
A user can issue a vouch for another user in a specific domain.

Every attestation includes:
- subject
- voucher
- domain
- statement
- confidence
- timestamp
- optional expiration/renewal window
- signature

Examples of domains:
- engineering judgment
- collaborator reliability
- repayment behavior
- event taste
- editorial discernment

The system should strongly discourage vague attestations like “trustworthy person” in favor of bounded claims.

### 2. Provenance paths
A user deciding whether to trust a stranger can inspect trust paths:
- who vouched for them
- who vouched for the voucher
- in which domain
- whether the chain is direct or transitive

The value is not automatic trust transfer. The value is legible trust routing.

### 3. Revocation / tombstones
Attestations can be revoked.

Revocation should not silently erase history. It should leave a visible tombstone that says:
- this attestation once existed
- it is no longer endorsed
- here is when it was withdrawn

This preserves accountability without creating a permanent uncorrectable score.

### 4. Selective disclosure
Not every attestation needs to be universally public.

Possible visibility modes:
- public
- visible to direct trust graph only
- private but shareable by link
- cryptographically provable without exposing the signer identity

This matters for sensitive or asymmetric contexts.

## Design principles
### 1. No global score
The system should avoid collapsing trust into one scalar number.

Trust is contextual.
A person can be excellent in one domain and unreliable in another.

### 2. Domain specificity over social prestige
The system should privilege narrow, bounded claims over broad status abstractions.

### 3. Revocability over permanence
Trust changes. The system must allow withdrawal without pretending the prior state never existed.

### 4. Legibility over hype
The most valuable surface is the visible provenance and scope of an attestation, not gamified metrics.

### 5. Trust quality over graph centrality
Being highly connected should not automatically confer authority.
What matters is whether a user’s past attestations later proved reliable within the relevant domain.

## Anti-abuse / core risk
The central failure mode is collusion:
- reciprocal vouch rings
- sybil identities
- status laundering
- coordinated inflation of standing

Promising countermeasures:
- attestation decay over time
- renewal requirements
- discounting tight reciprocal clusters
- domain-specific reliability histories for vouchers
- requiring downstream validation events where possible

Risky idea to avoid in naive form:
- directly rewarding “hubness” or social centrality

That path recreates influencer dynamics and incumbency bias.

## What it is not
- not a credit bureau clone
- not a decentralized LinkedIn replacement in full
- not a universal identity score
- not a public leaderboard of trusted people
- not a “rate humans” platform

## MVP
A plausible first version would be very narrow:
- issue signed domain-specific attestations
- view provenance chain
- revoke attestations with tombstones
- support limited visibility controls
- simple trust graph inspection

The first usable wedge should be one domain, not universal human trust.

Candidate wedges:
- contractor/operator references
- collaborator reliability
- domain-specific taste endorsement
- curator/editor judgment attestations

## Why it might matter to the Sinc universe
The most promising overlap with Sinc is not universal reputation. It is lightweight trust receipts.

Sinc may eventually benefit from:
- “I trust this person’s taste in this domain.”
- “This item reached you via these human judgment hops.”
- “This shelf is borrowed from someone whose judgment another trusted person vouched for.”

That use is quieter, more bounded, and more humane than trying to build a trust market for all life.

## Summary
TRUSTFALL becomes interesting when treated not as a total replacement for institutional reputation, but as an internet-native primitive for signed, revocable, domain-specific human attestation with visible provenance.

The keeper is portable trust receipts.
The danger is turning that into a universal score.
