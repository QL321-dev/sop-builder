# SOP Builder

A single-file HTML tool that walks you through writing a proper Standard Operating Procedure (SOP), then exports it as clean Markdown with one click.

**[Open the tool →](index.html)** — just click, fill, export. No install, no account, no server.

## What it is

- One HTML file. Double-click to open in any browser, or host it anywhere (GitHub Pages works out of the box)
- Guided 12-section skeleton: current section highlighted, filled sections turn blue, **missing required sections flash orange** — click any chip to jump
- Drafts auto-save to your browser's localStorage when you click **Save Draft**; reopening the page restores your work. Nothing is ever sent anywhere — it's all on your own machine
- Exports a Markdown file (`sop.md`) that pastes cleanly into Confluence, Notion, Obsidian, Typora, Google Docs, and most other editors

## The skeleton (12 sections: 9 required + 3 optional)

The structure follows internationally accepted SOP conventions — FDA document-control expectations for SOPs, ISO 9001 requirements for documented procedures, and the UK NHS SOP template structure:

| # | Section | Required | What goes in it | Export format |
|---|---|---|---|---|
| — | Document Header | ✅ | Business line, process name, version, effective date, prepared/reviewed/approved by | Info table at top |
| 1 | Purpose | ✅ | What problem this SOP solves | Text |
| 2 | References | ✅ | Governing policy documents (name + number) | Table |
| 3 | Scope | ✅ | Who it applies to, which scenarios, what's covered / not covered | Text |
| 4 | Roles & Responsibilities | ✅ | Role/department + responsibilities | Table |
| 5 | Definitions | Optional | Terms + definitions (only if you have jargon) | Table |
| 6 | Process Overview | Optional | The whole flow, one step per line | Numbered list |
| 7 | Procedure Steps | ✅ | Step name + description; branching decisions via nested hierarchy | `### Step N` + text / nested list |
| 8 | Exception Handling | Optional | Exception scenario + how to handle it | Table |
| 9 | Related Documents | ✅ | Companion forms and attachments (name + number/notes) | Table |
| 10 | Records | ✅ | Record name, completed by, how completed/stored, retention | Table |
| 11 | Revision History | ✅ | Version, date, changes, revised by | Table |

References and Related Documents are deliberately separate: the former are governing policies (the legal basis for doing the work), the latter are companion forms and attachments. Keeping them apart keeps both clearer.

## Export rules

- Required sections are always exported; optional sections are skipped when empty, and section numbers renumber automatically
- Table sections export as standard Markdown tables
- Steps export as `### Step N: title` + description + indented nested lists
- If required sections are missing, you get a warning listing them before export (you can force-export after confirming)
- The exported file ends with a fixed review note: *"Review this document every 12 months, or update it promptly whenever policies change."*

## What it deliberately does NOT cover

The following belong to a full controlled-document system, and this template intentionally leaves them out:

- Document numbering, security classification, distribution lists, review cycles (no document-control department to manage them)
- Step-level structured fields (owner / inputs / outputs / deadlines) — single author, single file; the writer is the executor
- KPIs, training requirements, risk & compliance (manufacturing QMS territory)
- Parallel version management rules (no need for multiple effective versions)
- A separate attachments section (content lives directly in steps and related documents)

## Scaling up later

If you ever outgrow "single author, single file" and move to multi-author, controlled release, the skeleton already has room: add document numbering and classification, step-level owners and deadlines, a separate attachments section, and approver/effective-date columns in revision history. Add sections — no need to rebuild.

## The quality test

The tool guarantees structural completeness — nothing missing, nothing skipped. **Content quality depends on the author.** The hard self-check:

> Hand the exported MD to a colleague who has never done this task. If they can get it right without asking you — it's a real SOP. Wherever they get stuck — that's where it's unclear.

> An SOP is a living document. When someone using it finds a step that's wrong, they fix the MD that day — not at the next 12-month review.
