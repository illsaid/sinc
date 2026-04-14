# Sinc — Save Anything Wedge v1 Product Spec

## Purpose
Translate the Save Anything wedge memo into an operational v1 specification.

This document is deliberately practical. It defines:
- the v1 promise
- what is in and out of scope
- screens and user flows
- item lifecycle
- data model
- ranking / resurfacing basics
- desktop/mobile architecture

It is not trying to define the whole Sinc universe.
It is trying to define the first useful product.

---

## 1. v1 product promise
**Catch anything before it disappears — and actually find it again later.**

The first version is a calm memory layer for the disappearing social web.

It helps users:
- save posts, videos, essays, and other media quickly
- avoid losing things they meant to revisit
- route saved items into a small number of meaningful shelves
- process those shelves in finite batches
- search and recover things later from a calm archive

This is not yet a full public judgment network.
This is not yet a generalized cultural-weather product.

---

## 2. v1 scope

### In scope
- desktop browser extension save flow
- mobile share-sheet capture flow
- automatic metadata extraction where possible
- lightweight routing into shelves
- finite shelf views
- lightweight item processing actions
- archive / memory view
- fuzzy search across saved items
- limited resurfacing of old saved items
- basic public read-only edition/weather pages only if they do not slow the personal loop

### Out of scope
- global public scoring layer
- universal browser overlay of crowd judgment
- complex trust graphs
- heavy social features
- comments/replies
- monetized curator layer
- public reputation systems
- generalized AI assistant layer
- protocol / crypto architecture

---

## 3. Target user and wedge

### Primary user
People who regularly encounter ephemeral or hard-to-refind media and feel the pain of losing it.

Examples:
- someone sees an Instagram reel and cannot find it later
- someone sees a Substack post and forgets to save it
- someone encounters a YouTube video they mean to revisit or share
- someone scrolls a lot but does not trust platforms to help them recover what mattered

### Initial emotional wedge
Not:
- better curation
- tame the algorithm
- build your knowledge system

But:
- “Oh good, I won’t lose this.”

---

## 4. Core v1 principles
1. **Save and keep are different actions.**
2. **No durable unsorted inbox.**
3. **Shelves stay few and narrow.**
4. **Processing happens in finite batches.**
5. **Archive is memory, not backlog.**
6. **Continuation is chosen, not trapped.**
7. **The product should feel calm, edited, and shelf-like.**

---

## 5. Primary object model

### Item
A saved/caught media object.

Possible types:
- video
- image/post
- article/essay
- podcast/audio
- miscellaneous URL

### Shelf
A narrow domain bucket the item belongs to.

Examples:
- Film
- Design
- Recipes
- Health
- Music
- Biotech

### Archive entry
A processed item that remains visible/searchable as part of the user’s attention history.

---

## 6. Item lifecycle

### States
1. **Caught**
   - item has been saved from extension/share sheet
   - metadata captured
   - not yet resolved to a shelf or disposition

2. **Resolved**
   - item has been assigned to a shelf
   - or explicitly discarded
   - or temporarily deferred

3. **Queued**
   - item is waiting inside a shelf for processing

4. **Processed**
   - user has taken a judgment action on it

5. **Archived**
   - processed item remains searchable and greyed/calm

6. **Discarded**
   - item intentionally removed from active life

### Hard rule
**Caught must not remain permanent.**
Every item must quickly become:
- shelfed
- discarded
- or very briefly deferred

---

## 7. v1 judgments/actions
Keep these lightweight.

### For resolve stage
- Add to suggested shelf
- Choose another shelf
- Create shelf
- Discard
- Not now

### For processing stage
- Keep
- Dismiss
- Wrong fit
- Already seen
- Open now

### Later but not required for first cut
- short note
- share onward
- move between shelves

---

## 8. Shelf rules

### Recommended v1 shelf count
- healthy range: 4–7 active shelves
- soft warning: 8+
- hard cap can be deferred until needed

