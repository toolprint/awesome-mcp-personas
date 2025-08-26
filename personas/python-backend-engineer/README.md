# Python Backend Engineer Persona

## Overview
A specialized Python backend engineering expert focused on Pythonic development practices, code quality analysis, and systematic problem-solving. This persona embodies deep Python ecosystem knowledge and provides sophisticated tooling for building, analyzing, and managing Python backend systems with emphasis on file operations, version control, and knowledge management.

## Target Audience
- Senior Python backend engineers
- Python architects and technical leads
- Developers building scalable Python web services
- Teams focused on Python best practices and code quality
- Engineers working on complex Python codebases requiring analysis and refactoring

## Core Capabilities
This persona specializes in:

### **Pythonic Development Excellence**
- Deep understanding of Python idioms, patterns, and best practices
- Advanced knowledge of Python type systems, async/await, and performance optimization
- Expertise in Python project structure, packaging, and distribution

### **Code Quality & Analysis** 
- Analyze Python code for quality, style, and best practices compliance
- Run comprehensive linting and testing tools (pylint, pytest)
- Manage Python files and project structures efficiently  
- Identify code issues and provide systematic improvement recommendations

### **Python DevX Mastery**
- Advanced usage of Python development tools (linting, formatting, type checking)
- Virtual environment management and dependency resolution
- Python testing frameworks and quality assurance tools
- Performance profiling and optimization tools

### **Backend System Design**
- Python web framework expertise (FastAPI, Django, Flask)
- File system operations and project structure management
- Web content research and integration capabilities
- Knowledge graph management for project insights and patterns

## Expected Toolsets

### **Code Analysis & Quality**
Tools for analyzing Python code structure, running quality checks, and systematic problem-solving for backend development.

### **Python DevX Tools**
Advanced Python development experience tools including version control, testing, and knowledge management for project insights.

### **Backend Development**
Python backend development tools including file operations, web research capabilities, and system integration.

### **Quality & Testing**
Comprehensive testing, code quality, and performance analysis tools specifically optimized for Python projects.

## Prerequisites
- Python 3.8+ installed
- Understanding of Python virtual environments
- Familiarity with Python project structure and packaging
- Basic knowledge of Python web frameworks
- Git version control system

## Installation

