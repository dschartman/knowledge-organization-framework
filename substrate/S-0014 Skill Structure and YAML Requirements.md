---
id: S-0014
date: 2025-10-25
author: @don.schartman
provenance: "Skill creation and review process; Anthropic Claude skills documentation"
tags: [skill-structure, yaml, frontmatter, metadata, documentation]
---

## Observations

- Every Claude skill requires a SKILL.md file with YAML frontmatter
- YAML frontmatter contains critical metadata: name, description
- Description field: Maximum 1024 characters, must answer two questions clearly: "What does this skill do?" and "When should I use it?"
- Description is the gate-keeper—if it doesn't communicate clearly, the LLM won't know whether to invoke the skill
- Skill directory structure: SKILL.md lives in skills/skill-name/ directory
- Skills can bundle multiple supporting files (markdown, scripts, reference materials)

## Progressive Disclosure Pattern

- Level 1 (Always loaded): YAML metadata (~100 tokens) - name, description
- Level 2 (Loaded on trigger): Core skill content in SKILL.md body - main instructions, core concepts, how to apply
- Level 3 (Loaded as needed): Supporting files - examples, templates, reference materials, scripts

## Content Organization for LLM Consumption

- LLMs work best with clear structure and explicit boundaries
- Hierarchical information (headings) helps LLMs navigate and prioritize
- Code blocks, examples, and structured lists improve comprehension
- Repetition and reinforcement help LLMs retain and apply concepts
- Clear "when to use" and "how to use" sections are essential
- Meta-commentary about how to read the skill itself can be helpful

## Word Choice Matters

- Every word builds upon previous words
- Strategic, efficient word choice creates better expressions
- Vague language (like "traceable") requires definition
- Technical terms need clear boundaries
- Consistency in terminology across the skill enables better understanding
- Removing unnecessary words focuses reader attention
