---
id: S-0010
date: 2025-10-24
author: @don.schartman
provenance: "Framework development conversation; identifying primary use case and constraints"
tags: [use-case, agentic-llm, claude-code, workflow, tooling]
---

## Observations

- Primary use case is using framework with agentic LLMs (specifically Claude Code)
- User reviews LLM-produced markdown documents rather than creating them manually
- Agentic LLM analyzes substrate/essence and produces expressions
- Current workflow: VS Code for reading documents, Claude Code for analysis and generation
- Programmatic validation less critical because LLM handles relationship navigation
- Token efficiency could matter (simpler formats = less context needed)
- User is solo (currently no collaborators, though future collaboration possible)
- Scale target: tens to hundreds of entries, not thousands
- Git version control desired (public repository)
- User is very technically inclined
- Preference: minimal time on structure maintenance, more time using framework
- LLMs work well with markdown and can navigate file structures
- Human review is key step: LLM produces, human evaluates and refines

## Context

This represents a distinct use case from typical knowledge management:
- Not primarily human-authored content
- LLM as knowledge worker/analyst/synthesizer
- Human as reviewer/curator/decision-maker
- Structure needs to serve both LLM efficiency and human readability

## Implications for Organization

- Simple, consistent structure easier for LLM to navigate
- Markdown preferred (LLMs handle it well, git-friendly)
- Minimal nesting reduces LLM navigation complexity
- Clear conventions help LLM understand what goes where
- Human readability still matters (review step)
- Don't need validation scripts if LLM maintains relationships
- Git history provides version control and change tracking
- Obsidian compatibility could be valuable (human graph visualization)

## Contrast with Other Use Cases

Different from:
- **Manual knowledge base**: Human types everything (favor simplicity)
- **Team collaboration**: Multiple authors (favor structured validation)
- **Large scale**: Thousands of entries (favor database)
- **Research**: Heavy citation networks (favor specialized tools)

Similar to:
- **Personal research assistant**: LLM helps organize thoughts
- **Decision support**: LLM surfaces relevant knowledge for decisions
- **Writing assistant**: LLM drafts from organized knowledge
