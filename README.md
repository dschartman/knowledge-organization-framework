# Knowledge Organization Framework

> **A framework for organizing knowledge with separation of concerns: what you know, what it means, and how you communicate or apply it.**

This framework helps you organize knowledge as a graph of facts, meanings, and relationships. It enables systematic writing, consistent decision-making, and clear thinking.

---

## What is This?

This repository contains a **knowledge organization framework** that separates concerns into three layers:

- **Substrate** (facts): Immutable observations and evidence with provenance
- **Essence** (meaning): Abstract principles, concepts, and their relationships derived from substrate
- **Expression** (application): Context-specific instantiations as documents, decisions, or actions

The framework is fundamentally a **knowledge graph**: concepts (nodes) connected by typed relationships (edges). How you implement it (file formats, directory structure, tools) is flexible and context-dependent.

**Meta-note:** This repository uses the framework to develop itself. The structure you see here is one expression of the framework's principles, not a prescription.

---

## Why Use This?

### Core Value

Knowledge organization creates value independent of any specific output. By separating facts from meaning from communication, you gain:

- **Traceability**: Every claim traces back to supporting evidence
- **Multiple uses**: Same knowledge → many different applications
- **Clarity**: Relationships between concepts become explicit
- **Maintainability**: Update facts or meaning; regenerate applications as needed
- **Consistency**: Decisions and communications aligned with stated principles

### What You Can Do

- **Systematic Writing**: Organize messy notes into clear, traceable documents
- **Decision-Making**: Build consistent frameworks traceable to data and values
- **Knowledge Synthesis**: Extract meaning from large volumes of information
- **Teaching**: Structure knowledge with proper concept ordering and dependencies
- **Living Principles**: Align actions with stated values; evolve based on experience

---

## Use Cases

### Resume Writing
**Problem:** 15 years of career history is too dense for a 1-2 page resume.

**Solution:**
- **Substrate:** All career facts (projects, metrics, skills, accomplishments)
- **Essence:** Key value propositions, professional persona, strongest claims
- **Expression:** Generate different resumes for different roles (data engineer vs. software engineer)

**Benefit:** Same facts, multiple targeted resumes. Every claim traceable to actual work.

### Decision Framework
**Problem:** Need consistent product prioritization across teams.

**Solution:**
- **Substrate:** User research, usage data, team capacity, past decisions
- **Essence:** Prioritization principles, success criteria, trade-off framework
- **Expression:** Actual prioritization decisions, documented rationale, team behaviors

**Benefit:** Decisions traceable to both principles and data. Learn from outcomes via meta-feedback.

### Personal Knowledge Management
**Problem:** Accumulating notes and experiences without clear organization.

**Solution:**
- **Substrate:** Observations, experiences, learnings, references
- **Essence:** Personal principles, concept relationships, what matters
- **Expression:** Blog posts, talks, project plans, daily decisions

**Benefit:** Knowledge compounds. Understanding deepens. Can teach what you've learned.

---

## Key Principles

### 1. Graph Structure is Core
The framework represents knowledge as a graph with nodes (concepts) and relationships (edges). Specific conventions (IDs, file formats) are implementation choices, not requirements.

### 2. Relationships Matter
Essence captures not just isolated concepts but how they relate and depend on each other. Order matters: concept B can't be explained before concept A if B depends on A.

### 3. Expression-Driven Development
Build what's useful, not what's perfect. The key question: **"Does it get the job done?"** Ship useful over perfect; iterate based on actual use.

### 4. Contradictions Are Features
Conflicting observations reflect reality. Contradictions signal missing information, nuance, or multiple valid perspectives. Don't force premature resolution.

### 5. Context Determines Everything
How you handle conflicts, what tools you use, what conventions you adopt: all depend on what you're building and for whom.

### 6. Implementation is Flexible
This repository's structure (directories, YAML, markdown) is **one expression** of the framework. Use what fits your context: Obsidian, Notion, graph database, plain text. All valid.

