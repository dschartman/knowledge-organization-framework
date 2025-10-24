---
id: S-0009
date: 2025-10-24
author: @don.schartman
provenance: "Framework development conversation; clarification that graph structure is core, not specific conventions"
tags: [graph-structure, conventions, traceability, flexibility, implementation]
---

## Observations

- The core value is concept relationships (graph structure), not specific naming conventions
- Original emphasis on traceability/validation came from software engineering reproducibility needs (Infrastructure-as-Code, Nuke-and-Pave)
- This framework has evolved to be more general than Infrastructure-as-Code approaches
- Specific conventions (S-XXXX IDs, directory structure, YAML format) are implementation expressions, not core framework
- Graph structure exists regardless of how you label nodes or format files
- ID conventions like S-XXXX are helpful but not mandatory
- The relationships between concepts matter more than the labels used for them
- Different implementations could use different conventions (timestamps, UUIDs, semantic names, no IDs at all)
- Graph databases, Obsidian, plain markdown—all can represent the same underlying knowledge graph
- Prescriptive conventions can obscure the core principle: knowledge has relationships that form a graph

## Context

When reviewing "missing substrate," it became clear that much of the original scaffold was prescriptive implementation details (validation rules, directory structure requirements, ID format specifications). These were attempts to make the framework "concrete" but risked confusing implementation with core concepts.

The framework is about organizing knowledge with separation of concerns and graph relationships. How you implement that is context-dependent.

## Trade-offs

**More prescriptive (original approach):**
- Easier to get started (clear "right way")
- Validation can be automated
- Consistency across implementations
- But: can feel rigid, discourages experimentation, confuses implementation with essence

**Less prescriptive (current recognition):**
- Flexible for different contexts
- Core principles more visible
- Acknowledges implementation as expression
- But: requires more thinking, less immediate guidance, harder to automate validation

## Implications

- Framework documentation should emphasize graph structure and separation of concerns
- Specific conventions (IDs, directories, formats) should be presented as examples, not requirements
- Repository structure is one expression of the framework, not THE framework
- Users can adopt conventions that fit their context (Obsidian, Notion, graph database, plain text)
- Validation rules are implementation concerns, not core framework
- The question "does this structure represent the knowledge graph clearly?" matters more than "did I follow the ID convention?"
