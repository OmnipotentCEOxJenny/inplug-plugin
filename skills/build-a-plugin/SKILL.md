---
name: build-a-plugin
description: Scaffold a new free plugin in the Cursor plugin format (manifest, skills, rules, README, CHANGELOG, MIT license, logo, optional MCP server). Use when a user wants to create, structure or package a plugin.
---

# Build a plugin

Follow `rules/pillars-and-scope.mdc`. Answer in the user's language; keep commands, file names and status labels unchanged. Source: https://cursor.com/docs/plugins (read 2026-10-20).

1. **Layout (Cursor Plugin):** `.cursor-plugin/plugin.json`, `rules/*.mdc`, `skills/<name>/SKILL.md`, optional `mcp.json`. The manifest needs only `name`; add `displayName`, `version`, `description`, `author`, `license`, `repository`, `logo`. An Agent Plugin (open standard) instead has a root `plugin.json`. In `mcp.json` use `${CURSOR_PLUGIN_ROOT}` for the plugin root.
2. **Skills:** each `SKILL.md` starts with YAML front-matter holding `name` (matches the folder) and `description` (what it does and when to use it).
3. **Rules:** `.mdc` files with front-matter `description` and `alwaysApply`.
   - YAML trap: a value containing ": " (colon + space) must be quoted, for example `description: "Scope: notes only"`, or the front-matter fails to parse. Validate every front-matter block with a YAML parser.
4. **Docs:** README (title, description, logo at top, quick start, testing, credits, honest limits), CHANGELOG, LICENSE (MIT), `assets/logo.png` (square, for example 1024x1024).
5. **MCP server (optional):** the MCP Python SDK 2.x renamed FastMCP. Use `from mcp.server.mcpserver import MCPServer`; `mcp.server.fastmcp` raises an error in 2.3.0 (checked in the 2.3.0 wheel on 2026-10-20). Pin versions in install steps, for example `pip install "mcp==2.3.0"`, or pin `mcp<2` for v1 code.
6. **Test locally without marketplace approval:**
   - Cursor (https://cursor.com/docs/plugins): copy the folder to `~/.cursor/plugins/local/<name>`, run Developer: Reload Window, and confirm the components appear in Customize. Needs the Cursor app; on Teams/Enterprise an admin setting can block local imports.
   - Grok Build CLI (https://github.com/xai-org/grok-build, user guide 09-plugins): `grok plugin install owner/repo --trust` or a local path. UNVERIFIED: whether it reads a `.cursor-plugin/plugin.json` manifest; check its docs. Only install sources you trust.
   - Grok Bot (chat app): no documented way to install an unlisted plugin was found (checked 2026-10-20); UNVERIFIED.

Output the file tree and each file's contents. Mark anything not checked against official docs UNVERIFIED.
