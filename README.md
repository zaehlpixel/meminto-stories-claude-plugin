# Meminto Stories for Claude

![Meminto Stories](assets/logo-square-512x512.png)

Write, shape and review your [Meminto](https://meminto.com/) books with Claude.
Meminto Stories connects Claude to your own Meminto account and adds seven
writing workflows that work for every Meminto theme, for your own factual topics
and for fiction you explicitly ask for. You can use guided questions, free
writing or both. No questionnaire, idea or complete chapter plan is needed to
begin.

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

- A Meminto account. Planning and coaching can start in the conversation, but
  reading or saving book content needs a book you can access.
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
- The plugin cannot create a new book from scratch, change a book template,
  delete an entire book, place print orders or process payments.
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

- "Help me start my Meminto book, even if it is blank and I have no idea what
  to write."
- "Improve a passage in my Meminto book and show me the changes before saving."
- "Check my Meminto book before printing and explain what needs attention."

## Support

- Help center: https://helpdesk.meminto.com
- Email: support@meminto.com
- Website: https://meminto.com/

Copyright Meminto GmbH. See [LICENSE](LICENSE).
