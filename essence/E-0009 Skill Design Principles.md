---
id: E-0009
type: essence
name: Skill Design Principles for LLM Audiences
version: 1.0
date: 2025-10-25
tags: [skill-design, pedagogy, llm-audience, information-architecture]
---

# Skill Design Principles for LLM Audiences

## Claim: YAML description is the gate-keeper for skill invocation

The description field in YAML frontmatter is disproportionately important because it determines whether an LLM will recognize that this skill is relevant to a task.

**Supports:** [[S-0014 Skill Structure and YAML Requirements]]

**Rationale:**
- Description is often read before full skill content
- Must answer: "What does this do?" and "When do I use it?"
- If description doesn't communicate clearly, skill goes unused
- Precision and clarity in description directly impact skill utility

## Claim: Every word matters in skill design

Skill content differs from normal documentation because each word builds on previous words and must be strategically chosen.

**Supports:** [[S-0014 Skill Structure and YAML Requirements]]

**Rationale:**
- LLMs process word-by-word sequentially
- Vague or imprecise terms confuse subsequent understanding
- Repetition with consistency reinforces learning
- Efficiency in word choice focuses attention
- Word choice mistakes compound through the document

## Claim: Information flow must proceed from abstract to concrete

Effective skills structure information so that abstract concepts are grounded in concrete examples early, preventing confusion.

**Supports:** [[S-0016 Skill Information Flow and Hierarchy]]

**Rationale:**
- Abstract concepts alone are hard to grasp
- Concrete examples make abstract ideas tangible
- LLMs apply concepts better when they have grounding
- Theory then application is harder than theory + application simultaneously

## Claim: LLMs need explicit concept dependencies

LLMs should know which concepts must be understood before others, rather than having to infer ordering.

**Supports:** [[S-0015 LLM as Target Audience for Skills]], [[S-0016 Skill Information Flow and Hierarchy]]

**Rationale:**
- Concept A may depend on understanding Concept B
- Explicit dependencies prevent confusion
- LLMs can then order their learning appropriately
- This mirrors how humans learn structured knowledge

## Principle: Progressive Disclosure Enables Efficiency

Skills should organize information into layers that are loaded as needed, respecting token limits and attention.

**Supports:** [[S-0014 Skill Structure and YAML Requirements]]

**Key Levels:**
1. **Metadata (YAML):** What is this? (~100 tokens, always)
2. **Core concepts:** How does it work? (Main skill body, on trigger)
3. **Supporting materials:** Examples, edge cases, deep dives (on need)

## Principle: Clarity Over Completeness

A skill should be clear and focused rather than comprehensive.

**Supports:** [[S-0014 Skill Structure and YAML Requirements]]

**Decision Framework:**
- Include: Essentials, clear examples, necessary caveats
- Exclude: Tangential information, comprehensive coverage of all cases, meta-commentary

## Concept Dependencies for Skill Design

1. **Understanding target audience (LLM)** comes before **designing information flow**
2. **Clarity on core concepts** comes before **writing instruction content**
3. **Explicit dependencies between concepts** comes before **organizing information hierarchy**
4. **Precision in language** comes before **building complex arguments**

---

## Application to This Framework's Skill

For the knowledge organization framework skill specifically:

**Priority 1 - Core Understanding:**
- What are the three layers? (substrate, essence, expression)
- How are they different?
- What is the boundary contract between them?

**Priority 2 - Application:**
- How do I identify substrate vs. essence?
- How do I create each layer?
- How do I use them together?

**Priority 3 - Depth:**
- What are the different use cases?
- What are common misunderstandings?
- How does this scale?

**Supporting Materials:**
- Concrete examples in different domains
- Reference materials and templates

---

## Anti-Patterns in Skill Design

### ❌ Comprehensive coverage
**Problem:** Including everything leads to unclear priorities
**Solution:** Focus on essentials and provide examples

### ❌ Abstract concepts without examples
**Problem:** LLMs struggle to apply theory without grounding
**Solution:** Use examples early and often

### ❌ Unclear or jargony language
**Problem:** Makes skill hard to understand and apply
**Solution:** Define terms clearly, use consistent terminology

### ❌ Poor concept ordering
**Problem:** Building on concepts that haven't been explained yet
**Solution:** Explicitly state dependencies, order accordingly

### ❌ Overly long introductions
**Problem:** Important content buried, reader loses focus
**Solution:** Get to core concepts quickly, provide context as needed
