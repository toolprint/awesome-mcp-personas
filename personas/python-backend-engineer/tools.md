# Python Backend Engineer - Tool Reference

## Overview
This persona provides access to specialized tools for Python backend development, code quality assurance, database operations, and advanced problem-solving.

---

## PRIMS (Python Runtime Interpreter)

**Server**: `prims`  
**Purpose**: Secure Python code execution and testing environment

### Tools

#### `run_code`
Execute Python code in an isolated virtual environment with pip package support.

**Parameters**:
- `code` (string, required): Python code to execute
- `requirements` (array, optional): List of pip packages to install
- `mount_files` (array, optional): Files to mount in the execution environment

**Use Cases**:
- Test algorithm implementations
- Prototype new features
- Validate code snippets
- Data analysis and processing

**Example**:
```python
# Test a FastAPI endpoint
code = '''
from fastapi import FastAPI
app = FastAPI()

@app.get("/health")
def health_check():
    return {"status": "healthy"}

print("FastAPI app created successfully")
'''
requirements = ["fastapi", "uvicorn"]
```

#### `list_dir`
Explore workspace directory structure and file listings.

**Parameters**:
- `path` (string, optional): Directory path to list (defaults to workspace root)

**Use Cases**:
- Navigate project structure
- Understand codebase organization
- Locate specific files or modules
- Verify file placement after operations

#### `preview_file`
Examine file contents without executing code.

**Parameters**:
- `file_path` (string, required): Path to file to preview
- `lines` (number, optional): Number of lines to show

**Use Cases**:
- Code review and inspection
- Configuration file analysis
- Documentation review
- Error log examination

---

## MCP Code Checker

**Server**: `code-checker`  
**Purpose**: Python code quality analysis and automated testing

### Tools

#### `run_pylint_check`
Comprehensive Python code quality analysis using pylint.

**Parameters**:
- `project_path` (string, required): Path to Python project or file
- `pylint_args` (array, optional): Additional pylint arguments
- `config_file` (string, optional): Path to pylint configuration file

**Reports**:
- Code quality score (0-10)
- Convention violations (C)
- Refactoring suggestions (R)
- Warning issues (W)
- Error conditions (E)
- Fatal problems (F)

**Use Cases**:
- Pre-commit code quality checks
- Continuous integration validation
- Code review preparation
- Technical debt assessment

#### `run_pytest_check`
Execute Python tests and analyze test results.

**Parameters**:
- `project_path` (string, required): Path to project containing tests
- `test_path` (string, optional): Specific test file or directory
- `pytest_args` (array, optional): Additional pytest arguments

**Reports**:
- Test execution summary
- Failed test details
- Coverage information (if available)
- Performance metrics

**Use Cases**:
- Automated testing workflows
- Test result analysis
- Regression testing
- Quality gate validation

#### `run_all_checks`
Combined code quality and testing analysis.

**Parameters**:
- `project_path` (string, required): Path to Python project
- `include_tests` (boolean, optional): Whether to run tests (default: true)
- `pylint_args` (array, optional): Pylint configuration options
- `pytest_args` (array, optional): Pytest configuration options

**Use Cases**:
- Comprehensive project health checks
- CI/CD pipeline validation
- Release readiness assessment
- Development workflow automation

---

## PostgreSQL Server

**Server**: `postgres`  
**Purpose**: Advanced database operations and query management

### Tools

#### `execute_query`
Execute SQL queries with structured response formatting.

**Parameters**:
- `query` (string, required): SQL query to execute
- `parameters` (array, optional): Query parameters for prepared statements
- `format` (string, optional): Response format ("table", "json", "csv")

**Use Cases**:
- Database schema exploration
- Complex data analysis queries
- Database migration validation
- Performance testing queries

#### `list_tables`
Retrieve database schema and table information.

**Parameters**:
- `schema` (string, optional): Specific schema to examine
- `pattern` (string, optional): Table name pattern matching

**Use Cases**:
- Database structure analysis
- Schema documentation
- Table relationship mapping
- Database health monitoring

#### `describe_table`
Get detailed table structure and metadata.

**Parameters**:
- `table_name` (string, required): Name of table to describe
- `schema` (string, optional): Schema containing the table

