# Claude Code Assistant - Tools Reference

This document provides a comprehensive reference of all available tools in the Claude Code Assistant persona, organized by toolset.

## Development Toolset

### Everything Server Tools
**Server**: @modelcontextprotocol/server-everything  
**Transport**: stdio via npx

- **everything.read_file**: Read file contents with encoding support
- **everything.write_file**: Write content to files with proper encoding  
- **everything.list_files**: List directory contents with filtering options
- **everything.run_command**: Execute shell commands and system operations

### Git Server Tools  
**Server**: mcp-server-git  
**Transport**: stdio via uvx

- **git.git_status**: Check repository status and working directory state
- **git.git_log**: View commit history with formatting options
- **git.git_diff**: Compare changes between commits, branches, or working directory  
- **git.git_add**: Stage changes for commit with path specifications
- **git.git_commit**: Commit staged changes with message and options
- **git.git_branch**: Manage branches, create, delete, and switch operations

## Visual Context Toolset

### Playwright Server Tools
**Server**: @playwright/mcp  
**Transport**: stdio via npx

- **playwright.screenshot**: Capture screenshots of browser tabs and web pages
- **playwright.navigate**: Navigate to URLs with wait conditions and options
- **playwright.evaluate**: Execute JavaScript code in browser context
- **playwright.click**: Click elements and interact with UI components

## Workflow Orchestration Toolset

### Task Master Server Tools
**Server**: task-master-ai  
**Transport**: stdio via npx

- **task-master.create_task**: Create and organize development tasks with dependencies
- **task-master.update_task**: Update task status, progress, and metadata
- **task-master.list_tasks**: View and filter task lists with status filtering
- **task-master.complete_task**: Mark tasks complete and update dependency chains

### MCPing Server Tools  
**Server**: @toolprint/mcping-mcp  
**Transport**: stdio via npx

- **mcping.send_notification**: Send notifications and alerts for development events
- **mcping.get_status**: Check notification delivery status and history

## Intelligence Analysis Toolset

### Sequential Thinking Server Tools
**Server**: @modelcontextprotocol/server-sequential-thinking  
**Transport**: stdio via npx

- **sequential-thinking.think**: Apply structured reasoning to complex development problems

### Context7 Server Tools
**Server**: Context7 (SSE)  
**Transport**: sse via https://mcp.context7.com/sse

- **context7.resolve-library-id**: Find Context7-compatible library identifiers
- **context7.get-library-docs**: Retrieve official documentation and patterns

## Deployment Operations Toolset

### Docker Server Tools
**Server**: mcp-server-docker  
**Transport**: stdio via uvx

- **docker.build_image**: Build Docker images from Dockerfiles with build context
- **docker.run_container**: Run containers with configuration and port mapping
- **docker.list_containers**: List running and stopped containers with filtering
- **docker.list_images**: List available Docker images with metadata
- **docker.get_logs**: Retrieve logs from running containers with options
- **docker.exec_command**: Execute commands inside running containers

## Research Documentation Toolset

### Exa Server Tools
**Server**: mcp-remote + exa.ai  
**Transport**: stdio via npx  
**Environment**: Requires EXA_API_KEY

- **exa.search**: Advanced search for development solutions and technical content

### Markitdown Server Tools  
**Server**: markitdown-mcp  
**Transport**: stdio via npx  
**Environment**: Requires WORKDIR configuration

- **markitdown.convert**: Convert documents between various formats (PDF, DOCX, etc.)

## Tool Usage Patterns

### Cross-Server Workflows

**Visual Development Debugging**:
1. `playwright.screenshot` → Capture current state
2. `sequential-thinking.think` → Analyze visual context  
3. `context7.get-library-docs` → Find relevant patterns
4. `everything.write_file` → Implement fixes
5. `git.git_commit` → Save changes

**Automated Feature Development**:
1. `task-master.create_task` → Plan development workflow
2. `exa.search` → Research implementations
3. `context7.resolve-library-id` → Validate patterns
4. `everything.run_command` → Build and test
5. `docker.build_image` → Containerize
6. `mcping.send_notification` → Notify completion

**Documentation Processing**:
1. `markitdown.convert` → Process specifications
2. `sequential-thinking.think` → Structure approach
3. `task-master.create_task` → Create milestones
4. `everything.write_file` → Implement features
5. `git.git_add` + `git.git_commit` → Track progress

## Environment Requirements

### Required Environment Variables
```bash
# For Exa server
EXA_API_KEY="<your-exa-api-key>"

# For Markitdown server  
WORKDIR="<your-working-directory>"
```

### System Dependencies
- **Node.js**: Required for npm-based servers (everything, task-master, mcping, sequential-thinking, playwright)
- **Python/UV**: Required for uvx-based servers (git, docker)  
- **Docker**: Required for container operations
- **Modern Browser**: Required for Playwright automation

## Tool Verification Status

⚠️ **Important**: Tool names in this reference are based on common MCP server patterns. 

**Verification Required**: The following servers need tool name confirmation against actual implementations:
- task-master (third-party server)
- mcping (@toolprint package)  
- docker (uvx mcp-server-docker)
- git (uvx mcp-server-git)
- everything (@modelcontextprotocol official)
- playwright (@playwright/mcp official)
- sequential-thinking (@modelcontextprotocol official)
- markitdown (markitdown-mcp)
- exa (remote server via mcp-remote)
- context7 (SSE server)

**Recommended**: Test each server individually to confirm exact tool names and parameters before production use.

## Usage Guidelines

### Best Practices
1. **Progressive Enhancement**: Start with basic tools, add complexity incrementally
2. **Error Handling**: Always handle tool failures gracefully with fallbacks
3. **Security**: Never hardcode credentials, use environment variables
4. **Performance**: Cache results where appropriate, especially for research tools
5. **Coordination**: Leverage cross-server workflows for complex operations

### Common Integration Patterns
- **Visual + Intelligence**: Screenshots → Analysis → Implementation
- **Planning + Execution**: Task creation → Development → Tracking  
- **Research + Implementation**: Discovery → Validation → Coding
- **Monitoring + Response**: Alerts → Workflow triggers → Automated response

This persona provides 27 tools across 10 MCP servers, enabling comprehensive development assistance with visual context, intelligent orchestration, and extensive automation capabilities.