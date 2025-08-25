# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a curated registry of persona-based MCP (Model Context Protocol) server configurations. Each persona bundles together MCP servers and tools optimized for specific professional roles or use cases, similar to installable packages or specialized Claude subagents.

## Repository Structure

```
awesome-mcp-personas/
├── personas/               # All persona definitions
│   ├── [persona-name]/    # Individual persona directory
│   │   ├── mcp.json       # MCP server configuration (required)
│   │   ├── README.md      # Persona documentation (required)
│   │   ├── tools.md       # Tool reference guide (required)
│   │   └── examples/      # Usage examples (optional)
├── README.md              # Main registry listing
├── CONTRIBUTING.md        # Contribution guidelines
└── LICENSE               # Repository license
```

## Key Standards

### Persona Definition Requirements

Every persona MUST include:
1. **mcp.json** - Valid MCP server configuration following the Model Context Protocol specification
2. **README.md** - Clear documentation explaining the persona's purpose, target audience, and key capabilities
3. **tools.md** - Comprehensive list of available tools and their usage

### MCP Configuration Format

```json
{
  "mcpServers": {
    "server-name": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-package"],
      "config": {
        // Server-specific configuration
      }
    }
  }
}
```

## Common Development Tasks

### Adding a New Persona

1. Create directory: `personas/[persona-name]/`
2. Add required files: mcp.json, README.md, tools.md
3. Validate JSON configuration syntax
4. Update main README.md with the new persona entry in the appropriate category
5. Ensure the persona listing includes: name, description, MCP servers list, key features, and best use cases

### Validating Persona Configurations

When reviewing or adding personas, verify:
- JSON syntax is valid in mcp.json
- All referenced MCP servers exist and are publicly available
- Configuration keys match the server's expected schema
- No duplicate server definitions within a persona
- Server combinations make logical sense for the stated use case

### Categories for Organization

Personas should be organized into these primary categories:
- Software Engineering (language-specific and framework-specific dev tools)
- Data Science & Analytics (data processing, ML, visualization)
- DevOps & Infrastructure (cloud, containers, monitoring)
- Content & Documentation (writing, editing, publishing)
- Security & Compliance (scanning, auditing, hardening)
- Research & Analysis (information gathering, processing)

### README.md Updates

When updating the main README:
- Maintain alphabetical order within categories
- Use consistent emoji indicators for visual recognition
- Include brief (1-2 line) descriptions
- List 3-5 key MCP servers for each persona
- Specify primary use cases

## Quality Guidelines

### Persona Quality Criteria

- **Specificity**: Target a clear, well-defined use case or professional role
- **Completeness**: Include all essential tools for the stated purpose
- **Compatibility**: Ensure MCP servers work well together without conflicts
- **Documentation**: Provide clear, actionable documentation with examples
- **Testability**: Configuration should be directly usable without modifications

### Documentation Standards

Each persona README should include:
1. Purpose statement
2. Target audience
3. Prerequisites or requirements
4. Installation instructions specific to the persona
5. List of included MCP servers with brief descriptions
6. Common workflows or use cases
7. Troubleshooting section for known issues

## File Validation Patterns

### JSON Validation
- Check for valid JSON syntax
- Verify required "mcpServers" top-level key
- Ensure each server has "command" and "args" properties
- Validate optional "config" objects match server requirements

### Markdown Validation
- Check for proper heading hierarchy
- Verify all links are valid (internal and external)
- Ensure code blocks have appropriate language tags
- Validate that required sections are present