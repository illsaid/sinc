# Sinc v0.4 — Design Notes

## Purpose
These notes capture the strongest product-design ideas surfaced during critique of the Sinc memo, especially around depletion, stalled lists, negative curation, and bounded social load-sharing.

The goal is not to turn Sinc into a social feed or group-chat product.
The goal is to preserve the shelf while giving it a circulatory system that activates under pressure.

## Core insight
Sinc is strongest when it acts as a finite personal shelf.

Its main risk is that a shelf can become inert when the user’s judgment is present but depleted.
The failure mode is not lack of taste.
It is activation paralysis.

In that state, a ledger can become a shame archive unless the product provides a relief mechanism.

## Key design question
Is Borrowed Taste merely an overlay, or can it become a bounded load-sharing mechanism when a shelf stalls?

The most promising answer is:
- keep the shelf personal by default
- activate circulation only when a list is stale, stalled, or explicitly routed outward

This preserves agency without forcing users to carry the full burden of curation at every moment.

## Principles to preserve from Sinc
- finite domain-specific shelves
- visible cardinality
- finishability
- no hidden ranking magic
- no infinite feed logic
- narrow trust over generic follows
- public measurement without public steering
- search before recommendation

These remain core and should not be weakened by adding social circulation.

## Proposed additions

### 1. Stalled list detection
A list can enter a stalled state when:
- it has been untouched for a meaningful period
- items remain unread beyond their useful freshness window
- the user repeatedly defers rather than finishes or deletes
- the user explicitly requests help

“Stalled” should be a product condition, not a failure judgment.
It simply means the shelf may benefit from assistance.

### 2. Item half-life / staleness
Unread items should not remain static forever.

Instead of using a universal timer, staleness should be contextual:
- domain-sensitive
- optionally urgency-sensitive
- informed by item type and age

When an item goes stale, the system should ask:
- do you still care about this?
- should this be reviewed by someone you trust?
- is this now better treated as a query than a possession?

The important shift:
A stale item becomes an active judgment prompt, not passive shelf clutter.

### 3. Ask-for-triage mode
When a list stalls, users can deliberately route the burden outward.

Possible actions:
- ask trusted circle to cut this list
- ask for re-ranking
- ask which one item is actually worth reading
- ask what is now redundant
- ask what can be safely ignored

This should be bounded:
- domain-specific
- only to explicitly trusted people
- no mass social broadcasting

This is not a feed.
It is relief by delegated discernment.

### 4. Negative curation as first-class value
One of the strongest possible additions to Sinc is making dismissal more informative.

Current save-centric systems overvalue inclusion.
In an AI-abundance environment, the more valuable signal may often be:
- what to ignore
- what is redundant
- what is bad faith
- what is too weak, too early, or too derivative

Suggested object:
Pass with Warrant

Examples:
- “Redundant with earlier Atlantic piece.”
- “Bad-faith framing.”
- “Too early; wait for synthesis.”
- “Good topic, weak execution.”

These should stay short and high-signal.

### 5. Shared Pass archive within trusted scope
Passes may be more useful to share than Saves.

A trusted-circle Pass archive could help users answer:
- what can I ignore?
- what have people I trust already ruled out?
- what is merely the same argument in new packaging?

This should remain scoped:
- within a circle
- within a domain
- searchable by warrant/type

The point is not public shaming.
It is pressure relief through negative curation.

### 6. Deliberate refill ritual
When a list is finished, Sinc should not auto-refresh into another stream.

Instead, the refill should be conscious.
Potential refill sources:
- my deeper backlog
- recent saves from a trusted domain contact
- recent Passes / exclusions from my circle
- a search query into public shelves

The refill moment is structurally important.
It preserves closure while allowing continuation.

## Borrowed Taste: revised role
Borrowed Taste should remain narrow and domain-specific.

But it should evolve from aesthetic overlay to structural support under load.

That means:
- optional in normal conditions
- more available when a shelf stalls
- useful for cuts, re-ranking, redundancy detection, and selective amplification

Borrowed Taste becomes most valuable not when it says “look at this,” but when it says:
- “skip this”
- “you already got this argument elsewhere”
- “this one is the only item on your shelf worth the effort”

## Trust transfer / path visibility
A promising later idea is visible one-hop trust provenance.

Example:
- I trust Maya on ambient music
- Maya trusts Eli on Japanese cinema
- I can see that path and decide whether to inspect Eli’s shelf

Important: visible path is better than automatic trust transfer.
The system should show provenance before it delegates judgment.

## What not to do
- do not turn circulation into default feed behavior
- do not make social routing mandatory in all cases
- do not auto-push items into others’ attention without clear consent
- do not convert Sinc into generalized reputation infrastructure
- do not over-mechanize staleness with fake precision
- do not let negative curation become public pile-on theater

## Product summary
Sinc should remain shelf-first.

But shelf-first does not mean socially inert.
The strongest evolution path is:
- a finite personal ledger by default
- bounded circulatory support at the moment of depletion, stall, or uncertainty
- stronger negative curation signals
- deliberate refill rituals instead of endless continuation

## Compressed formulation
Sinc remains a ledger.
But when the shelf starts to sag, it should be able to borrow structural integrity from a trusted circle.

That is the likely path from elegant concept to useful prosthesis.
