---
id: E-0003
type: essence
name: Boundary Contracts Between Layers
version: 1.0
date: 2025-10-24
tags: [contracts, boundaries, traceability, meta-feedback]
---

# Boundary Contracts Between Layers

## Claim: Essence claims must cite substrate

Every essence claim must cite one or more substrate IDs to maintain traceability.

**Supports:** [[S-0005 Separation of Concerns]], [[S-0002 Resume Use Case]]

**Rationale:** S-0005 establishes that separation of concerns requires clear boundaries. S-0002 shows the value of traceability (resume claims to actual work).

## Claim: Substrate to essence is interpretive but verifiable

The substrate → essence boundary is interpretive but verifiable. Interpretation is allowed; invention is prohibited.

**Supports:** [[S-0004 Expression as Input]], [[S-0005 Separation of Concerns]]

**Rationale:** S-0004 shows essence emerges from breaking down expressions (interpretation). S-0005 establishes that clear boundaries prevent tight coupling.

## Claim: Essence to expression is representational

The essence → expression boundary is representational. Expression renders essence without directly modifying it.

**Supports:** [[S-0003 Document Evolution]], [[S-0004 Expression as Input]]

**Rationale:** S-0003 shows that patching expressions causes drift. S-0004 establishes expressions as outputs that can become inputs for refinement.

## Claim: Expression failures generate meta-feedback

Expression failures generate meta-feedback that accumulates for periodic essence review, not immediate changes.

**Supports:** [[S-0003 Document Evolution]], [[S-0004 Expression as Input]]

**Rationale:** S-0003 shows incremental reactive changes cause problems. S-0004 establishes the learning cycle: expression → understanding → refinement.

## Claim: Substrate is append-only

Substrate is append-only. Corrections add new entries rather than mutating existing records.

**Supports:** [[S-0003 Document Evolution]]

**Rationale:** S-0003 shows editing and patching causes information drift. Immutability preserves history and prevents accidental loss.

## Claim: Meta-feedback loop enables learning

The meta-feedback loop enables learning: Expression → meta-feedback → essence updates → regenerated expression.

**Supports:** [[S-0004 Expression as Input]]

**Rationale:** S-0004 establishes that the framework mirrors learning (absorb → extract → synthesize). Meta-feedback enables continuous improvement.

---

## The Two Contracts

### Contract 1: Substrate → Essence
**Type:** Interpretive but Verifiable

**Rules:**
- No invention: every essence claim must cite substrate fact IDs
- Interpretation is allowed but must be traceable
- If a claim lacks substrate support, either add substrate or remove the claim

**Purpose:** Prevents the "telephone game" where meaning drifts from truth.

**Verification:** Traceability validation can be automated.

### Contract 2: Essence → Expression
**Type:** Representational

**Rules:**
- Expression renders essence; it does not modify essence
- Stylistic and audience variations are allowed
- Expression issues generate meta-feedback for later review
- Meta-feedback accumulates; essence updated when warranted

**Purpose:** Keeps clear separation between "what to say" (essence) and "how to say it" (expression).

**Feedback Loop:** Expression → meta-feedback → periodic review → essence updates (if needed) → regenerated expression

---

## Anti-Patterns

### ❌ Patching expression directly
**Problem:** Accumulates drift and bloat

**Correct approach:** Update essence, regenerate expression

### ❌ Inventing essence claims without substrate
**Problem:** Breaks traceability, allows unsupported assertions

**Correct approach:** Add substrate first, then create essence claim with citations

### ❌ Mutating old substrate records
**Problem:** Loses history, risks information loss

**Correct approach:** Add new entry with correction, mark old one as superseded

### ❌ Expression directly modifying essence
**Problem:** Reactive changes, unclear boundaries

**Correct approach:** Log meta-feedback, review later, update essence if warranted
