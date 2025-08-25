# Simpleton Persona

A simple example persona demonstrating basic MCP server configuration.

## Overview

The Simpleton persona is a minimal configuration that provides essential file system and git operations. It's perfect as a starting point for understanding how personas work or as a base for creating more complex personas.

## Target Audience

- New users learning about MCP personas
- Developers needing basic file and git operations
- Anyone looking for a minimal, clean configuration

## Included MCP Servers

### filesystem
- **Command**: `npx -y @modelcontextprotocol/server-filesystem`
- **Transport**: stdio (default)
- **Tools**:
  - `filesystem.read` - Read file contents
  - `filesystem.write` - Write file contents

### git
- **Command**: `npx -y @modelcontextprotocol/server-git`
- **Transport**: stdio (explicit)
- **Tools**:
  - `git.status` - Check repository status
  - `git.commit` - Create commits

## Installation

```bash
# Install hypertool-mcp if not already installed
npm install -g hypertool-mcp

# Use this persona
hypertool --persona simpleton
```

## Usage Examples

### Reading Files
The filesystem server allows you to read and write files in your project:
```
Read the contents of README.md
Write a new configuration file
```

### Git Operations
The git server provides basic version control:
```
Check the current git status
Commit changes with a descriptive message
```

## Customization

To customize this persona:

1. Fork or copy this directory
2. Modify `persona.yaml` to add more tool IDs
3. Update `mcp.json` to include additional MCP servers
4. Adjust the toolsets to match your workflow

## Troubleshooting

### Common Issues

**Issue**: MCP servers not starting
- **Solution**: Ensure you have Node.js and npm installed
- **Solution**: Check that npx can access the MCP server packages

**Issue**: Tools not available
- **Solution**: Verify the tool IDs in persona.yaml match the actual tools provided by the MCP servers
- **Solution**: Check that the MCP server names in mcp.json match the prefixes in tool IDs

## Contributing

This is an example persona. Feel free to:
- Use it as a template for your own personas
- Suggest improvements via pull requests
- Report issues if you find any problems