**Returns**:
- Column definitions and types
- Constraints and indexes
- Foreign key relationships
- Table statistics

**Use Cases**:
- Database design validation
- ORM model generation
- Data migration planning
- Performance optimization

---

## Git Server

**Server**: `git`  
**Purpose**: Advanced Git operations and repository management

### Tools

#### `git_log`
Retrieve commit history and branch information.

**Parameters**:
- `repository_path` (string, required): Path to Git repository
- `branch` (string, optional): Specific branch to examine
- `limit` (number, optional): Number of commits to retrieve
- `format` (string, optional): Output format for commit information

**Use Cases**:
- Code history analysis
- Release planning
- Bug tracking and blame analysis
- Team contribution assessment

#### `git_diff`
Compare changes between commits, branches, or files.

**Parameters**:
- `repository_path` (string, required): Path to Git repository
- `source` (string, optional): Source commit/branch
- `target` (string, optional): Target commit/branch
- `file_path` (string, optional): Specific file to diff

**Use Cases**:
- Code review preparation
- Change impact analysis
- Merge conflict resolution
- Feature comparison

#### `git_status`
Get current repository state and working directory changes.

**Parameters**:
- `repository_path` (string, required): Path to Git repository

**Returns**:
- Modified files
- Staged changes
- Untracked files
- Branch status

**Use Cases**:
- Development workflow management
- Pre-commit validation
- Repository health checks
- CI/CD pipeline integration

---

## Sequential Thinking Server

**Server**: `sequential-thinking`  
**Purpose**: Complex problem decomposition and systematic analysis

### Tools

#### `create_reasoning_session`
Start a structured problem-solving session.

**Parameters**:
- `problem_description` (string, required): Description of the problem to solve
- `context` (object, optional): Additional context and constraints
- `goals` (array, optional): Specific objectives to achieve

**Use Cases**:
- Architectural decision making
- Complex debugging workflows
- System design challenges
- Performance optimization planning

#### `analyze_step_by_step`
Break down complex problems into manageable steps.

**Parameters**:
- `session_id` (string, required): ID of reasoning session
- `current_step` (string, required): Current step being analyzed
- `evidence` (array, optional): Supporting evidence or data

**Use Cases**:
- Root cause analysis
- Multi-step algorithm design
- System integration planning
- Quality improvement workflows

#### `synthesize_solution`
Combine analysis results into actionable solutions.

**Parameters**:
- `session_id` (string, required): ID of reasoning session
- `priority` (string, optional): Solution priority level
- `constraints` (array, optional): Implementation constraints

**Use Cases**:
- Solution recommendation
- Implementation planning
- Risk assessment
- Decision validation

---

## Best Practices

### Code Quality Workflow
1. **Analysis**: Use `run_pylint_check` for initial code quality assessment
2. **Testing**: Run `run_pytest_check` to validate functionality
3. **Review**: Use `preview_file` and `git_diff` for code examination
4. **Execution**: Test implementations with `run_code` in isolated environments

### Database Development
1. **Schema First**: Use `list_tables` and `describe_table` for understanding
2. **Query Development**: Test queries with `execute_query` before implementation
3. **Performance**: Monitor query execution and optimize based on results
4. **Migration**: Validate schema changes against existing data

### Problem-Solving Approach
1. **Decomposition**: Use Sequential Thinking for complex architectural decisions
2. **Evidence**: Gather data through database queries and code analysis
3. **Testing**: Validate solutions using PRIMS execution environment
4. **Version Control**: Track changes and decisions through Git operations

---

## Integration Patterns

### Development Workflow
```
Code Analysis → Testing → Database Integration → Version Control → Deployment
     ↓              ↓              ↓                 ↓              ↓
  pylint check → pytest run → query validation → git commit → final tests
```

### Quality Assurance Pipeline
```
Sequential Analysis → Code Quality → Test Execution → Database Validation
        ↓                 ↓              ↓                 ↓
   problem breakdown → pylint → pytest → database queries
```

### Debugging Workflow
```
Problem Analysis → Code Execution → Database Query → Git History → Solution
       ↓               ↓               ↓              ↓            ↓
   sequential → run_code testing → data analysis → blame/log → implementation
```