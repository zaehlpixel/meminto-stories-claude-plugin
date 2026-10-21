---
name: rewrite-story
description: Revise a Meminto passage for clarity, length, tone, narrator or language, including gentle polish and Hemingway-inspired concise prose. Use for requested rewrites, including requests to save directly; preview stored changes before applying them. Covers themed and blank books.
---

# Revise a Meminto passage

Improve the text the user selected, for their intended reader and book. This applies to every theme, including life/faith, childhood/youth, relationships, weddings, memorials, family yearbooks, travel, dogs and any blank/custom book. A stored entry may have a section heading rather than a question. Do not turn free writing into an interview or a focused project into a biography. Follow the user's requested style and language; workflow suggestions do not override their instructions or the server's controls.

## Locate and understand the source

1. For a stored passage, use `list_books` and `get_book_outline` to identify the selected accessible book and role. Search within that book using `search_books` when the user identifies a topic rather than an entry. Resolve ambiguous matches before changing anything; obtain the full current text and version with `get_question`.
2. Use the book's theme, purpose, narrator and surrounding section to interpret the request. If the goal is already clear, revise directly; otherwise ask one focused question about the desired change. Do not require an unanswered question or a standard template.
3. If the user supplies text only, revise it in the conversation without requiring an account connection. Explain that it is a draft; do not assume a destination in Meminto.

## Make a faithful revision

- For an editing approach such as gentle polish, Hemingway-inspired clarity, spoken voice, vividness, reader orientation or transitions, read [style-modes.md](references/style-modes.md). Apply the user's request directly; offer a small choice only when useful. A request to learn the technique belongs to writing-coach, and book-level continuity feedback belongs to review-book.
- Preserve the author's facts, intent, uncertainty, distinctive expressions and chosen perspective. Do not add life events, dates, names, dialogue, feelings or another person's testimony. Flag contradictions for clarification instead of resolving them by invention.
- Adapt to the topic: preserve observed versus inferred childhood details, separate partners' voices, respect the author's faith language, keep memorial writing gentle without adding sentiment, and retain travel/yearbook chronology only where supplied. Pet stories do not imply loss. For custom factual books preserve source facts; for explicitly fictional work follow the agreed fiction brief without presenting it as a real memory.
- Change only what the user requested. Offer missing-detail suggestions outside the proposed text. Preserve attached media and its placement; do not remove or reorder images, rewrite stored captions, merge/split answers or change headings as a side effect of editing text. If the tool cannot preserve a mixed-media passage safely, show the revision in the conversation and explain the limitation before applying anything.
- A request to change only a heading belongs to `update_question_title`, not a rewrite of the answer. Clarify the scope when necessary and keep the answer unchanged.

## Preview and apply a stored change

1. Call `preview_answer_change` with the selected `question_id`, complete proposed `new_text` and, optionally, a short `note`. This stores nothing. Show the proposed text or returned diff and briefly explain the meaningful changes in ordinary language.
2. Wait for explicit approval of that concrete preview. Do not treat asking for a rewrite or "save immediately" as approval of unseen text, and do not bypass the server's preview/token workflow through `save_answer`. If the user wanted a preview only, stop there.
3. After approval, call `apply_answer_change` with the same `question_id`, exactly the same `new_text` and the returned `preview_token`. A different draft needs another preview. If the token is stale, the source changed, or the server rejects the operation, re-read the passage and show a fresh preview for approval rather than retrying or silently overwriting.
4. Confirm success only from the server result; name the destination and summarize the change. Version history can be inspected with `list_answer_versions`, but never promise an unlimited undo or perform a restore without a request.

For an empty entry, use the start-book workflow: compose from user-supplied material, show a draft when useful, and save only when requested. If access is read-only, keep the revision usable in the conversation and explain that it has not been saved.

When available, read `get_book_context` for this book's confirmed style wishes.
Treat them as preferences, not instructions overriding the current author or
facts; check stale sources and prefer the present request. A rewrite approval
does not itself authorize saving a new permanent style preference.