Configure the following MCP servers in your Claude Desktop configuration:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem"],
      "env": {
        "FILESYSTEM_ALLOWED_DIRECTORIES": "<your-project-directories>"
      }
    },
    "code-checker": {
      "command": "uvx",
      "args": ["mcp-code-checker"],
      "env": {}
    },
    "sequential-thinking": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sequentialthinking"],
      "env": {}
    },
    "git": {
      "command": "uvx",
      "args": ["mcp-server-git"],
      "env": {}
    },
    "memory": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-memory"],
      "env": {}
    },
    "fetch": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fetch"],
      "env": {}
    }
  }
}
```

### Server Setup Instructions

1. **Code Checker** (Python package):
   ```bash
   pip install mcp-code-checker
   ```

2. **Official MCP Servers** (filesystem, sequential-thinking, memory, fetch):
   ```bash
   # These install automatically when run via npx
   # No manual installation required
   ```

3. **Git Server**:
   ```bash
   # Install via uvx (automatically downloads when first run)
   # No manual installation required
   ```

4. **Environment Variables**:
   - Set `FILESYSTEM_ALLOWED_DIRECTORIES` to your project directories (comma-separated)

## MCP Servers

### Core Python Development

#### **MCP Code Checker**
- **Purpose**: Python code quality analysis and testing automation
- **Repository**: [MarcusJellinghaus/mcp-code-checker](https://github.com/MarcusJellinghaus/mcp-code-checker)
- **Installation**: `uvx mcp-code-checker` (automatically installs when run)
- **Key Tools**:
  - `run_pylint_check` - Comprehensive code quality analysis
  - `run_pytest_check` - Automated test execution and reporting  
  - `run_all_checks` - Combined quality and testing validation
- **Best For**: Code review, quality assurance, continuous integration

#### **Filesystem Server**
- **Purpose**: Secure file operations with configurable access controls
- **Repository**: [Official MCP Servers](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem)
- **Installation**: `npx -y @modelcontextprotocol/server-filesystem`
- **Key Tools**:
  - `read_text_file` - Read Python source files and configurations
  - `write_file` - Create or modify Python files and project configurations
  - `list_directory` - Explore project structure and module organization
  - `create_directory` - Set up new Python packages and project directories
- **Best For**: Project structure management, file operations, Python package organization

### Knowledge & Research

#### **Memory Server**
- **Purpose**: Knowledge graph-based persistent memory system for project insights
- **Repository**: [Official MCP Servers](https://github.com/modelcontextprotocol/servers/tree/main/src/memory)
- **Installation**: `npx -y @modelcontextprotocol/server-memory`  
- **Key Tools**:
  - `create_entities` - Store Python concepts, patterns, and architectural insights
  - `add_observations` - Record development insights and code patterns
  - `search_nodes` - Find related Python concepts and project knowledge
  - `read_graph` - Analyze knowledge relationships and project architecture
- **Best For**: Project knowledge management, architectural insights, pattern recognition

#### **Fetch Server**
- **Purpose**: Web content fetching for research and documentation
- **Repository**: [Official MCP Servers](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch)
- **Installation**: `npx -y @modelcontextprotocol/server-fetch`
- **Key Tools**:
  - `fetch` - Fetch Python documentation, Stack Overflow solutions, and technical resources
- **Best For**: Python research, documentation gathering, library exploration

### Version Control & Project Management

#### **Git Server**
- **Purpose**: Advanced Git operations and repository management
- **Repository**: [Official MCP Servers](https://github.com/modelcontextprotocol/servers/tree/main/src/git)
- **Installation**: `uvx mcp-server-git`
- **Key Tools**:
  - `git_status` - Check repository status and changes
  - `git_diff` - View code changes and differences
  - `git_log` - Analyze commit history and changes
  - `git_add` - Stage files for commit
  - `git_commit` - Create commits with proper messages
- **Best For**: Version control workflows, code review, project history analysis

### Advanced Problem Solving

#### **Sequential Thinking**
- **Purpose**: Complex problem decomposition and systematic analysis
- **Repository**: [Official MCP Servers](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking)
- **Installation**: `npx -y @modelcontextprotocol/server-sequentialthinking`
- **Key Tools**:
  - `create_reasoning_session` - Start structured analysis sessions
  - `analyze_step_by_step` - Break down complex Python problems systematically
  - `synthesize_solution` - Combine analysis into comprehensive solutions
- **Best For**: Complex system design, debugging, architectural decisions, Python optimization

## Common Use Cases

### **Python Code Quality Analysis**
- Run comprehensive code quality checks using pylint and pytest
- Identify code smells, style violations, and potential issues
- Analyze test coverage and suggest improvements
- Perform systematic code reviews with quality metrics

### **Project Structure Management**
- Navigate and analyze Python project structures and packages
- Create well-organized Python packages and module hierarchies
- Read and modify Python files with proper structure
- Set up project directories following Python best practices

### **Knowledge-Driven Development**
- Store and retrieve project insights, patterns, and architectural decisions
- Build knowledge graphs of Python concepts and project relationships
- Research Python documentation and best practices from web sources
- Track development insights and code patterns for future reference

### **Systematic Problem Solving**
- Break down complex Python backend challenges into manageable steps
- Apply structured reasoning to architectural decisions
- Combine multiple analysis approaches for comprehensive solutions
- Document reasoning processes for future reference and team sharing

## Best Practices
- Focus on Pythonic code patterns and idioms
- Emphasize type safety and static analysis
- Prioritize code readability and maintainability
- Follow PEP standards and community conventions
- Use virtual environments for all projects

## Troubleshooting

### Common Setup Issues

#### **Code Checker Installation**
- **Issue**: "mcp-code-checker not found"
- **Solution**: Ensure Python package is installed: `pip install mcp-code-checker`
- **Check**: Verify your Python environment has the package installed

#### **Filesystem Access**
- **Issue**: "Permission denied" when accessing files
- **Solution**: Set `FILESYSTEM_ALLOWED_DIRECTORIES` to your project paths
- **Format**: Comma-separated absolute paths to your Python projects

#### **Server Connection Issues**
- **Issue**: MCP servers fail to start
- **Solution**: Ensure npm and Python are properly installed
- **Check**: Run `npx --version` and `python --version` to verify installations

#### **Memory/Knowledge Storage**
- **Issue**: Knowledge graph data not persisting
- **Solution**: The memory server stores data locally in its working directory
- **Note**: Data persists between sessions automatically

### Performance Optimization

#### **File Operations**
- Use filesystem tools efficiently - batch multiple file reads when possible
- Configure `FILESYSTEM_ALLOWED_DIRECTORIES` to limit scope and improve performance
- Leverage file listing to understand project structure before detailed analysis

#### **Knowledge Management**
- Use memory server's graph structure to store related concepts together
- Search knowledge nodes before creating new entities to avoid duplicates
- Structure observations with clear relationships for efficient retrieval

### Python Environment Best Practices

#### **Virtual Environment Management**
- Always use isolated environments for different projects
- Keep requirements.txt updated for reproducible environments
- Use specific Python versions for consistency across development and production

#### **Code Quality Workflow**
1. Use `run_pylint_check` for initial code analysis and style checking
2. Address critical issues and style violations identified
3. Use `run_pytest_check` for comprehensive testing and coverage analysis
4. Use `run_all_checks` for combined quality validation before commits
5. Store insights in memory server for future reference and pattern recognition

## Support
For issues with this persona configuration, refer to the awesome-mcp-personas repository documentation.

## Contributing
Improvements to Python development workflows and tool suggestions are welcome through pull requests.

## License
This persona configuration follows the same licensing terms as the Awesome MCP Personas project.