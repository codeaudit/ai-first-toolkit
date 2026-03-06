# TechWolf AI-First Toolkit

Open-source AI skills, plugins, and MCP servers from [TechWolf](https://techwolf.com)'s [AI-First Engineering](https://ai-first.techwolf.ai) program.

This repository is a **plugin marketplace** for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) and provides **MCP servers** for Cursor, Windsurf, and other AI coding tools.

## Available Plugins

| Plugin | Description | Status |
|--------|-------------|--------|
| [ai-firstify](plugins/ai-firstify/) | AI-first project auditor and re-engineer based on the 9 design principles and 7 design patterns from the TechWolf AI-First Bootcamp | Available |
| [content-studio](plugins/content-studio/) | Content studio for thought leadership (LinkedIn, blog, opinion) with visual editor and Claude Code skills | Available |

## Installation

### Claude Code (Recommended)

Add the marketplace and install any plugin:

```bash
# Add the TechWolf marketplace (once)
claude plugin marketplace add techwolf-ai/ai-first-toolkit

# Install a specific plugin
claude plugin install ai-firstify@techwolf-ai-first
claude plugin install content-studio@techwolf-ai-first
```

### Cursor / Windsurf / Other MCP Clients

Coming soon -- MCP server versions of our plugins for use with any MCP-compatible client.

## Contributing

We welcome contributions! Whether it's a bug fix, a new skill, or an improvement to an existing plugin — feel free to open an issue or submit a pull request.

### Adding a New Plugin

Each plugin lives in `plugins/<plugin-name>/` and follows this structure:

```
plugins/my-plugin/
├── .claude-plugin/
│   └── plugin.json       # Plugin manifest
├── skills/               # Agent skills (SKILL.md files)
├── agents/               # Specialized subagents (optional)
├── hooks/                # Event handlers (optional)
├── .mcp.json             # MCP server config (optional)
├── src/                  # MCP server source code (optional)
├── package.json          # For NPM publishing (optional)
└── README.md             # Plugin documentation
```

## License

[MIT](LICENSE)

---

Built by [TechWolf](https://techwolf.com) as part of the [AI-First Engineering](https://ai-first.techwolf.ai) program.
