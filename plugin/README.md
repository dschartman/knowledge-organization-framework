# Regenerative Writing Framework Plugin

A Claude Code plugin for the Regenerative Writing Framework - a self-hosting knowledge organization system that separates facts (substrate), meaning (essence), and communication (expression).

## Structure

```
plugin/
├── .claude-plugin/
│   ├── plugin.json              # Main plugin manifest
│   ├── commands/                # Custom slash commands
│   ├── agents/                  # Specialized subagents
│   └── skills/                  # Agent Skills
└── README.md                    # This file
```

## Components

### Commands
Custom slash commands for working with the framework. Place `.md` files with YAML frontmatter in `commands/`.

Example: `commands/create-substrate.md` for creating new substrate entries.

### Agents
Specialized subagents for specific tasks. Configure in `agents/` directory.

Example: Agents for analyzing substrate relationships or generating essence summaries.

### Skills
Agent Skills that extend Claude's capabilities. Include `SKILL.md` with YAML frontmatter in `skills/`.

Example: A skill for organizing knowledge graph structures or validating wiki-links.

## Development

1. Add new commands, agents, or skills to their respective directories
2. Test locally with Claude Code
3. Debug with `claude --debug` to inspect plugin loading

## Distribution

The plugin is distributed through the marketplace configured at `.claude-plugin/marketplace.json` in the repository root.

To add this marketplace to Claude Code:
```
/plugin marketplace add https://github.com/[your-username]/regenerative-writing-framework.git
```

## Updating the Marketplace URL

Before publishing, update the source URL in `.claude-plugin/marketplace.json` to point to your actual GitHub repository.
