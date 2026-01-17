# Project Information

## 1. About this project

This project is a **Claude Code Plugin** that provides skills to synchronize Agent configurations between different Agent tools, such as Claude Code, VSCode, Claude Desktop, Codex, Cursor, Gemini CLI, and Antigravity.

The plugin includes two skills:

- **sync-mcp-config**: Synchronizes MCP (Model Context Protocol) server settings
- **sync-skill-config**: Synchronizes skill configurations

## 2. Directory Structure

This project follows the Claude Code plugin structure:

```text
sync-agent-config/
├── .claude/
│   └── CLAUDE.md            # Project instructions
├── .claude-plugin/
│   └── plugin.json          # Plugin manifest (required)
├── skills/
│   ├── sync-mcp-config/     # MCP config sync skill
│   │   ├── SKILL.md         # Skill definition
│   │   └── reference/       # Reference documentation
│   │       ├── antigravity.md
│   │       ├── claude_code.md
│   │       ├── claude_desktop.md
│   │       ├── codex_cli.md
│   │       ├── cursor.md
│   │       ├── gemini_cli.md
│   │       └── vscode.md
│   └── sync-skill-config/   # Skill config sync skill
│       ├── SKILL.md         # Skill definition
│       └── reference/       # Reference documentation
│           ├── antigravity.md
│           ├── claude_code.md
│           ├── codex_cli.md
│           ├── cursor.md
│           ├── gemini_cli.md
│           └── vscode.md
├── dist/                    # Release archives
├── LICENSE
├── README.md
└── README_ja.md
```

## 3. File Description

Markdown(.md) files in `skills/` directory should be written in English.

## 4. How to release plugin (How to create plugin zip file)

- Create archive file of the entire plugin.
- The zip file should include:
  - `.claude-plugin/` directory with `plugin.json`
  - `skills/` directory with all skill files
  - `LICENSE` file
- Name the archive file as `sync-agent-config-<version>.zip`, where `<version>` is the version number.
- Version number is read from `.claude-plugin/plugin.json` (`version` field).
- Zip file should be output to `dist` directory at the root of this repository.
