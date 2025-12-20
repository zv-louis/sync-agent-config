# Project Information

## 1. About this project

This project provides a skill to synchronize MCP (Model Control Platform) server settings between different Agent tools, such as Claude Code and Codex.  
It reads the MCP configuration from a source Agent tool and applies it to a target Agent tool, ensuring consistent settings across multiple environments.

## 2. Directry Location

The skill is located in the `sync-mcp-config` directory.

## 3. File Description

Markdown(.md) files in sync-mcp-config directory should be written in English.  

## 4. How to release skill (How to create skill zip file)

- Create archive file including `sync-mcp-config` directory.
- compress the `sync-mcp-config` directory into a zip file.
- zip file should include all files and subdirectories within `sync-mcp-config` directory.
- Name the archive file as `sync-mcp-config-<version>.zip`, where `<version>` is the version number of the skill.
- version number is read from `sync-mcp-config/VERSION` file.
- zip file should be output to `dist` directory at the root of this repository.
