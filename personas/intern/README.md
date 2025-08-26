# Simpleton Persona

## Overview

The Simpleton persona is a comprehensive getting-started package designed for users new to MCP (Model Context Protocol) personas. It provides essential tools across multiple domains including version control, file management, web requests, and data persistence, making it ideal for basic development tasks and learning the MCP ecosystem.

## Target Audience

- Developers new to MCP personas
- Users looking for a simple, well-rounded starter configuration
- Learning and experimentation with MCP servers
- Basic automation and scripting tasks
- Prototype development and proof-of-concepts

## Prerequisites

- Node.js 16+ (for npm-based servers)
- Python 3.8+ with pip (for Git MCP server)
- Git installed on your system
- Basic understanding of command-line tools

## Installation

1. Install the Git MCP server:
   ```bash
   pip install mcp-server-git
   ```

2. The Node.js-based servers will be automatically installed when first used via npx.

3. Set up environment variables (optional):
   ```bash
   # Optional: Set project root for filesystem server
   export PROJECT_ROOT=/path/to/your/project
   ```

## MCP Servers

### 1. git
Version control operations powered by the Git MCP server:
- **Source**: mcp-server-git (Python package)
- **Transport**: stdio
- **Authentication**: None required (uses local git config)

### 2. filesystem
File and directory operations:
- **Source**: @modelcontextprotocol/server-filesystem
- **Transport**: stdio
- **Configuration**: PROJECT_ROOT environment variable (defaults to current directory)

### 3. fetch
HTTP client for web requests and API interactions:
- **Source**: @modelcontextprotocol/server-fetch
- **Transport**: stdio
- **Authentication**: None required

### 4. memory
In-memory key-value storage for session persistence:
- **Source**: @modelcontextprotocol/server-memory
- **Transport**: stdio
- **Authentication**: None required

## Toolsets

### 1. file-and-version-control (default)
Essential tools for file management and version control.

**Tools:**
- `filesystem.read` - Read file contents
- `filesystem.write` - Write to files
- `filesystem.list` - List directory contents
- `filesystem.create_directory` - Create directories
- `git.git_status` - Check repository status
- `git.git_add` - Stage files for commit
- `git.git_commit` - Commit changes
- `git.git_diff` - View differences
- `git.git_log` - View commit history

**Common Workflows:**
- Browse project structure
- Read and modify files
- Track changes with git
- Commit work incrementally

### 2. web-and-api
Tools for HTTP requests and API interactions.

**Tools:**
- `fetch.fetch` - Generic HTTP request
- `fetch.get` - HTTP GET request
- `fetch.post` - HTTP POST request
- `memory.store` - Cache API responses
- `memory.retrieve` - Retrieve cached data

**Common Workflows:**
- Fetch data from REST APIs
- Submit form data
- Cache API responses for reuse
- Test webhooks and endpoints

### 3. data-persistence
Memory and file-based data storage.

**Tools:**
- `memory.store` - Store data in memory
- `memory.retrieve` - Retrieve stored data
- `memory.list` - List all stored keys
- `memory.delete` - Delete stored data
- `filesystem.write` - Persist to files
- `filesystem.read` - Load from files

**Common Workflows:**
- Save configuration data
- Cache computation results
- Maintain session state
- Persist data between runs

### 4. project-exploration
Tools for understanding project structure and history.

**Tools:**
- `filesystem.list` - Browse directories
- `filesystem.read` - Read documentation
- `git.git_log` - View project history
- `git.git_status` - Check current state
- `git.git_branch` - View branches

**Common Workflows:**
- Explore new codebases
- Understand project layout
- Review commit history
- Check branch structure

## Common Use Cases

### 1. Quick Development Tasks
```
- Read project files
- Make simple edits
- Commit changes
- Check git status
```

### 2. API Testing
```
- Make HTTP requests
- Cache responses
- Compare results
- Debug endpoints
```

### 3. Project Setup
```
- Create directory structure
- Initialize git repository
- Set up basic files
- Configure project
```

### 4. Learning MCP
```
- Experiment with different tools
- Understand tool interactions
- Build simple automations
- Learn best practices
```

## Configuration

The persona uses sensible defaults but can be customized:

### Environment Variables
- `PROJECT_ROOT`: Root directory for filesystem operations (optional, defaults to current directory)

### Customization
To customize the persona:
1. Edit `mcp.json` to modify server configurations
2. Edit `persona.yaml` to adjust toolsets or add new tools
3. Ensure all changes comply with the MCP schema

## Troubleshooting

### Common Issues

1. **Git commands not working**
   - Ensure Git is installed: `git --version`
   - Check you're in a git repository: `git status`
   - Verify mcp-server-git is installed: `pip show mcp-server-git`

2. **Filesystem access denied**
   - Check file permissions
   - Verify PROJECT_ROOT is set correctly
   - Ensure the directory exists

3. **Fetch requests failing**
   - Check network connectivity
   - Verify the URL is correct
   - Check for CORS issues if accessing browsers

4. **Memory storage lost**
   - Memory storage is session-based
   - Use filesystem.write to persist data permanently

## Best Practices

1. **Start Simple**: Begin with the default toolset to understand basics
2. **Combine Tools**: Use multiple servers together for complex workflows
3. **Cache Wisely**: Use memory storage for temporary data, filesystem for permanent
4. **Version Control**: Always use git tools to track your changes
5. **Explore Safely**: Use filesystem.list before reading/writing files

## Contributing

To improve this persona:
1. Verify all tool names against actual MCP server implementations
2. Test each toolset with real-world scenarios
3. Document any additional tools discovered
4. Submit improvements via pull request

## License

This persona configuration is part of the Awesome MCP Personas project and follows the same licensing terms.

## Support

For issues or questions:
- Check the validation notes in `validation_notes.md`
- Review the MCP documentation for each server
- Submit issues to the Awesome MCP Personas repository