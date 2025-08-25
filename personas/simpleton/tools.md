# Tools Reference for Simpleton Persona

## Git Tools (mcp-server-git)

### git.git_status
Check the current status of the git repository.
- **Returns**: Modified files, staged files, untracked files
- **Usage**: Check what changes are pending

### git.git_add
Stage files for commit.
- **Parameters**: File paths to stage
- **Usage**: Prepare files for committing

### git.git_commit
Create a commit with staged changes.
- **Parameters**: Commit message
- **Usage**: Save changes to repository history

### git.git_diff
View differences between files.
- **Parameters**: Optional file paths
- **Returns**: Diff output showing changes
- **Usage**: Review changes before committing

### git.git_log
View commit history.
- **Parameters**: Optional number of commits
- **Returns**: Commit list with messages and metadata
- **Usage**: Review project history

### git.git_branch
Manage git branches.
- **Parameters**: Branch operations
- **Returns**: Branch information
- **Usage**: View or switch branches

## Filesystem Tools (@modelcontextprotocol/server-filesystem)

### filesystem.read
Read contents of a file.
- **Parameters**: File path
- **Returns**: File contents as text
- **Usage**: View file contents

### filesystem.write
Write content to a file.
- **Parameters**: File path, content
- **Returns**: Success/failure status
- **Usage**: Create or overwrite files

### filesystem.list
List contents of a directory.
- **Parameters**: Directory path
- **Returns**: List of files and subdirectories
- **Usage**: Explore project structure

### filesystem.create_directory
Create a new directory.
- **Parameters**: Directory path
- **Returns**: Success/failure status
- **Usage**: Set up project structure

## Fetch Tools (@modelcontextprotocol/server-fetch)

### fetch.fetch
Make a generic HTTP request.
- **Parameters**: URL, method, headers, body
- **Returns**: Response data
- **Usage**: Flexible HTTP operations

### fetch.get
Make an HTTP GET request.
- **Parameters**: URL, optional headers
- **Returns**: Response data
- **Usage**: Retrieve data from APIs

### fetch.post
Make an HTTP POST request.
- **Parameters**: URL, body, optional headers
- **Returns**: Response data
- **Usage**: Submit data to APIs

## Memory Tools (@modelcontextprotocol/server-memory)

### memory.store
Store a value in memory.
- **Parameters**: Key, value
- **Returns**: Success status
- **Usage**: Cache data for later use

### memory.retrieve
Retrieve a stored value.
- **Parameters**: Key
- **Returns**: Stored value
- **Usage**: Access cached data

### memory.list
List all stored keys.
- **Returns**: Array of keys
- **Usage**: View what's in memory

### memory.delete
Delete a stored value.
- **Parameters**: Key
- **Returns**: Success status
- **Usage**: Clean up memory storage

## Tool Combinations

### File + Git Workflow
1. `filesystem.read` - Review file
2. `filesystem.write` - Make changes
3. `git.git_status` - Check changes
4. `git.git_add` - Stage changes
5. `git.git_commit` - Commit changes

### API + Cache Workflow
1. `fetch.get` - Retrieve data
2. `memory.store` - Cache response
3. `memory.retrieve` - Use cached data
4. `filesystem.write` - Persist important data

### Project Setup Workflow
1. `filesystem.create_directory` - Create structure
2. `filesystem.write` - Create initial files
3. `git.git_add` - Stage everything
4. `git.git_commit` - Initial commit

### Exploration Workflow
1. `filesystem.list` - Browse directories
2. `filesystem.read` - Read interesting files
3. `git.git_log` - Understand history
4. `git.git_status` - Check current state