---
name: review-book
description: Review a Meminto manuscript for its central thread, structure, continuity, reader orientation or consistent voice. Use for editorial feedback on a chapter or book; technical print validation alone belongs to check-print-readiness, and a requested passage rewrite belongs to rewrite-story.
---

# Read a Meminto book as an editor

Assess the writing against the author's intended book, reader and scope. Work
with themed books, free collections, factual custom projects and explicitly
fictional work. Offer useful observations, not a universal ideal manuscript.
This is an editorial review; it does not certify facts or physical print quality.

## Establish scope and coverage

Select the accessible book with `list_books` and `get_book_outline`. Reuse a
book compass supplied in this conversation if still relevant; otherwise infer
only what the text supports and clarify a material ambiguity. Without a book
connection, review supplied text and say that coverage is limited to it.

Read complete relevant chapters with `get_book_outline(detail: "full",
chapter_id: ...)` or passages with `get_question`. Follow `truncated` results
until the requested scope is covered, or disclose precisely what remains
unread. Summary excerpts and search hits help find sources; they do not prove
whole-book coverage. `analyse_book` can supply leads, not conclusions about
coherence; its life-decade and chapter-length heuristics may not fit this book.
Use `search_books` within the selected book to investigate a specific issue.

## Review what matters to this project

- Central thread and order: explain what connects sections and where a reader
  may lose orientation. An episodic collection needs no forced plot, conflict,
  revelation or equal coverage of every period.
- Continuity: compare stated dates, names, relationships, places and narrator
  knowledge. Distinguish a probable conflict from different events, deliberate
  flashbacks, uncertain memories or differing contributors' accounts. Cite both
  passages; ask rather than deciding which account is true.
- Reader orientation: check introductions, unclear pronouns, unexplained family
  terms and time/place jumps for the intended audience. A family reader and an
  unfamiliar reader may need different amounts of context.
- Repetition and open threads: distinguish accidental duplication from a chosen
  motif or independent recollection. A missing transition or unfulfilled setup
  must be grounded in actual text, not an invented chapter requirement.
- Voice and perspective: identify unexplained shifts without erasing a dialect,
  personal expression, multiple contributors or an intentional style change.
- Beginning and ending: consider whether they serve this particular book.
  Do not invent closure, a lesson, an emotion or details of a loss.

For a factual book, separate the author's statements, uncertain recollections
and your interpretations. Do not add dialogue or sensory details to repair a
gap. For explicit fiction, assess consistency against the agreed fictional
brief without presenting it as real testimony.

## Give evidence and an actionable result

Lead with the assessment and coverage. Prioritize a few useful findings while
disclosing the total if there are more. For each finding, name the chapter and
section, give a short exact example or two conflicting locations, explain the
reader's difficulty, and offer a concrete next step. Label confirmed textual
issues, questions needing clarification and optional preferences separately.
Say what already works when the source supports it. Do not invent a numerical
quality score or guaranteed reader reaction. A requested simulated reader view
is an AI perspective, not feedback from real test readers.

A review changes nothing: do not rewrite, reorder, add, merge, remove or render
as a side effect. If the user subsequently requests a fix, show the structural
plan or concrete text preview and follow the relevant tools' approval/version
controls. Technical print questions need `validate_before_print` through the
print-review workflow; an editorial opinion cannot replace that result.
If `get_book_context` is offered by the connected server, read it when resuming
this book. With the author's agreement, save a concise compass, style preference
or editorial note using `save_book_context`. Preserve unrelated items and send
the read `expected_version`; reconcile conflicts rather than overwriting.
Use confirmed/proposed/uncertain accurately, and reference current source
question IDs/versions for text-dependent notes. `sources_stale` is computed
read metadata: omit it from saved items. Re-read stale passages before relying
on a note. These notes are private to this user/book and never printed; they
are not shared with other contributors. `items: []` clears them when requested.
If these tools are absent, keep a copyable handoff in the conversation and say
that it has not been saved across chats. Never store notes in printable answers.
