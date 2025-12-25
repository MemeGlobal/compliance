# Compliance Extract Command

Extract normalized statement items from a questionnaire file and update the knowledge base.

## Usage

```
/compliance.extract <questionnaire_file>
```

## Description

This command processes a completed questionnaire file and extracts normalized statement items for the knowledge base. The knowledge base is maintained as a single Confluence page with a table (Option B). The goal is to create clear, atomic, reusable statements in table row format — without guessing or over-committing.

## Examples

```
/compliance.extract FORTUNE_questionnaire_QA.md
/compliance.extract @questionnaire_file.md
```

## Process

When this command is invoked:

1. **Read the questionnaire file** specified in the argument
2. **Read the controlled tag taxonomy** (`controlled_tag_taxonomy.md`)
3. **Read the existing knowledge base** (`compliance_knowledge_base.md`)
4. **Extract statements** from the questionnaire following all guardrails below
5. **Tag each statement** using only tags from the controlled taxonomy
6. **Match against existing statements** in the KB
7. **Generate table rows** in the required format
8. **Update the knowledge base** file with new/refined statements

---

## Guardrails for Statement Extraction

### What the LLM Is Doing

When given a questionnaire, the LLM must:
- Read the **entire questionnaire**
- Identify **explicit security / compliance claims**
- Convert them into **individual statement items**
- Tag each statement using the **controlled taxonomy**

### What Counts as a Statement

A statement must be:
- Explicitly stated in the questionnaire
- Factual and present tense
- One clear claim only

Rephrase questionnaire answers into clear, factual statements. Remove pronouns ("we", "our") and convert to present tense.

**CRITICAL**: Remove entity names (e.g., "Vendor", "Company", "Trinity") from statements. Statements should describe what is done, not who does it. Use passive voice or focus on the control/process itself.

**Good examples:**
> Access to production databases requires VPN access with MFA.
> Pseudonymized, anonymized, aggregate, or de-identified personal data is not re-identified.

**Bad examples:**
> We follow strong access security.
> Vendor does not attempt to re-identify pseudonymized, anonymized, aggregate, or de-identified personal data.
> Trinity maintains a written information security program.

### One Statement = One Item

Each statement item must contain **one claim only**.

If a sentence contains multiple claims, split it into multiple items.

**Example:**
> Access is restricted and logged.

Create two items:
- Access is restricted
- Access is logged

### Handling Yes / No / N/A Answers

- **Yes** → Create a statement only if the answer clearly describes what is done
- **No** → Create a statement with status `not-implemented` (represents what is not done)
- **N/A** → Create a statement only if it clearly defines scope or exclusion (use status `out-of-scope`)

Do not invent explanations.

### What the LLM MUST NOT Do

The LLM must **never**:
- Guess or infer missing details
- Add "industry standard" behavior
- Strengthen wording beyond what was answered
- Assume controls exist because related controls exist
- Generalize customer-specific answers

**If unsure → do not create a statement.**

### Refinement vs New Statement

When a questionnaire overlaps with existing knowledge:
- **Refine** an existing statement only if it is the **same control**, made more precise
- **Create a new statement** if it describes a different control or behavior

Never merge unrelated concepts.

**Example**: If the knowledge base has "Access is restricted" and the questionnaire says "Access is restricted to authorized personnel only", refine the existing statement rather than creating a new one.

### Standalone Knowledge Base

The knowledge base is **standalone**. Statements must be complete and self-contained.
- **Do not** refer to source documents for additional information
- **Do not** create statements that require reading the questionnaire to understand
- If context is needed, add it in the statement or Notes field
- If information is missing, create additional statements to provide context

### Tags (Mandatory)

Each statement must include tags from the **Controlled Tag Taxonomy** (`controlled_tag_taxonomy.md`).

**Rules (must follow):**
- Use **only** tags defined in `controlled_tag_taxonomy.md`
- **Do not invent new tags**
- **Do not use synonyms or variants**
- **Do not use tool, vendor, or product names**
- Prefer **fewer tags** over more

If a concept cannot be expressed using existing tags:
- Flag it for review
- Update the taxonomy **before** using a new tag

### Status (Mandatory)

Each statement must have **exactly one** status:
- **implemented**: The control or practice is in place
- **conditional**: The control exists but depends on specific conditions
- **not-implemented**: The control is explicitly stated as not being done
- **out-of-scope**: The control does not apply to this context

### Required Output Format

The knowledge base is maintained as a **single Confluence page with a table** (Option B).

For each statement item, provide a **paste-ready table row**:

```
| <ID> | <Statement> | <tag1, tag2, tag3> | <status> | <Questionnaire + question reference> | <Notes or blank> |
```

#### Table Row Format Details

- **ID**: Ascending numbers (1, 2, 3, ...) as used in the knowledge base. For new statements from questionnaires, leave blank (numbers will be assigned when added to the knowledge base). If refining an existing statement, include the existing numeric ID.
- **Statement**: Single clear claim in present tense.
- **Tags**: Comma-separated tags; must come from `controlled_tag_taxonomy.md`.
- **Status**: Must be exactly one of `implemented`, `conditional`, `not-implemented`, `out-of-scope`.
- **Source**: Questionnaire name + question reference (e.g., "FORTUNE Questionnaire — Question 8"). If information comes from multiple questions, list them separated by semicolons (e.g., "FORTUNE Questionnaire — Question 8; Question 12").
- **Notes**: Only include if needed for scope or clarity; otherwise leave blank.

#### Example Table Rows

New statement (ID left blank):
```
|  | Access to production databases requires VPN access with MFA. | access-control, database, network, vpn, mfa, production | implemented | FORTUNE Questionnaire — Question 8 |  |
```

Refining existing statement (ID included):
```
| 42 | Access to production databases requires VPN access with MFA. | access-control, database, network, vpn, mfa, production | implemented | FORTUNE Questionnaire — Question 8 |  |
```

Multiple sources (when information spans questions):
```
|  | Access to production databases requires VPN access with MFA. | access-control, database, network, vpn, mfa, production | implemented | FORTUNE Questionnaire — Question 8; Question 12 |  |
```

### Safety Rule (Most Important)

> **If a statement is not clearly and explicitly stated in the questionnaire, do not create it.**

### Final Check

Before creating any statement, verify:
- ✅ Atomic (one claim only)
- ✅ Explicit (clearly stated in questionnaire)
- ✅ Tagged (using controlled taxonomy)
- ✅ No guessing (only what is explicitly stated)
- ✅ Safe to reuse (standalone and self-contained)

