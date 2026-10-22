# Meminto – Write Your Book for Claude

![Meminto Stories](assets/logo-square-512x512.png)

**From idea to printed book.** Plan, write and organize your book with Claude.
Turn memories, ideas and scattered notes into a coherent manuscript, find a
central thread and develop your own voice. Planning, coaching and feedback on
supplied passages can begin in the conversation without a Meminto account.
Review the final layout and order your printed book in Meminto when you are
ready; the plugin does not place orders or process payments.

Connect [Meminto](https://meminto.com/) to work with an existing book: organize
chapters, save approved revisions, import manuscripts and supported photos,
resume private working notes and check technical print readiness. Seven shared
workflows support memoirs, family and travel stories, other factual subjects
and explicitly requested fiction. Guided questions and free writing are both
welcome. No questionnaire or complete chapter plan is required.

## What the plugin contains

- A remote MCP server reference to `https://app.meminto.com/mcp/v1/mcp.php`,
  the same server as the Meminto Stories connector.
- Seven skills:

| Skill | What it helps with |
| --- | --- |
| `start-book` | Begin or continue a book through a guided interview or free writing, including an empty book and an author without an idea. |
| `shape-book` | Find a central thread, a flexible structure and a chapter plan, or organize scattered material. |
| `writing-coach` | Small optional exercises and explanations of writing techniques, in the author's own voice. |
| `rewrite-story` | Faithful revision, including Hemingway-inspired clarity, shown as a preview before anything is saved. |
| `review-book` | Editorial feedback on structure, continuity, voice and reader orientation, citing the actual passages. |
| `import-book` | Private manuscript upload, a proposed structure and a complete conversion review before an approved import. |
| `check-print-readiness` | Technical print blockers, warnings and optional improvements. |

## Requirements

- No Meminto account is needed for conversation-only planning, coaching or
  feedback on supplied book material. Reading or saving stored book content
  requires a connected Meminto account and an accessible existing book.
- Sign-in uses Meminto's OAuth page (Authorization Code with PKCE). Your
  Meminto password is entered only on `app.meminto.com`; the plugin contains no
  credentials or tokens.

## How changes are handled

- Suggestions are not authorization. Nothing is saved unless you ask for it.
- Rewrites of existing text are stored as a concrete preview first. They are
  applied only after your explicit approval and only with the matching current
  preview version. Facts, uncertainty, narrator, voice and media are preserved.
  Missing memories, dialogue and facts are never invented.
- Manuscript import is owner-only and needs an existing writable book. A file
  attached to the chat is not a Meminto upload: the skill gives you a private
  upload link, shows the complete converted plan, and adds new chapters and
  sections at the end of the book only after you approve. Supported sources are
  DOCX, UTF-8 TXT and Markdown, and, when enabled, digital PDF text with supported
  embedded images. No OCR or exact original layout is promised. Recognized
  public YouTube links can become video/QR references; other links stay text.
  Remote videos are not downloaded and original photos are never replaced by
  generated pictures.
- Book permissions, book status and package capacity always apply.
- When first-book setup is enabled, register and confirm your email in the
  Meminto browser flow, then grant access separately. Eligible accounts without
  an owned book can approve one limited starter book after reviewing its theme,
  title and actual capacities. Blank mode adds no preset questions. A separate
  permission is required; existing write grants do not automatically include it.
- General book creation, template changes, whole-book deletion, print orders
  and payments are not supported.
- When the server enables private working notes, they stay outside printed
  book content and are private to you and the selected book.

## Data and privacy

The plugin runs no local code. It sends requests only to the Meminto MCP server
above, which returns the book data needed for the tools Claude calls (for
example outlines, sections, media metadata, import previews or print findings)
to Claude so it can answer you. Meminto stores data under its
[privacy policy](https://meminto.com/privacy-policy/) and
[terms](https://meminto.com/general-terms-and-conditions/). You can disconnect
at any time in Claude's connector settings; disconnecting does not delete your
Meminto books.

## Example prompts

- "I want to write a book, but I don't know where to start."
- "Help me turn my memories and notes into a chapter plan."
- "I already have a manuscript. Help me organize it into a book."

The connection is needed for stored book operations, not to discuss an idea.
A plan in the conversation does not create a book in Meminto. An installation
screen may still offer connector setup; it is distinct from the writing task.

## Support

- Help center: https://helpdesk.meminto.com
- Email: support@meminto.com
- Website: https://meminto.com/

Copyright Meminto GmbH. See [LICENSE](LICENSE).
