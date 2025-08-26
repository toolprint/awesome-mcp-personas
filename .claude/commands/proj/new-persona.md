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

### 2. Initial README Generation

Based on user requirements, create a comprehensive README.md as the foundation:

#### Step 2a: Generate Initial README
Create directory and generate README.md using `/schema/README.template.md`:
```
personas/[persona-name]/
└── README.md (with persona requirements and use cases)
```

**README Content:**
- Persona name, description, and target audience from user input
- Core capabilities and workflow requirements  
- Placeholder sections for MCP servers (to be researched)
- Example use cases and workflow descriptions
- Prerequisites and setup structure

### 3. MCP Server Discovery

Hand off to @mcp-researcher to find appropriate MCP servers:

#### Step 3a: Research Delegation
**Delegate to @mcp-researcher** with these instructions:
- **Input**: Read the generated README.md to understand persona requirements
- **Task**: Research and identify 3-7 MCP servers that support the persona's use cases
- **Research Focus**: Find servers for each core capability mentioned by user
- **Validation**: Verify server existence and provide correct installation commands
- **Output**: Update README.md with discovered servers and capabilities

#### Step 3b: Expected Research Results
The @mcp-researcher will enhance the README.md with:
- Complete MCP server list with descriptions and sources
- Verified installation commands for each server
- Tool capabilities and integration examples
- Workflow-to-server mappings

### 4. Configuration Generation & Final Validation

Hand off to @persona-engineer for implementation and validation:

#### Step 4a: Implementation Delegation  
**Delegate to @persona-engineer** with these instructions:
- **Input**: Read the researched README.md with MCP server recommendations
- **Generate**: Create persona.yaml with proper toolsets based on discovered servers
- **Generate**: Create mcp.json with verified server configurations
- **Validate**: Use WebFetch to verify all tool names from official documentation
- **Auto-fix**: Correct any issues with server configs or tool references
- **Document**: Create validation_notes.md and update docs/mcp-servers-used.md

#### Step 4b: Final Deliverables
The @persona-engineer will produce:
- **persona.yaml**: Complete toolset definitions with verified tool IDs
- **mcp.json**: Validated server configurations with correct packages
- **Updated README.md**: Finalized documentation with accurate server information
- **validation_notes.md**: Documentation of all validation and fixes applied

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