---

## Repository Structure

This repository practices what it preaches with a simple, flat structure:

```
substrate/
  S-0001 Framework Purpose.md
  S-0002 Resume Use Case.md
  S-0010 Agentic LLM Use Case.md
  ...

essence/
  E-0001 Core Framework Principles.md
  E-0002 Three-Layer Architecture.md
  E-0005 Graph Structure.md
  ...

expression/
  (optional directory for expressions)

Root level:
  README.md
  CLAUDE.md
```

All files are markdown with YAML frontmatter. Wiki-links (`[[S-0001 Framework Purpose]]`) create navigable relationships. No separate index files needed.

---

## Getting Started

### 1. Explore This Repository
- Read substrate entries in `substrate/` to see raw observations
- Read essence entries in `essence/` to see derived meaning
- Notice how essence claims use wiki-links to cite substrate (traceability)
- Open in Obsidian to see the knowledge graph

### 2. Try It Yourself

**Start with an expression** (like a messy document or pile of notes):

1. **Distill to substrate**: Extract factual observations with provenance
2. **Extract essence**: Identify principles, concepts, and relationships
3. **Check relationships**: What depends on what? What conflicts?
4. **Generate expression**: Create new artifact from essence for your audience

**Or start fresh:**

1. **Gather substrate**: Document observations as you learn/work
2. **Identify patterns**: What principles emerge? How do concepts relate?
3. **Capture essence**: Abstract the meaning; trace to substrate
4. **Apply**: Use organized knowledge to write, decide, or act

### 3. Choose Your Tools

- **Plain text**: Markdown files, any editor
- **Obsidian**: Knowledge graph visualization, backlinks, wiki-links
- **Notion**: Database views, rich formatting
- **Custom**: Whatever fits your workflow

The graph structure matters; the tool doesn't.

---

## Contributing

### This Repository Uses Itself

Contributions follow the framework's principles:

1. **Add substrate** (observed issues, new insights, research findings)
   - Create `S-XXXX Title.md` in `substrate/`
   - Include YAML frontmatter with provenance
   - Document factual observations

2. **Update essence** (new principles or relationship insights)
   - Modify or create `E-XXXX Name.md` in `essence/`
   - Use wiki-links to cite substrate: `[[S-0001 Framework Purpose]]`
   - Ensure all claims have supporting substrate

3. **Regenerate expressions** (when essence changes or gaps discovered)
   - Update framework documentation at root level
   - Add examples or use cases
   - Note meta-feedback for essence review

### Contribution Guidelines

- **Start with substrate**: New ideas need observations first
- **Trace to substrate**: Essence changes must cite supporting facts
- **Keep it simple**: Avoid over-engineering; discover through use
- **Question everything**: If conventions don't serve you, propose changes
- **Self-hosting mindset**: We're using the framework to develop the framework

### What We Value

- Clarity over cleverness
- Practical insights over theoretical perfection
- Traceability and transparency
- Learning through use
- Flexible implementation over rigid prescription

---

## Philosophy

This framework acknowledges several realities:

- **Expression as input is normal**: Knowledge enters as conversations and documents; we organize it from there
- **Repository structure is itself an expression**: There's a meta-paradox: we need expressions to organize knowledge about expressions
- **Conventions are tools, not rules**: Graph relationships matter more than ID formats
- **Errors are human**: Imperfections at each layer are acceptable; continuous improvement is the goal

We're discovering the framework through use, not prescribing it in advance.

---

## License

[Choose appropriate license]

---

## Acknowledgments

This framework draws inspiration from:
- Software engineering principles (separation of concerns, DRY)
- Knowledge management tools (Obsidian, Roam, Notion)
- Infrastructure-as-Code practices
- Research methods (citation networks, provenance)

Built through self-hosting: using the framework to develop the framework.

---

**Questions? Issues? Contributions?** Open an issue or submit a PR. Let's discover what works together.
