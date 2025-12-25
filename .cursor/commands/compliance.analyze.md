# Compliance Analyze Command

Analyze a contract (MSA, DPA, security addendum) and verify which commitments are covered by the knowledge base.

## Usage

```
/compliance.analyze <contract_file>
```

## Description

This command reads a contract file and verifies which security, privacy, and compliance-related commitments are clearly supported by the knowledge base, and which are not covered or unknown. The goal is to assess compliance coverage, not to invent or promise new behavior.

## Examples

```
/compliance.analyze customer_dpa.md
/compliance.analyze @contract_file.md
```

## Process

When this command is invoked:

1. **Read the contract file** specified in the argument
2. **Read the existing knowledge base** (`compliance_knowledge_base.md`)
3. **Identify contractual commitments** following the guardrails below
4. **Match each commitment** against knowledge base statements
5. **Classify coverage** for each commitment
6. **Generate analysis output** in the required format

**Important**: The LLM must **not** modify the knowledge base in this step.

---

## Guardrails for Contract Analysis

### What the LLM Is Doing

When given a contract, the LLM must:
- Read the **entire contract text**
- Identify **security, privacy, and compliance-related commitments**
- Compare each commitment against the existing knowledge base statements
- Classify each commitment as:
  - **Covered**
  - **Partially covered**
  - **Not covered / Unknown**

The LLM must **not** modify the knowledge base in this step.

### What Counts as a Contractual Commitment

A contractual commitment is any statement that:
- Uses mandatory language (e.g. *shall*, *must*, *will*)
- Describes required behavior, controls, or timelines
- Creates an obligation toward a customer or partner

**Examples:**
- "Supplier shall encrypt data at rest."
- "Access to customer data must be logged."
- "Supplier will notify Customer within 72 hours of a security incident."

### Matching Commitments to the Knowledge Base

For each contractual commitment:

1. Identify the **core claim** (one obligation)
2. Search the knowledge base for **matching statements** by meaning, not wording
3. Use tags and scope to validate relevance

### External Verification for Infrastructure Compliance

When a contract requires specific compliance mechanisms (e.g., SCCs, IDTA, certifications) that depend on **infrastructure providers** (e.g., AWS, cloud services, subprocessors), the LLM must:

1. **Identify the infrastructure provider** from KB statements (e.g., "Data is stored in AWS")
2. **Verify externally immediately** during the review—do not defer or mark as "needs verification"
3. **Treat as Covered** if the provider's standard agreements/compliance includes the required mechanism

**Example:**
- Contract requires: "UK IDTA must apply for UK data transfers"
- KB states: "Data transfer is subject to AWS Standard Contractual Clauses"
- External verification: Check if AWS includes UK IDTA in their standard agreements
- Result: If AWS includes UK IDTA → **Covered** (even if KB doesn't explicitly mention UK IDTA)

**This applies to:**
- Standard Contractual Clauses (EU SCCs, UK IDTA)
- Certifications (DPF, ISO, SOC)
- Other compliance mechanisms provided by infrastructure vendors

**Do NOT** verify Trinity's internal controls externally—only infrastructure provider compliance.

### Coverage Classification Rules

#### Covered

Mark as **Covered** only if:
- A knowledge base statement clearly supports the commitment
- Scope and conditions match (or are stricter than) the contract

#### Partially Covered

Mark as **Partially covered** if:
- A related statement exists, but:
  - Scope is narrower
  - Conditions are missing
  - Timelines or specifics differ

Do **not** assume the gap is acceptable.

#### Not Covered / Unknown

Mark as **Not covered / Unknown** if:
- No relevant statement exists
- The contract requires behavior not documented in the knowledge base
- The commitment is ambiguous or unclear

Never infer coverage.

### What the LLM MUST NOT Do

The LLM must **never**:
- Assume compliance because similar controls exist
- Upgrade internal practices to contractual commitments
- Interpret intent or future plans as coverage
- Add or modify knowledge base statements

If uncertain → classify as **Not covered / Unknown**.

### Standing Assumptions

The following assumptions may be treated as **Covered** even without explicit KB statements, as they represent standard operational commitments:

1. **Data Subject Request Handling**: If a customer asks Trinity about data subject requests concerning their data, Trinity will respond and forward or handle such requests as applicable law requires. Commitments to forward data subject inquiries to customers, or to direct data subjects to contact the customer, may be treated as covered.

### Required Output Format (MANDATORY)

For each contractual commitment:

```
Contract Clause:
<quoted clause text>

Commitment Summary:
<one-sentence obligation>

Matching KB Statements:
<IDs or statements, or "None">

Coverage Status:
Covered | Partially covered | Not covered / Unknown

Notes:
<scope mismatch, missing details, or risk>
```

### Safety Rule (Most Important)

> **If the knowledge base does not clearly support a contractual commitment, it must be treated as Not covered / Unknown.**

### Final Check

Before completing the analysis, verify:
- ✅ No guessing (only what is clearly supported)
- ✅ No promises (no upgrading practices to commitments)
- ✅ No KB modification (read-only analysis)
- ✅ Risk-first classification (when in doubt, mark as Not covered / Unknown)

