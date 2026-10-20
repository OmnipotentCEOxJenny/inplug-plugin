---
name: build-a-plugin
description: Scaffold a new free plugin in the Cursor plugin format (manifest, skills, rules, README, CHANGELOG, MIT license, logo, optional MCP server). Use when a user wants to create, structure or package a plugin.
---

# Build a plugin

Follow `rules/pillars-and-scope.mdc`. Answer in the user's language; keep commands, file names and status labels unchanged. Source: https://cursor.com/docs/plugins (read 2026-10-20).

1. **Layout (Cursor Plugin):** `.cursor-plugin/plugin.json`, `rules/*.mdc`, `skills/<name>/SKILL.md`, optional `mcp.json`. The manifest needs only `name`; add `displayName`, `version`, `description`, `author`, `license`, `repository`, `logo`. An Agent Plugin (open standard) instead has a root `plugin.json`. In `mcp.json` use `${CURSOR_PLUGIN_ROOT}` for the plugin root.
2. **Skills:** each `SKILL.md` starts with YAML front-matter holding `name` (matches the folder) and `description` (what it does and when to use it).
3. **Rules:** `.mdc` files with front-matter `description` and `alwaysApply`.
4. **Docs:** README (title, description, logo at top, quick start, testing, credits, honest limits), CHANGELOG, LICENSE (MIT), `assets/logo.png` (square, for example 1024x1024).
5. **MCP server (optional):** the MCP Python SDK 2.x renamed FastMCP. Use `from mcp.server.mcpserver import MCPServer`; `mcp.server.fastmcp` raises an error in 2.3.0 (checked in the 2.3.0 wheel on 2026-10-20). Pin versions in install steps, for example `pip install "mcp==2.3.0"`, or pin `mcp<2` for v1 code.
6. **Test locally:** copy the folder to `~/.cursor/plugins/local/<name>`, reload the window, and confirm the components appear in Customize.

Output the file tree and each file's contents. Mark anything not checked against official docs UNVERIFIED.
