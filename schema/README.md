# Persona Schema Documentation

This directory contains the schema definitions and examples for creating persona configurations in the awesome-mcp-personas registry.

## Overview

Each persona is defined by two required files:
1. **persona.yaml** - The persona definition including metadata, toolsets, and configuration
2. **mcp.json** - The MCP server configuration that provides the actual tools

## File Structure

```
personas/
└── [persona-name]/
    ├── persona.yaml    # Persona definition (required)
    ├── mcp.json       # MCP server configuration (required)
    └── README.md      # Documentation (recommended)
```

## Schema Files

### persona.schema.yaml
The YAML schema definition for `persona.yaml` files. This schema enforces:
- Required fields (name, description)
- Naming conventions (lowercase, hyphen-delimited)
- Toolset structure and tool ID format
- Optional metadata fields

### mcp.schema.json
The JSON schema definition for `mcp.json` files. This schema validates:
- MCP server configurations
- Command and argument structures
- Optional configuration objects

## Quick Start

### Creating a New Persona

1. **Create the persona directory:**
   ```bash
   mkdir personas/your-persona-name
   ```

2. **Create persona.yaml:**
   ```yaml
   name: your-persona-name
   description: A brief description of your persona's purpose
   version: "1.0"
   toolsets:
     - name: default
       toolIds:
         - servername.toolname
         - anotherserver.anothertool
   defaultToolset: default
   metadata:
     author: Your Name
     tags:
       - category1
       - category2
   ```

3. **Create mcp.json:**
   ```json
   {
     "mcpServers": {
       "servername": {
         "command": "servername-mcp",
         "args": ["--stdio"]
       },
       "anotherserver": {
         "command": "anotherserver-mcp",
         "args": ["--stdio"],
         "config": {
           "option": "value"
         }
       }
     }
   }
   ```

## Validation

### Validating persona.yaml

The persona.yaml file must:
- Have a `name` matching the directory name (lowercase, hyphen-delimited)
- Include a descriptive `description`
- Define toolsets with valid tool IDs (format: `servername.toolname`)
- Reference only MCP servers defined in the accompanying mcp.json

### Validating mcp.json

The mcp.json file must:
- Have a top-level `mcpServers` object
- Define each server with at minimum `command` and `args` properties
- Match server names referenced in persona.yaml toolsets

### Tool ID Format

Tool IDs follow the format: `<server-name>.<tool-name>`

Examples:
- `git.status` - The "status" tool from the "git" MCP server
- `docker.ps` - The "ps" tool from the "docker" MCP server
- `filesystem.read` - The "read" tool from the "filesystem" MCP server

The server name must correspond to a key in the mcp.json's `mcpServers` object.

## Examples

See the [example/](./example/) directory for a complete, valid persona configuration including:
- persona.yaml with multiple toolsets
- mcp.json with corresponding server definitions
- Demonstration of metadata fields
- Multiple toolset configurations

## Best Practices

1. **Naming Conventions:**
   - Use lowercase, hyphen-delimited names
   - Choose descriptive, specific names
   - Ensure directory name matches persona.yaml's `name` field

2. **Toolset Organization:**
   - Group related tools into logical toolsets
   - Provide a sensible default toolset
   - Consider different workflows when defining multiple toolsets

3. **Documentation:**
   - Always include a clear description
   - Add relevant tags for discoverability
   - Include author information for attribution
   - Document any special configuration requirements

4. **Version Management:**
   - Use semantic versioning (e.g., "1.0", "1.1", "2.0")
   - Update `lastModified` when making changes
   - Document breaking changes in persona README

## Schema Validation Tools

You can validate your persona files using standard YAML and JSON schema validators:

```bash
# Validate persona.yaml against schema
ajv validate -s schema/persona.schema.yaml -d personas/your-persona/persona.yaml

# Validate mcp.json against schema
ajv validate -s schema/mcp.schema.json -d personas/your-persona/mcp.json
```

## Support

For questions about the schema or help creating personas, please:
- Check the example configurations in [example/](./example/)
- Review existing personas in the registry
- Open an issue in the repository for clarification