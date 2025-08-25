# /validate-persona

Validate a persona package using the persona-engineer agent.

## Purpose

This command delegates to the persona-engineer agent to validate that a persona package meets all schema requirements and acceptance criteria.

## Usage

```bash
/validate-persona [persona-name]
```

## Process

1. **Parse Arguments**
   - Extract the persona name from the command
   - If no persona name provided, prompt the user

2. **Delegate to Persona Engineer**
   - Hand off to the persona-engineer agent (`.claude/agents/persona-engineer.md`)
   - Pass the persona name for validation

3. **Validation Steps** (performed by persona-engineer)
   - Check file existence (`personas/[persona-name]/persona.yaml` and `mcp.json`)
   - Validate against schemas in `/schema/`
   - Cross-validate tool IDs with MCP servers
   - Perform security checks

## Command Flow

```
User Input: /validate-persona simpleton
    ↓
Parse persona name: "simpleton"
    ↓
Check if persona exists: personas/simpleton/
    ↓
Delegate to persona-engineer agent
    ↓
Agent performs validation:
  - Schema compliance check
  - MCP server validation
  - Tool ID verification
  - Security validation
    ↓
Return validation results to user
```

## Expected Output

### Success Case
```
Validating persona: simpleton
Delegating to persona-engineer agent...

✅ Validation Results for 'simpleton'
──────────────────────────────────────
✅ File Structure
  - persona.yaml: Found
  - mcp.json: Found

✅ Schema Compliance
  - persona.yaml: Valid against /schema/persona.schema.yaml
  - mcp.json: Valid against /schema/mcp.schema.json

✅ Cross-File Validation
  - filesystem.read → Server 'filesystem' ✓
  - filesystem.write → Server 'filesystem' ✓
  - git.status → Server 'git' ✓
  - git.commit → Server 'git' ✓

✅ Security Check
  - No hardcoded secrets
  - Environment variables properly templated
  - No local paths detected

Summary: All validation checks passed!
```

### Failure Case
```
Validating persona: invalid-example
Delegating to persona-engineer agent...

❌ Validation Results for 'invalid-example'
──────────────────────────────────────────
✅ File Structure
  - persona.yaml: Found
  - mcp.json: Found

❌ Schema Compliance
  - persona.yaml: FAILED
    • name does not match pattern ^[a-z0-9]+(-[a-z0-9]+)*$
    • description length is 8 (minimum: 10)

❌ Cross-File Validation
  - database.query → Server 'database' NOT FOUND in mcp.json

⚠️ Warnings
  - No defaultToolset specified (2 toolsets exist)
  - Missing metadata.author

Summary: 3 errors, 2 warnings
Please fix errors before using this persona.
```

## Implementation Instructions

When this command is invoked:

1. **Validate Input**
   ```typescript
   if (!personaName) {
     prompt("Enter persona name to validate:");
   }
   ```

2. **Check Persona Exists**
   ```typescript
   const personaPath = `personas/${personaName}/`;
   if (!exists(personaPath)) {
     error(`Persona '${personaName}' not found`);
   }
   ```

3. **Delegate to Agent**
   ```typescript
   // Load persona-engineer agent
   const verifier = loadAgent('.claude/agents/persona-engineer.md');
   
   // Execute validation
   const results = verifier.validate(personaName);
   ```

4. **Format and Display Results**
   - Use ✅ for passed checks
   - Use ❌ for failed checks
   - Use ⚠️ for warnings
   - Provide clear, actionable error messages

## Validation Criteria

The persona-engineer agent will check:

### Required Validations
- **File Existence**: Both persona.yaml and mcp.json must exist
- **Schema Compliance**: Files must validate against `/schema/` definitions
- **Tool Mapping**: All tool IDs must have corresponding servers
- **Security**: No hardcoded secrets or local paths

### Schema Rules
- **persona.yaml**: Must follow `/schema/persona.schema.yaml`
- **mcp.json**: Must follow `/schema/mcp.schema.json`

### Acceptance Criteria
- Name matches directory and follows pattern
- Description is 10-500 characters
- At least one toolset with valid tool IDs
- Tool IDs follow `server.tool` format
- Servers have valid transport types

## Error Handling

### File Not Found
```
Error: Persona 'unknown' not found
Please ensure the persona exists at: personas/unknown/
```

### Invalid YAML/JSON
```
Error: Failed to parse persona.yaml
SyntaxError: Unexpected token at line 5
```

### Schema Validation Failed
```
Error: Schema validation failed for persona.yaml
- Field 'name' does not match required pattern
- Field 'toolsets' is required but missing
```

## Quick Actions

After validation, suggest next steps:

### On Success
```
✅ Persona is valid and ready to use!

To use this persona:
  hypertool --persona simpleton
```

### On Failure
```
❌ Validation failed with errors

To fix:
1. Review the errors above
2. Edit the files to fix issues
3. Run validation again: /validate-persona simpleton
```

## Related Commands

- `/new-persona` - Create a new persona with proper structure
- `/list-personas` - List all available personas
- `/fix-persona [name]` - Attempt to auto-fix common issues