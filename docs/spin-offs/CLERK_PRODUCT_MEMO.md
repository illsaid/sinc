# CLERK — Product Memo v0.1

## One-line
CLERK is a finite anti-feed queue built from post-consumption judgment capture and taste alignment, designed to restore the feeling of being guided by someone whose taste actually maps to yours.

## What it is
CLERK is a digital replacement for the record-store clerk, the used-bookstore employee, the video-store person in the back — the human who had been through everything, remembered what you liked last time, and could say:
- don’t bother with that one
- this one is yours

The product is the lost job.

It does not ask users to write reviews, build a social audience, or browse an endless recommendation feed. It captures tiny moments of judgment after consumption, learns which other people’s judgments best predict your own, and returns a short finite queue of things likely to be worth your time.

## The problem
The issue is not merely that there is too much content.
It is that the function once performed by human editorial judgment has been replaced by engagement optimization.

Engagement optimization is not a worse version of curation.
It is a different function with different incentives and different outputs.

This creates a distinctive emotional wound:
- people can no longer trust their own consumption
- algorithmic feeds often produce a vaguely hollow feeling after the fact
- FOMO keeps users from skipping things confidently
- recommendation systems optimize for attention capture, not honest fit

The product should make that feeling go away.

## Product thesis
What users need is not another discovery engine.
They need a trustworthy sense that some of their attention was well spent.

The key mechanisms are:
- minimal post-consumption judgment capture
- taste alignment based on demonstrated fit rather than social ties
- finite queue rather than infinite feed
- permission to skip without guilt

## Core product
### 1. End-of-consumption capture
At the natural stopping point for a piece of content, CLERK asks a minimal question:
- was this worth your time?

Optional second field:
- who is this for?

This is not a review.
It is not star rating theater.
It is a tiny judgment captured at the moment a user is already stopping.

Examples:
- worth it
- not worth it
- for people who want x
- only worth it if you care about y

The value is low friction and honest post-hoc signal.

### 2. Taste alignment engine
CLERK does not primarily use the user’s social graph.

Instead, it looks for people whose past judgments best predict the user’s own judgments.

This is the core idea:
- the people you know are not always the people whose taste fits yours best
- social obligation and good taste are independent variables

The system should discover predictive alignment from repeated comparative judgments.

### 3. Finite queue
What CLERK returns is not a feed.
It is a finite queue.

Example promise:
- here are seven things worth your time this week
- when you’re done, you’re done

This is structurally important.
The queue must end.
An infinite queue would collapse back into the feed logic the product is trying to escape.

### 4. Permission to reject
One of the strongest emotional functions of the old clerk was permission.

The good clerk did not only say:
- you will love this

They also said:
- don’t bother with that one

CLERK must make this explicit.
When aligned judges bailed on something, the user should be able to let it go without anxiety.

This is not a small feature.
It is one of the major emotional payoffs.

## What it is not
- not a review platform
- not a social network
- not a generic discovery engine
- not an aggregator of what most people liked
- not a feed

It does not care whether something is new.
It cares whether it is right for you, now.

## Emotional job to be done
CLERK should make users feel:
- less manipulated by recommendation systems
- less guilty about skipping
- less hollow after consumption
- more confident that the time they spent was spent honestly

Even disappointment should feel cleaner, because the expectation was honest.

## MVP
### Must have
- lightweight post-consumption capture
- optional “who is this for?” note
- imported seed signals from existing histories where possible
- taste-alignment engine based on repeated judgments
- finite queue
- visible queue end / completion state
- clear skip signal informed by aligned users’ judgments

### Good later additions
- stronger domain segmentation
- explicit confidence tags
- richer comparative alignment view
- optional provenance notes (“why this reached you”)

### Do not build yet
- public profiles
- social graph theater
- generic creator/follower mechanics
- endless browsing surfaces
- full review/comment systems

## Relationship to Sinc
CLERK is both a possible spin-off and a productive challenge to Sinc.

Sinc tends to emphasize:
- chosen human influence
- explicit borrowed taste
- shelves and lists as visible objects

CLERK emphasizes:
- inferred taste resonance
- post-consumption capture
- queue-based mediation
- permission to reject

These can coexist.

Possible future relationship:
- Sinc uses Clerk-like taste alignment internally
- Clerk acts as a queue-based wedge beside the shelf model
- users can choose between explicit trust and inferred alignment

## Summary
CLERK becomes compelling when it restores the feeling of being guided by a person whose taste genuinely maps to yours.

Its strongest product promise is simple:
we are not trying to capture all of your attention.
we are trying to make some of your attention feel like it was well spent.
