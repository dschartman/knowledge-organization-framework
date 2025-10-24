# Claude Code Context: Knowledge Organization Framework

## What This Is
A self-hosting knowledge organization framework that separates facts (substrate), meaning (essence), and communication (expression). Uses itself to develop itself.

## Repository Structure

```
substrate/          # S-XXXX: Observable facts with provenance
essence/            # E-XXXX: Principles, concepts, relationships
expression/         # Optional: Generated documents
Root files          # Expressions (README, docs, etc.)
```

All files are **markdown with YAML frontmatter**. Relationships via **wiki-links** (`[[S-0001 Framework Purpose]]`).

## Key Concepts

**Three Layers:**
- **Substrate**: Immutable observations, no interpretation
- **Essence**: Abstract meaning derived from substrate (traceable via wiki-links)
- **Expression**: Context-specific instantiation (documents, decisions, actions)

**Navigation:**
- Substrate files start with `S-XXXX`
- Essence files start with `E-XXXX`
- Wiki-links show relationships: `[[S-0001 Framework Purpose]]`
- No index files needed (wiki-links ARE the index)

**Graph Structure:**
- Framework is fundamentally a knowledge graph
- Essence claims cite substrate via wiki-links
- Expressions derive from essence
- Repository structure itself is an expression

## Tooling

**Python:**
- Use `uv` for Python package management
- Add dependencies: `uv add <package>`
- Run scripts: `uv run <script>`

**Git:**
- Repository is version controlled
- Commit prefixes: `substrate:`, `essence:`, `expression:`

## Working Sessions

**Adding substrate:** Create `substrate/S-XXXX Title.md` with YAML frontmatter (id, date, author, provenance, tags)

**Adding essence:** Create `essence/E-XXXX Name.md` with claims citing substrate via wiki-links

**Creating expressions:** Derive from essence, document what essence supports it

**Finding information:**
- Search for `S-XXXX` or `E-XXXX` IDs
- Follow wiki-links to navigate
- Grep for concepts or tags

## Philosophy (Context for Decisions)

- **Expression-driven**: Build what's useful, not what's perfect
- **Contradictions okay**: They reflect reality, don't force resolution
- **Context matters**: Implementation choices fit the use case
- **Keep it simple**: Structure serves content, not vice versa
- **Repository structure is an expression**: Can evolve based on what works

## Current State

- 10 substrate entries (S-0001 through S-0010)
- 5 essence entries (E-0001 through E-0005)
- Multiple expressions at root level
- Recently migrated to simplified structure

## This File's Purpose

This file is an **expression** optimized for Claude Code cold starts. It's intentionally minimal and high-density. For comprehensive understanding, see other documentation.
