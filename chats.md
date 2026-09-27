# AI Chat Records — Fix the Slop

This directory contains the AI-assisted development records used during
the "Fix the Slop" challenge for the MegaCorp Ultra Portal 2000 (`Nexora`)
codebase under Ticket MC-4471.

The records below identify every AI session used during the event. Complete
conversation records are stored in the corresponding files in this directory.
The conversation files preserve the original prompts and responses in their
original order.

---

## 01 — ChatGPT Session

- **AI Tool:** ChatGPT
- **Date:** September 27, 2026
- **Record:** `01-chatgpt-session.md`
- **Description:** Repository analysis, debugging workflow, repository-policy
  interpretation, identification of protected/generated files, analysis of
  browser DevTools output, and preparation of targeted debugging prompts.

This session was used to establish an observation-driven repair workflow:
inspect the existing website, identify a specific reproducible issue, make
the smallest appropriate repair, and verify the result without rebuilding
or redesigning the project.

Repository constraints discussed during this session included the fixed
1400px layout requirement, generated-file restrictions, audit markers,
script/link ordering, CSS variable naming requirements, commit-message
requirements, protected/sign-off instructions, and the repository's
AI-policy markers.

**Complete conversation:** `01-chatgpt-session.md`

---

## 02 — Google Antigravity — Session 1

- **AI Tool:** Google Antigravity
- **Date:** September 27, 2026
- **Record:** `02-antigravity-session.md`
- **Description:** Live inspection and targeted in-place repairs covering
  Tasks 02–07.

### Work covered

- **Task 02 — Forum Persistence:** Corrected the `localStorage` key mismatch
  from `"thread"` to `"threads"` on `contact.html`.
- **Task 03 — Contact Form Accessibility:** Associated `<label>` elements
  with their corresponding input controls using `for`/`id` relationships.
- **Task 04 — Blog Search Accessible Name:** Added an accessible label to
  the archive search control.
- **Task 05 — Blog Interactive Semantics:** Improved keyboard accessibility
  for interactive `<span>` elements using appropriate roles, tabindex
  values, and keyboard interaction.
- **Task 06 — Admin Search Case Normalization:** Added case-insensitive
  handling for order-table search queries.
- **Task 07 — Admin Search Multi-Field Scope:** Extended search filtering to
  cover order ID, customer name, email, and product fields.

**Complete conversation:** `02-antigravity-session.md`

---

## 03 — Google Antigravity — Session 2

- **AI Tool:** Google Antigravity
- **Date:** September 27, 2026
- **Record:** `03-antigravity-session.md`
- **Description:** Final maintenance, audit-marker compliance, runtime
  stability work, navigation repair, and cross-page quality assurance
  covering Tasks 08–10.

### Work covered

- **Task 08 — Admin Sidebar Interaction Feedback:** Added navigation
  interaction feedback and active-state handling for existing sections,
  while providing explicit non-interactive feedback for sections that were
  not implemented.
- **Task 09 — Favicon Resource:** Added a valid favicon resource and
  referenced it across the required HTML pages.
- **Task 10 — HTML Audit Marker:** Verified and added the required
  `otter-7` generator marker to the relevant HTML files.
- **Navigation Route Repair:** Created the required root-level
  `contact.htm` route to resolve legacy navigation references.
- **Runtime Stability:** Added the required CMS bootstrap fallback so the
  existing CMS boot timer would not produce an uncaught reference error.
- **Cross-Page QA:** Performed a regression pass across the project pages
  while preserving the fixed 1400px layout, existing script/link ordering,
  and protected generated files.

**Complete conversation:** `03-antigravity-session.md`

---

## 04 — Claude Sonnet Session

- **AI Tool:** Claude Sonnet
- **Date:** September 27, 2026
- **Public Share Link:** https://claude.ai/share/baeb1be6-1187-4f79-a5d3-56c32a4c2f5f
- **Record:** `04-claude-session.md`
- **Description:** Debugging and analysis of the existing website using
  Chrome DevTools console screenshots and the supplied `globals.js` and
  `main.js` source files.

The session examined runtime errors and source-code behavior, including
the `#hero-video.play()` null-reference issue, the
`nexoraBootstrapCMS()` call, the `toggleTheme()` comparison issue, the
`isAdmin` default behavior, sanitization behavior, and mousemove-related
reflow concerns.

The session also examined instructions embedded within source files and
distinguished repository-provided code/sign-off instructions from
actionable application defects.

**Complete conversation:** `04-claude-session.md`

**Public access requirement:** The shared Claude conversation should be
accessible without requiring the reviewer to log in.

---

# Submission Notes

- The files listed above contain the complete AI conversation records
  corresponding to each session.
- Conversation records must preserve the original prompt/response order.
- No conversation should be replaced by a summary inside its corresponding
  record file.
- No prompts or responses should be intentionally omitted from the
  complete conversation records.
- `CHATS.md` serves as the index for the complete records.
- The individual `.md` files are the authoritative conversation records
  for this submission.
