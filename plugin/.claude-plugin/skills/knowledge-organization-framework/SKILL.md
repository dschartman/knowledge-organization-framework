---
name: knowledge-organization-framework
description: A self-hosting knowledge organization framework that separates facts (substrate), meaning (essence), and communication (expression). Helps apply the framework to organize knowledge systematically across different use cases.
---

# Knowledge Organization Framework Skill

## What This Skill Does

This skill helps you apply a knowledge organization framework to systematically structure knowledge with clear separation of concerns. It's designed to help you and other LLMs:

- Understand the **three-layer architecture** (substrate, essence, expression) and why separation matters
- Apply the framework to different use cases (writing, decision-making, research synthesis, personal knowledge management)
- Navigate the boundary contracts that keep layers clean and traceable
- Think through how to organize knowledge *before* producing expressions
- Generate better documents, decisions, and artifacts from well-organized knowledge

**Key insight:** Good knowledge organization creates value independent of any specific output artifact. It enables better writing, better decisions, and better thinking.

---

## The Three-Layer Architecture

### Substrate Layer: Observable Facts
**Purpose:** Immutable inventory of verified observations and evidence

**What lives here:**
- Factual observations with provenance (where they come from)
- Data points, experiences, research findings
- Concrete examples and evidence
- Metrics, dates, outcomes
- Direct quotes or records

**Characteristics:**
- Append-only (corrections add new entries rather than mutate old ones)
- No interpretation or judgment
- Traceable sources
- Examples: career accomplishments, project outcomes, research data, meeting notes, customer feedback

**Why it matters:**
- Prevents the "telephone game" where facts drift over time through repeated retelling
- Creates a single source of truth for what we actually know
- Enables traceability: "Where did this claim come from?"

### Essence Layer: Meaning and Relationships
**Purpose:** Abstract, auditable model of significance derived from substrate

**What lives here:**
- Claims and principles that interpret substrate facts
- Relationships between concepts and their dependencies
- Priorities and what matters
- Ordering dependencies (concept A before concept B)
- Terminology and definitions
- Cause-and-effect reasoning

**Characteristics:**
- Traceable to substrate (every claim cites supporting facts)
- Abstract and generalizable (not tied to specific contexts)
- Can evolve as understanding deepens
- Captures relationships and concept ordering as much as individual concepts

