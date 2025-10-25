---
id: E-0010
type: essence
name: Skill Markdown as a Specific Expression Type
version: 1.0
date: 2025-10-25
tags: [expression, skill-design, documentation, context-specific, markdown]
---

# Skill Markdown as a Specific Expression Type

## Claim: A SKILL.md file is an expression with specific constraints and purposes

A skill markdown file is a particular type of expression: it renders knowledge framework content for a specific audience (LLM) in a specific context (tool invocation).

**Supports:** [[E-0002 Three-Layer Architecture]], [[E-0007 Expressions as Decomposable Primary Interface]], [[S-0014 Skill Structure and YAML Requirements]]

**Rationale:**
- It takes organized substrate and essence (the framework content)
- It renders that content for a specific audience (Claude as LLM)
- It has specific format requirements (YAML frontmatter, markdown)
- It has specific constraints (token budgets, progressive disclosure)
- Like any expression, it can be regenerated if substrate/essence changes

## Claim: The SKILL.md structure reflects the three-layer framework itself

The skill uses progressive disclosure (metadata → core → supporting) which mirrors substrate (facts), essence (meaning), and expression (communication).

**Supports:** [[S-0014 Skill Structure and YAML Requirements]], [[E-0002 Three-Layer Architecture]]

**Parallel:**
- **YAML (Metadata):** Like substrate—immutable, fundamental facts (name, description)
- **Main content (Core concepts):** Like essence—abstract principles, relationships
- **Supporting files (Examples, references):** Like expression—contextualized applications

## Claim: Skill design requires understanding the audience as primary constraint

The choice to prioritize LLM comprehension over human readability (or any other audience) fundamentally shapes the expression.

**Supports:** [[S-0015 LLM as Target Audience for Skills]], [[E-0002 Three-Layer Architecture]]

**Rationale:**
- Different audiences need different expressions
- LLMs have specific cognitive patterns (sequential word processing, context windows)
- Clarity about audience enables better design decisions
- This skill is optimized for LLM consumption, not human documentation

## Claim: The description field determines whether the skill gets used at all

YAML description is not auxiliary metadata—it is the first filter determining skill relevance.

**Supports:** [[S-0014 Skill Structure and YAML Requirements]], [[E-0009 Skill Design Principles]]

**Rationale:**
- LLMs may read descriptions before deciding to load full skill
- Imprecise descriptions waste the skill content below
- Description must answer both "what" and "when"
- Description quality directly correlates with skill utility

## Principle: Expression Must Be Verifiable Against Substrate/Essence

The skill (expression) should render substrate and essence accurately, staying true to the framework's actual concepts.

**Supports:** [[E-0008 Verifiability as Validation Gateway]]

**Application:**
- Every concept in skill should map to substrate or essence
- Skill should not invent new framework concepts
- Skill can exemplify and reorganize, but should not distort
- If skill feels wrong, the problem is likely in substrate/essence, not skill

## Principle: Regeneration Requires Clear Substrate/Essence

A well-designed skill can be regenerated from substrate/essence if new insights emerge.

**Supports:** [[E-0002 Three-Layer Architecture]]

**Requirement:**
- Substrate must be clear and verifiable
- Essence must explicitly state what the skill should convey
- Essence should capture: what matters most, what are dependencies, what are non-negotiables
- Then the skill (expression) can be rewritten to better serve the audience

## Concept Dependencies for Skill Design

1. **Clarity on what substrate and essence contain** comes before **designing skill structure**
2. **Explicit skill design principles** comes before **writing the skill markdown**
3. **Understanding information flow** comes before **organizing sections and content**
4. **Precision in core concepts** comes before **elaboration and examples**

---

## Regeneration Decision Framework

**When to regenerate a skill:**
- Substrate or essence changed significantly
- New use cases discovered that change priorities
- Information structure feels wrong for audience
- Description doesn't reflect actual content

**What to preserve:**
- Core concepts from substrate/essence
- Framework integrity
- Audience-appropriate framing

**What can change:**
- Organization and hierarchy
- Examples and supporting materials
- Word choice and phrasing
- Level of detail at each section
