# /new-persona

Generate a new persona definition for the awesome-mcp-personas registry.

## Purpose

This command helps users create a new persona by walking through a structured Q&A process to gather requirements and generate the necessary configuration files following the project schemas.

## Process

### 1. Initial Questions

Ask the user these questions to understand their persona requirements:

**Q1: Basic Information**
- What is the name of your persona? (lowercase, hyphen-delimited, e.g., "data-scientist", "frontend-developer")
- Provide a brief description of this persona's purpose (10-500 characters)
- Who is the target audience for this persona?

**Q2: Work Domain**
- What type of work will this persona primarily do? (Choose one or more)
  - Software Development
  - Data Analysis
  - DevOps/Infrastructure
  - Content Creation
  - Security/Compliance
  - Research
  - Other (specify)

**Q3: Core Tools**
- What are the essential tools/capabilities this persona needs? (List key functionalities)
  - Version control (git)
  - File system operations
  - Language-specific tools (npm, pip, cargo, etc.)
  - Testing frameworks
  - Database access
  - API interactions
  - Cloud services
  - Other (specify)

**Q4: MCP Servers**
- Do you have specific MCP servers in mind? (If yes, list them)
- Should I research and suggest appropriate MCP servers based on your requirements? (Uses @mcp-researcher agent)

**Q5: Toolsets Organization**
- Do you want multiple toolsets for different workflows? (e.g., "development", "testing", "deployment")
- If yes, describe the different workflows/contexts

**Q6: Transport Preferences**
- What type of MCP server connections do you prefer?
  - stdio (standard I/O) - Default, most common
  - http (HTTP endpoints)
  - sse (Server-Sent Events)
  - Mixed (different servers use different transports)

### 2. File Generation

Based on the user's answers, generate the following files:

#### Directory Structure
```
personas/[persona-name]/
├── persona.yaml
├── mcp.json
└── README.md
```

#### persona.yaml
Generate according to `/schema/persona.schema.yaml`:
- Required: name, description
- Generate toolsets based on Q5 response
- Include toolIds in format "servername.toolname"
- Set defaultToolset if multiple toolsets exist
- Add metadata (author, tags, timestamps)

#### mcp.json
Generate according to `/schema/mcp.schema.json`:
- Create mcpServers object with server configurations
- Use appropriate transport type (stdio, http, sse)
- Include command and args for stdio servers
- Include url for http/sse servers
- Add env variables if needed

#### README.md
Generate documentation including:
- Persona name and description
- Target audience
- Prerequisites
- Installation instructions
- List of included MCP servers
- Available toolsets and their purposes
- Example workflows
- Troubleshooting tips

### 3. Validation & Auto-Fix

After generating files:
1. **Hand off to @persona-engineer** for comprehensive validation and auto-fix
2. The agent will:
   - Validate against schemas (persona.schema.yaml, mcp.schema.json)
   - Verify MCP server existence and tool names from primary sources
   - Auto-fix any issues found
   - Update docs/mcp-servers-used.md with new server usage
   - Create validation_notes.md with results

### 4. Integration with Workflow System

This command leverages the full persona workflow:

**Agent Integration:**
- **@mcp-researcher**: Discovers and validates MCP servers based on requirements
- **@persona-engineer**: Validates final configuration and applies auto-fixes

**Documentation Updates:**
- **docs/mcp-servers-used.md**: Automatically updated with new server usage
- **docs/mcp-servers.md**: Reference for server availability and installation
- **docs/future-roadmap.md**: Context for persona development priorities

**Schema References:**
- `/schema/persona.schema.yaml` - Persona configuration structure
- `/schema/mcp.schema.json` - MCP server configuration structure

## Example Interaction

```
User: /new-persona