**Why it matters:**
- Meaning emerges from relationships, not isolated facts
- Proper ordering enables teaching and understanding (you can't learn B before A if B depends on A)
- Traceability prevents unsupported assertions and keeps meaning grounded in reality
- You can reason about multiple expressions from the same essence

### Expression Layer: Communication and Application
**Purpose:** Context-specific instantiation of essence for audiences and purposes

**What lives here:**
- Documents, articles, blog posts
- Decisions and decision rationales
- Actions and implementations
- Presentations and communications
- Anything that puts knowledge to work for a specific purpose

**Characteristics:**
- Audience-specific (tailored for who will use it)
- Purpose-driven (optimized for a specific goal)
- Can be regenerated if essence changes
- Derived entirely from essence (not invented from scratch)

**Why it matters:**
- Same knowledge can produce multiple expressions for different contexts
- Separates "what to say" (essence) from "how to say it" (expression)
- Enables systematic regeneration: if essence improves, expressions can be refreshed
- Failures in expression generate meta-feedback for essence review

---

## The Two Boundary Contracts

### Contract 1: Substrate → Essence
**Type:** Interpretive but Verifiable

**The rule:** Every essence claim must cite supporting substrate facts.

**What this allows:**
- ✅ Interpretation of facts (drawing meaning from data)
- ✅ Combining multiple facts into larger claims
- ✅ Identifying patterns and relationships

**What this prevents:**
- ❌ Invention (claims with no factual support)
- ❌ Telephone games (facts drifting away from sources)
- ❌ Unsupported assertions

**How it works:**
- Essence explicitly references substrate IDs (e.g., "[[S-0001 Framework Purpose]]")
- If you find yourself making a claim without substrate support, add substrate first, then create the essence claim with citations
- If substrate is missing, either add it or remove the unsupported claim

### Contract 2: Essence → Expression
**Type:** Representational

**The rule:** Expression renders essence; it does not modify essence.

**What this allows:**
- ✅ Stylistic variation (different tones for different audiences)
- ✅ Selecting relevant subsets of essence
- ✅ Audience-appropriate framing

**What this prevents:**
- ❌ Direct modification of essence from expression
- ❌ Reactive patching that accumulates drift
- ❌ Unclear boundaries between "what to say" and "how to say it"

**How it works:**
- Expression failures generate *meta-feedback* for later review
- Meta-feedback accumulates until periodic essence review
- If essence needs updating based on expression feedback, you update essence and regenerate the expression
- This prevents the accumulation of patches and keeps expression clean and regenerable

---

## How to Apply This Framework

### Step 1: Capture Substrate (The Facts)
Start with what you actually know—don't worry about organizing it perfectly yet.

**Do this when:**
- Reviewing existing documents or conversations
- Working through a decision
- Researching a topic
- Gathering requirements or feedback

**Create substrate entries by:**
- Recording observable facts, outcomes, or data points
- Including the source or context (provenance)
- Being specific: "5 customers requested feature X" not "people want feature X"
- Adding one entry per distinct fact or observation

**Example:**
```
id: S-0042
date: 2025-10-25
author: @your-name
provenance: "Customer interviews, Oct 2025"
tags: [feedback, feature-request]

## Observations
- 5 out of 8 interviewed customers mentioned difficulty with onboarding
- Average time to first successful login: 23 minutes (compared to 5 minutes for competitor)
- 3 customers mentioned unclear terminology in the setup wizard
```

### Step 2: Extract Essence (The Meaning)
Once you have substrate, look for patterns, relationships, and meaning.

**Do this when:**
- You have enough substrate to see patterns
- You're preparing to make a decision
- You want to understand what knowledge actually enables
- You're about to create an expression

**Create essence entries by:**
- Identifying claims or principles that emerge from the facts
- Explicitly citing the substrate that supports each claim
- Capturing relationships and dependencies between concepts
- Explaining *why* something matters or how concepts relate

**Example (building on the substrate above):**
```
id: E-0042
type: essence
name: Onboarding Complexity Affects User Adoption

## Claim: Onboarding difficulty is the primary adoption barrier

The data shows onboarding time and clarity issues directly correlate with initial adoption success.

**Supports:** [[S-0042 (the substrate entry above)]]

**Reasoning:** The 23-minute onboarding time vs 5-minute competitor baseline suggests structural issues. Multiple mentions of terminology confusion point to a specific addressable problem.

## Related Concept Dependencies
- Understanding why users struggle (terminology clarity) must come before redesigning the setup flow
- Competitive context (5-minute baseline) provides urgency and success criteria
```

### Step 3: Generate Expression (The Output)
With organized substrate and essence, create the specific artifact you need.

**Expressions might be:**
- A onboarding redesign document
- A decision to prioritize the onboarding project
- A support guide explaining the setup process
- A product roadmap emphasizing onboarding improvements
- An email to stakeholders explaining the problem

**How to approach it:**
- Ask: "What essence do I need to render for this audience and purpose?"
- Draw on substrate for concrete examples and numbers
- Use essence relationships to structure your thinking
- Generate the expression knowing you can regenerate it if essence changes

---

## Different Use Cases (Theory, Not Prescription)

### 1. Systematic Writing
**Goal:** Write well-informed documents that improve over time

**How it works:**
- Substrate: notes, research, sources, examples
- Essence: argument structure, key claims, narrative flow
- Expression: the actual document (blog post, article, paper)

**Value:** As you learn more, add substrate. Update essence. Regenerate documents that are now better informed.

### 2. Decision-Making
**Goal:** Make decisions that are well-reasoned and traceable

**How it works:**
- Substrate: data, stakeholder input, constraints, outcomes from similar past decisions
- Essence: principles for this decision, trade-offs, dependencies, success criteria
- Expression: the actual decision, decision rationale, implementation plan

**Value:** Decisions are traceable to evidence. Future you (or your team) understands *why* this choice was made.

### 3. Research and Synthesis
**Goal:** Deeply understand a topic and communicate that understanding

**How it works:**
- Substrate: papers, experiments, observations, findings from literature
- Essence: what the research means, how findings relate, gaps in understanding
- Expression: synthesis document, literature review, research roadmap

**Value:** You don't just collect papers—you understand relationships between them and can identify what's missing.

### 4. Personal Knowledge Management
**Goal:** Organize what you know so you can think more clearly and act more effectively

**How it works:**
- Substrate: books you've read, conversations you've had, things you've learned
- Essence: principles and relationships that emerge from your learning
- Expression: principles you live by, decisions you make, guidance you give others

**Value:** Your knowledge compounds. Relationships between concepts become visible. You can apply knowledge consistently.

---

## Core Principles to Guide Application

### 1. Expression-Driven Development
**The rule:** The value of creating an expression should drive what you do.

**Key question:** "Does this expression get the job done?"

**Decision tree:**
- Expression gets the job done → Finish and ship it (even if substrate/essence aren't perfect)
- Expression doesn't feel right or doesn't solve the problem → Go back and revise essence/substrate

**Avoid:** Letting perfect substrate or essence block useful, working expression.

### 2. Keep It Simple
**The rule:** Don't over-engineer the structure.

**Focus on:**
- What actually helps you organize and apply knowledge
- Discovering what works through use
- Core concepts and relationships, not perfect taxonomy

**Avoid:**
- Rigid naming schemes
- Overly prescriptive structure
- Treating this framework as a research tool rather than a working system

### 3. Relationships Matter More Than Labels
**The rule:** How ideas connect to each other matters more than the IDs or names you use.

**This means:**
- The specific ID format (S-0001 vs S-UUID vs timestamps) doesn't matter
- The relationships captured (supports, depends on, contradicts) are what create value
- You can restructure without losing the framework

### 4. Context Determines Everything
**The rule:** Answers to "how should I handle X?" depend on what expression you're creating.

**Questions to ask:**
- What am I building this for?
- Who will use this?
- What problem am I solving?

**Example:** Contradictory substrate facts might be *the point* (political analysis) or noise (building a spec). Context determines which.

---

## Common Questions

### Q: Should everything go into substrate first?
**A:** No. Start wherever makes sense for your use case. Personal knowledge management might start with essence (principles you live by). A decision might start with substrate (the facts you're deciding about). Let expression need drive the process.

### Q: What if I don't have perfect substrate?
**A:** That's fine. Create the essence claim and note what substrate would strengthen it. Come back later to fill gaps. The framework is for organizing what you know, not forcing premature perfection.

### Q: Can I have expressions that I'm not currently using?
**A:** Yes. You might generate a document and keep it as a potential expression without publishing it. It's value captured for later use.

### Q: What if essence and substrate contradict each other?
**A:** Preserve both. Contradictions often signal missing information, multiple valid perspectives, or context-dependency. Your essence can acknowledge the contradiction or resolve it based on what matters for your expression.

### Q: How do I know if my layers are working?
**A:** Ask:
- Can I trace essence claims back to substrate? (Contract 1)
- Can I generate different expressions from the same essence? (Contract 2)
- Does organizing knowledge this way actually improve my output?
- Am I spending time maintaining the structure or using it?

### Q: Can this framework work with large scale (thousands of entries)?
**A:** The framework itself can. Your implementation might change (database vs files, custom tools vs Obsidian, etc.). The core principle (three layers, clear boundaries, graph structure) remains.

---

## Getting Started

1. **Pick a small, real problem:** something you need to communicate, decide, or understand
2. **Capture substrate:** write down what you actually know about it (facts, data, evidence)
3. **Extract essence:** identify the key claims and relationships that emerge
4. **Generate an expression:** create the document, decision, or artifact you need
5. **Evaluate:** did this work? Did organizing knowledge this way improve the output?

That's it. The framework is discovered through use, not prescribed in advance.