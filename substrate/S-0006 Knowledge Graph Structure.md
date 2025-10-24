---
id: S-0006
date: 2025-10-24
author: @don.schartman
provenance: "Framework development conversation; recognition of underlying graph structure"
tags: [knowledge-graph, data-structure, obsidian, visualization, relationships]
---

## Observations

- The framework represents a knowledge graph: nodes (substrate/essence/expression entries) with directed, typed edges (supports, derives_from, cites)
- Current representation uses ID arrays in YAML frontmatter: `supports: [S-0001, S-0005]`
- IDs are opaque; you must look up what "S-0005" means to understand relationships
- No automatic bidirectional visibility; substrate doesn't know what essence references it without checking all essence files
- Graph has hierarchical structure: Substrate → Essence → Expression (directed, mostly acyclic)
- Within layers, nodes can reference each other more freely
- Obsidian note-taking tool uses wiki-links `[[note-name]]` to create relationships between markdown files
- Obsidian automatically generates backlinks showing reverse relationships
- Obsidian provides visual graph view of all linked notes
- Obsidian still stores everything as plain markdown files on disk
- Using descriptive filenames (e.g., `S-0001-framework-purpose.md`) makes references more readable
- Could use wiki-links in addition to YAML ID arrays for human readability
- Tags create another dimension of relationships (e.g., all entries tagged `#knowledge-organization`)
- Graph structure enables queries like "show all essence claims supported by S-0001" or "show everything that derives from E-0002"

## Trade-offs Considered

**ID Arrays (current approach):**
- Simple and explicit
- Machine-parseable for validation
- Works in any text editor
- But: opaque, no auto-backlinks, manual index maintenance

**Wiki-links (Obsidian-style):**
- Human-readable (file names visible)
- Automatic backlinks and graph
- Hover previews in supporting tools
- But: requires compatible tool, links break on file rename

**Hybrid approach:**
- Keep ID arrays for validation
- Add wiki-links in prose for readability
- Get both machine validation and human readability
- Slight duplication but valuable

**Graph database (Neo4j, etc.):**
- Native graph storage and queries
- But: major complexity increase, loses plain text simplicity, premature optimization

## Concerns Raised

- Don't want to overcomplicate early
- Readability and human review is important
- Markdown preference should be maintained
- Need better way to represent and visualize relationships
- Current approach feels manual and disconnected

## Parallels

Framework structure is similar to:
- Obsidian knowledge graphs
- Academic citation networks
- Software dependency graphs
- RDF/linked data
- Property graphs in Neo4j

## Opportunities

- Could make repository immediately usable in Obsidian
- Could generate graph visualizations from YAML metadata
- Could provide backlink views (what references this entry?)
- Could query graph structure (impact analysis: what changes if S-0001 changes?)
- Validation can check graph properties (no cycles violating layer boundaries, all essence cites substrate, etc.)
