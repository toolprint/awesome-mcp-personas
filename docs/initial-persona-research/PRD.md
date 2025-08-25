# Persona Content Pack (MCP)

This package contains **Model Context Protocol (MCP)** configurations and persona definitions
(Claude-code style) designed to speed up common workflows across multiple roles (personas).

## What’s inside

- `personas/<persona-name>/mcp.json` — MCP server launcher config for the persona’s server set.
  - Uses **remote runners** (no local project checkout required):
    - Node/TS servers via `npx`
    - Python servers via `uvx` (from `uv`)
  - Environment variables use `"<placeholder>"` tokens.
- `personas/<persona-name>/persona.yaml` — the AI persona definition and its **toolsets**:
  - `name`: hyphenated, lower-case
  - `description`: one-paragraph summary
  - `toolsets[]`:
    - `name`: hyphenated, lower-case (theme, not a single narrow task)
    - `description`: short paragraph + examples
    - `tools[]`: list of **namespaced tool names** in the form `server.tool`
    - `_meta.tags.categories`: list of tags describing the theme
  - `_meta`: persona-level metadata
    - `definition_link`: upstream persona reference (e.g., registry)
    - `tags.categories`: union of toolset theme tags

> We intentionally **omit per-tool source URLs** and **omit `_meta.servers`** at persona level
  to keep the persona files compact and runner-agnostic. Server install docs live in their
  respective GitHub repos/registries.

## Naming conventions

- Personas: `hyphenated-lowercase`, typically ending with `-assistant`.
- Toolsets: `hyphenated-lowercase`.
- Tool names: `server.tool` (exact MCP tool name from the server).

## Runners

- **Node** MCP servers are executed with: `npx <mcp-package>`
- **Python** MCP servers are executed with: `uvx <mcp-console-script>`

> You’ll need `npm` (for `npx`) and `uv` (for `uvx`) available in your environment.

## Adding a new persona

1. Create a folder: `personas/<persona-name>/`
2. Add:
   - `mcp.json` (servers + env placeholders)
   - `persona.yaml` (description + themed toolsets + tools)
3. Validate:
   - tool names exist on the referenced MCP servers
   - `persona.yaml` meets schema rules above

## PR guidelines

- One persona per PR keeps review focused.
- Include a short PR body:
  - Persona name and purpose
  - Summary of server set and toolsets
  - Notes on environment variables required

## Security / Secrets

- Never commit secrets.
- `mcp.json` must only contain `"<placeholder>"` tokens for env vars.
- Reference server env requirements in the persona description or PR body, not in the repo.
