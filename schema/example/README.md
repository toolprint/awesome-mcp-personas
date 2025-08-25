# Example Persona Configuration

This directory contains a complete, valid example of a persona configuration that demonstrates all the key features of the persona schema.

## Files

### persona.yaml
Demonstrates:
- Basic metadata (name, description, version)
- Multiple toolsets (development and testing)
- Tool ID format with server prefixes
- Default toolset selection
- Complete metadata including author, tags, and timestamps

### mcp.json
Demonstrates:
- Multiple MCP server configurations
- Different command patterns (direct commands vs npx)
- Standard I/O communication (`--stdio`)
- Optional configuration objects for servers
- Server names that match the prefixes in persona.yaml tool IDs

## Key Features Illustrated

### 1. Toolset Organization
The persona defines two logical toolsets:
- **development**: Core development tools (git, docker, filesystem)
- **testing**: Testing and coverage tools (jest, coverage)

### 2. Tool ID Convention
All tool IDs follow the `server.tool` format:
- `git.status` references the "status" tool from the "git" MCP server
- `filesystem.read` references the "read" tool from the "filesystem" MCP server

### 3. Server Configuration
The mcp.json shows different configuration patterns:
- Simple servers with just command and args (git, docker, filesystem)
- NPX-based servers for npm packages (jest)
- Servers with configuration objects (jest, coverage)

### 4. Metadata
Complete metadata demonstration including:
- Author attribution
- Categorization tags
- ISO 8601 timestamps for creation and modification

## Usage

To use this example as a template for your own persona:

1. Copy these files to a new directory under `personas/`
2. Update the `name` field to match your directory name
3. Modify the `description` to explain your persona's purpose
4. Define your own toolsets with relevant tool IDs
5. Configure the corresponding MCP servers in mcp.json
6. Update metadata with your information

## Validation

These files conform to:
- [persona.schema.yaml](../persona.schema.yaml) for the persona definition
- [mcp.schema.json](../mcp.schema.json) for the MCP configuration

You can validate your modifications using standard schema validators to ensure compliance.