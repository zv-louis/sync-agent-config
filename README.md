# sync-mcp-config

English | [日本語](README_ja.md)

A skill for synchronizing MCP (Model Context Protocol) server settings across different Agent tools.

## Overview

This project provides a skill that enables you to synchronize MCP server configurations between different Agent environments such as Claude Code, VSCode, Claude Desktop, Codex, and Gemini CLI.  
It reads the MCP configuration from a source Agent tool and applies it to a target Agent tool, ensuring consistent settings across multiple development environments.

## Features

- **Cross-Platform Support**:  
  Works on Windows, macOS, and Linux
- **Multi-Tool Compatibility**:  
  Supports various Agent tools including:
  - Claude Code
  - VSCode
  - Claude Desktop
  - Codex CLI
  - Gemini CLI
  - Antigravity
- **Safe Synchronization**:  
  Creates backups and validates configurations before applying changes
- **Intelligent Handling**:  
 Automatically handles format differences between different Agent tools
- **Web Search Integration**:  
 Automatically searches for configuration specifications when documentation is not available

## Installation

1. Download the latest release from the `dist` directory:  
  
   ```txt
   sync-mcp-config-<version>.zip
   ```

2. Install the skill according to your Agent tool's skill installation procedure.

## Usage

Simply tell your Agent to synchronize MCP settings between tools:

**Examples:**

- "I want to apply Claude Code's MCP settings to Codex"
- "Sync my MCP configuration from VSCode to Claude Desktop"
- "Copy MCP server settings from Claude Desktop to Claude Code"

The skill will:  

1. Verify your operating system environment
2. Read the source Agent tool's MCP configuration
3. Check available MCP servers
4. Apply the settings to the target Agent tool
5. Validate the configuration

## How It Works

1. **OS Environment Check**:  
  Detects your operating system and sets appropriate paths
2. **Configuration Verification**:  
  Reads and understands both source and target configuration formats
3. **Server Discovery**:  
  Identifies all MCP servers registered in the source configuration
4. **Format Conversion**:  
  Automatically converts settings to match the target tool's format
5. **Safe Application**:  
  Backs up existing configurations before making changes
6. **Validation**:  
  Ensures the new configuration is valid

## Configuration File Locations

The skill automatically detects configuration file paths based on your operating system and Agent tool. Reference documentation for each supported Agent tool is available in the [`sync-mcp-config/reference/`](sync-mcp-config/reference/) directory.

## Development

### Project Structure

```txt
sync-mcp-config/
├── SKILL.md              # Skill definition and procedures
├── VERSION               # Current version number
└── reference/            # Configuration reference documentation
    ├── antigravity.md
    ├── claude_code.md
    ├── claude_desktop.md
    ├── codex_cli.md
    ├── gemini_cli.md
    └── vscode.md
```

### Building a Release

To create a release archive:

1. The skill archive should include all files and subdirectories within the `sync-mcp-config` directory
2. Name the archive as `sync-mcp-config-<version>.zip`, where `<version>` matches the version in the [`sync-mcp-config/VERSION`](sync-mcp-config/VERSION) file
3. Output the zip file to the `dist` directory at the root of this repository

## Version

Current version: 0.5.1

## Safety Features

- **Backup Creation**:  
  Automatically backs up existing configurations before making changes
- **Conflict Detection**:  
  Identifies when servers are already registered and asks for user confirmation
- **Validation**:  
  Checks configuration file integrity after modifications
- **Read-Only Mode**:  
  Only modifies MCP server settings, leaving other configurations untouched

## Error Handling

The skill handles various error scenarios:  

- Missing source configuration files
- Write-protected target files
- Invalid configuration formats
- Incompatible settings between different Agent tools

## License

Please refer to the project license file for licensing information.
