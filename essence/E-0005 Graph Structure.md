---
id: E-0005
type: essence
name: Graph Structure as Core Organizing Principle
version: 1.0
date: 2025-10-24
tags: [graph, structure, implementation, flexibility]
---

# Graph Structure as Core Organizing Principle

## Claim: Framework is fundamentally a knowledge graph

The framework is fundamentally a knowledge graph with nodes (concepts) and directed, typed edges (relationships).

**Supports:** [[S-0006 Knowledge Graph Structure]], [[S-0007 Essence Relationships]], [[S-0009 Graph Over Conventions]]

**Rationale:** S-0006 recognizes the underlying graph structure. S-0007 establishes that relationships are essential. S-0009 clarifies graph structure is core, not specific conventions.

## Claim: Graph structure exists across all layers

Graph structure exists across all three layers: substrate facts relate to each other, essence concepts have dependencies, expressions reference essence.

**Supports:** [[S-0006 Knowledge Graph Structure]], [[S-0007 Essence Relationships]]

**Rationale:** S-0006 notes hierarchical graph with relationships within and between layers. S-0007 shows concept relationships are critical.

## Claim: Naming conventions are implementation expressions

Specific naming conventions (IDs, directory structure, file formats) are implementation expressions, not core framework requirements.

**Supports:** [[S-0008 Repository as Expression]], [[S-0009 Graph Over Conventions]]

**Rationale:** S-0008 establishes repository structure is itself an expression. S-0009 clarifies conventions are implementation choices, not core principles.

## Claim: Relationships matter more than labels

The relationships between concepts matter more than the labels or IDs used to reference them.

**Supports:** [[S-0007 Essence Relationships]], [[S-0009 Graph Over Conventions]]

**Rationale:** S-0007 establishes relationships are as important as concepts themselves. S-0009 states relationships matter more than labels.

## Claim: Different tools can represent the same graph

Different tools and formats can represent the same underlying knowledge graph (Obsidian, graph databases, plain markdown, etc.).

**Supports:** [[S-0006 Knowledge Graph Structure]], [[S-0009 Graph Over Conventions]]

**Rationale:** S-0006 explores multiple representation options (Obsidian, Neo4j, plain text). S-0009 notes graph exists regardless of how you label nodes or format files.

## Claim: Repository structure is an expression

Repository structure is an expression of the framework, not the framework itself. Implementation choices should fit context.

**Supports:** [[S-0008 Repository as Expression]], [[S-0009 Graph Over Conventions]]

**Rationale:** S-0008 recognizes repository structure is itself an expression. S-0009 states implementation details should be examples, not requirements.

---

## Graph Properties

### Nodes
- **Substrate:** Observable facts, experiences, data points
- **Essence:** Concepts, principles, claims, relationships
- **Expression:** Documents, decisions, actions, artifacts

### Edges (Directed, Typed)
- **Supports:** Essence claims → Substrate facts (verifiable)
- **Derives from:** Expression → Essence concepts (representational)
- **Relates to:** Within-layer concept relationships
- **Depends on:** Ordering dependencies (concept A before B)
- **Contradicts:** Conflicting claims (preserved, not resolved)

### Structure
- **Layered:** Hierarchical (Substrate → Essence → Expression)
- **Directed:** Edges have direction (mostly acyclic between layers)
- **Typed:** Different relationship types have different semantics
- **Flexible:** Within layers, more freedom for bidirectional references

---

## Implementation Flexibility

### ID Conventions
**Examples:** S-XXXX sequential IDs, timestamps, UUIDs, semantic names, no IDs with wiki-links only

**Principle:** Choose what fits your context. Consistency within project matters more than specific format.

### File Formats
**Examples:** Markdown + YAML, JSON, Obsidian notes, Notion database, Graph database

**Principle:** Format should enable human readability and machine validation for your needs.

### Directory Structure
**Examples:** layers/substrate/registry/, flat with tags, nested by topic, database tables

**Principle:** Organize for your access patterns. Structure is an expression choice.

### Tools
**Examples:** Plain text editors, Obsidian, Notion, Roam, Neo4j, custom tools

**Principle:** Tool should help you see and navigate the graph. No single right answer.

---

## Validation Focus

### What Matters
- Are relationships clear and navigable?
- Can you trace essence to substrate?
- Does structure represent the knowledge graph faithfully?
- Is it usable for your context?

### What Matters Less
- Exact ID format used
- Specific directory naming
- Choice of markdown vs. JSON vs. database
- Following a prescribed convention

---

## Trade-offs

### Prescriptive Approach
**Pros:** Easy to start, clear guidance, consistency, automation

**Cons:** Feels rigid, obscures core principles, one-size-fits-all

**When:** Early exploration, need structure, team alignment

### Flexible Approach
**Pros:** Fits context, core principles visible, encourages understanding

**Cons:** Requires thinking, less immediate guidance, inconsistency risk

**When:** Mature understanding, unique context, evolving needs

**Recommended:** Start with examples (like this repo's structure) but recognize them as expressions, not requirements. Adapt as needed.

---

## Key Terms

**Knowledge Graph:** A data structure of nodes (concepts) and edges (relationships) representing organized knowledge with semantic meaning.

**Directed Edge:** A relationship with a direction (A → B is different from B → A).

**Typed Edge:** A relationship with a semantic type (supports, derives_from, depends_on, etc.).

**Acyclic:** No circular references that violate layer boundaries (essence can't support substrate, for example).
