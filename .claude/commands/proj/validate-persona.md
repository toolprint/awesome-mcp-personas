# /validate-persona

Validate and auto-fix a persona package using the persona-engineer agent.

## Usage

```bash
/validate-persona [persona-name]
```

## Purpose

Delegates to the persona-engineer agent to validate, auto-fix, and report on persona package compliance.

## Process

When invoked with a persona name (e.g., `/validate-persona simpleton`):

1. **Check if persona exists** at `personas/[persona-name]/`
2. **Delegate to persona-engineer agent** for comprehensive validation and auto-fixing
3. **Agent will automatically**:
   - Validate against schemas
   - Research and verify MCP servers
   - Fix any issues found
   - Generate validation_notes.md
   - Report final status

## Arguments

- `[persona-name]` - Name of the persona to validate (required)

## Implementation

```typescript
// Pseudocode for command execution
function validatePersona(personaName: string) {
  // 1. Verify persona exists
  if (!exists(`personas/${personaName}/`)) {
    return error(`Persona '${personaName}' not found`);
  }

  // 2. Delegate to persona-engineer
  const agent = loadAgent('.claude/agents/persona-engineer.md');
  
  // 3. Execute validation with auto-fix
  const result = agent.validateAndFix(personaName);
  
  // 4. Return result
  return result;
}
```

## Notes

- The persona-engineer agent will auto-fix issues without requiring user intervention
- All fixes are documented in `personas/[persona-name]/validation_notes.md`
- The agent researches actual tool names from MCP server documentation
- No manual approval needed - fixes are applied automatically