### Shelf naming rules
- lightweight creation only
- fuzzy duplicate check when creating new shelf
- suggest similar existing shelf before allowing explosion

### Why
Unlimited shelf creation recreates warehouse behavior under a different name.

---

## 9. Home screen spec
Home must not be a giant all-items feed.

### Required home modules
1. **New to resolve**
   - count of newly caught unresolved items
   - compact list of 1–3 recent ones

2. **Shelves**
   - each shelf shows waiting count + processed count
   - example: Film 5 waiting, Design 2 waiting

3. **Recently kept**
   - calm, greyed memory strip

4. **One resurfaced item**
   - one older archived/queued item worth re-seeing

### Home should not contain
- infinite chronology
- giant inbox
- all saved items mashed together

---

## 10. Desktop screens

### Screen A — Extension quick save
User clicks extension or page action.

#### Required fields shown
- title
- source/platform
- thumbnail/preview when available
- suggested shelf
- save confirmation

#### Primary actions
- Save to suggested shelf
- Change shelf
- Discard

### Screen B — Resolve queue
Small finite list of unresolved items.

For each item:
- preview
- source
- timestamp
- suggested shelf
- actions: assign / create shelf / discard / not now

### Screen C — Shelf view
The core processing surface.

Required:
- shelf name
- waiting count
- processed count
- finite visible batch (e.g. 5 items)
- each item card shows preview, source, timestamp

Actions:
- open
- keep
- dismiss
- wrong fit
- already seen

### Screen D — Archive/search
Searchable calm memory view.

Required:
- search bar
- filter by shelf
- filter by platform/source
- date range
- preview-first results
- greyed visual treatment for processed entries

---

## 11. Mobile screens

### Mobile principle
Mobile is share-sheet first, not overlay first.

### Screen A — Share-sheet confirmation
After sharing from Instagram/YouTube/Safari/etc:
- saved preview
- suggested shelf
- keep/change/discard

### Screen B — Resolve queue
Very light card stack.

### Screen C — Shelf view
Finite batch cards with swipe-friendly actions.

### Screen D — Archive/search
Fast search and recovery.

### Mobile anti-patterns to avoid
- dashboard overload
- long forms
- heavy typing requirements
- giant saved list as home

---

## 12. v1 user flows

### Flow 1 — Desktop catch
1. user sees item on web
2. clicks extension save
3. metadata extracted
4. suggested shelf shown
5. confirms save
6. item enters Caught then Resolved/Queued

### Flow 2 — Mobile catch
1. user sees item in app/browser
2. taps Share
3. chooses Sinc
4. confirmation sheet appears
5. suggested shelf accepted or changed
6. item enters Caught then Resolved/Queued

### Flow 3 — Resolve queue
1. user opens app/site
2. sees 1–3 unresolved items
3. routes each item to shelf / discard / temporary defer
4. unresolved count drops to zero

### Flow 4 — Process shelf
1. user opens shelf
2. sees finite batch of queued items
3. opens or judges items one by one
4. processed items move to archive with greyed treatment
5. shelf shows progress and completion

### Flow 5 — Recover later
1. user vaguely remembers an item
2. uses fuzzy search or shelf/source/date filters
3. finds preview
4. opens or re-shares it

---

## 13. Resurfacing rules
Resurfacing should be extremely restrained.

### v1 resurfacing candidates
- one archived item not opened in a long time
- one queued item that has sat too long
- one saved item from a shelf the user frequently revisits

### Constraints
- max 1 resurfaced item on home at once
- no feed-like “you might also like” module
- no endless queue of resurfaced content

---

## 14. Search requirements
Search is central because retrieval is central.

### Search should match on
- title
- extracted text/snippet
- source/platform
- shelf/domain
- user note (if later added)
- date/time windows

### Important UX examples
- “that weird lamp reel”
- “hormone substack”
- “japanese movie clip”

