# Confluence Knowledge Base (Option B) — Table Template

This is a **paste-ready template** for maintaining the compliance/security **Statement Knowledge Base** as a **single Confluence page** (Option B).

## Page setup (recommended)

- **Page title**: `Compliance Knowledge Base — Statements`
- **Audience**: humans + Rovo/LLMs
- **Goal**: keep each row **atomic** (one claim), **explicit**, and **traceable** to a source.

## Table (create this in Confluence)

Columns:

- **ID**: Optional stable identifier for a statement (helps refinement without duplication)
- **Statement**: One clear, present-tense claim
- **Tags**: Comma-separated tags from `controlled_tag_taxonomy.md`
- **Status**: One of `implemented`, `conditional`, `not-implemented`, `out-of-scope`
- **Source**: Questionnaire name + question reference (e.g., `Customer Due Diligence v2025 — Q8`)
- **Notes**: Optional scope/clarifying notes (no new claims)

Paste this header row:

| ID | Statement | Tags | Status | Source | Notes |
| --- | --- | --- | --- | --- | --- |

## Row format (for copy/paste)

Each new statement becomes **one row**:

| <ID or blank> | <Statement> | <tag1, tag2, tag3> | <implemented \| conditional \| not-implemented \| out-of-scope> | <Questionnaire + question ref> | <Notes or blank> |

## Rules (keep the KB clean)

- **One row = one claim** (split compound sentences into multiple rows)
- **No guessing**: if not explicitly stated in the questionnaire, do not add it
- **Tags**: must come from `controlled_tag_taxonomy.md` (no synonyms, no vendor/tool names)
- **Prefer fewer tags** over more
- **Refinement**: if a new questionnaire adds precision to the same control, **update the existing row** (keep the ID), and add the new source reference in the Source cell (append with `;`)

## Example rows

| AC-DB-001 | Access to production databases requires VPN access with MFA. | access-control, database, production, vpn, mfa | implemented | Customer Due Diligence v2025 — Q8 | Applies to remote access from local machines. |
|  | Penetration testing is conducted periodically. | vulnerability-management | conditional | Customer Due Diligence v2025 — Q12 | Frequency stated as 12–18 months. |


