---
name: "find-mcp"
description: "Find MCP servers based on criteria and purpose, research and update registry"
---

# Find MCP Server

Discover MCP servers matching specific criteria and use cases, then research and update the server registry.

## Usage

```bash
/find-mcp [purpose or criteria]
```

## Examples

```bash
# Find database-related MCP servers
/find-mcp database integration for data analysis

# Find authentication servers  
/find-mcp user authentication and authorization

# Find UI testing tools
/find-mcp browser automation and frontend testing
```

## Workflow

1. **Analysis**: Parse the purpose/criteria to understand requirements
2. **Brief Creation**: Generate research brief with search strategy  
3. **Handoff**: Delegate to @mcp-researcher with the research brief
4. **Research & Update**: Agent discovers servers and updates docs/mcp-servers.md

The @mcp-researcher agent will handle server discovery, validation, and documentation updates.