### Result treatment
Results should emphasize:
- preview image
- source
- shelf
- date
- status

---

## 15. Metadata capture requirements
Per saved item, capture as much as reliably possible.

### Minimum metadata
- canonical URL
- source platform
- title
- preview image/thumbnail
- timestamp saved
- raw source URL
- extracted snippet/description if available

### Nice to have
- author/account name
- duration/runtime
- canonical content ID (e.g. YouTube ID)
- screenshot for fragile posts

---

## 16. v1 technical architecture

### Desktop
- Chrome extension (Manifest V3)
- content scripts only where needed
- extension popup or mini-panel for save flow

### Mobile
- native app or thin app wrapper with share-sheet ingestion
- avoid relying on full mobile browser overlay for v1

### Backend
- auth
- item ingestion API
- metadata extraction service
- shelf + item tables
- search index
- resurfacing job

### Jobs
- metadata refresh/retry
- fuzzy duplicate detection
- resurfacing candidate generation
- optional later edition/weather generation

---

## 17. Data model (v1 logical schema)

### users
- id
- email / auth id
- created_at

### shelves
- id
- user_id
- name
- normalized_name
- created_at
- archived_at nullable

### items
- id
- canonical_url
- raw_url
- source_platform
- source_object_id nullable
- title
- preview_image_url nullable
- snippet nullable
- author_name nullable
- created_at

### user_items
Represents a user’s relationship to an item.
- id
- user_id
- item_id
- shelf_id nullable
- state (caught, resolved, queued, processed, archived, discarded)
- saved_at
- processed_at nullable
- last_opened_at nullable
- defer_count default 0
- judgment nullable (keep, dismiss, wrong_fit, already_seen)

### notes (optional v1.5)
- id
- user_item_id
- text
- created_at

---

## 18. Duplicate/canonicalization rules
This is one of the hardest technical parts.

### v1 strategy
Start with strong platform-specific rules where possible:
- YouTube video ID
- normalized Substack/article URL
- stripped tracking params
- Instagram canonical permalink if obtainable

### General rule
Try to collapse equivalent URLs into one canonical item record while preserving raw source URL for debugging.

---

## 19. Public edition/weather layer (deferred but structurally compatible)
This should not block v1 personal utility.

### If added later, likely signals include
- saved/caught count
- kept count
- reopen count
- finished/opened count where measurable
- pass-along/share count
- recency

### Public IA for broad capture
- platform first
- time second

Examples:
- YouTube → Right now / Today / This week / Archive
- Instagram → Right now / Today / This week / Archive
- Essays → Right now / Today / This week / Archive

### Public page should feel like
- edition
- chart
- paper
- weather

not:
- feed
- social wall
- creator dashboard

---

## 20. Sharing requirements
Everything meaningful should eventually be shareable.

### v1 minimum
- share item link
- share shelf link privately or publicly if enabled later

### later
- share section
- share dated edition
- share card image

---

## 21. Success criteria for v1
The product is working if users:
- save items quickly without friction
- do not accumulate a terrifying blob
- can resolve most caught items into shelves/discard quickly
- process shelves in small batches
- successfully re-find items later
- report relief rather than guilt

### Suggested metrics
- median time from save to shelf resolution
- unresolved items older than 7 days
- active shelf count per user
- % of saved items later recovered/opened
- % of queued items processed
- repeat save behavior after first week

---

## 22. Anti-goals
v1 must not become:
- another bookmark manager with nicer branding
- a productivity guilt system
- a giant “all saved” warehouse
- a public comment layer
- a social reputation game
- a feed replacement that starts feeding again

---

## 23. Compressed v1 definition
**Sinc v1 is a cross-platform catch-anything memory layer with finite shelves, lightweight routing, calm archive/search, and an explicit anti-blob design.**

The product is not yet trying to solve public culture in full.
It is trying to solve a simpler and more immediate problem well enough that later public weather can emerge from real use.
