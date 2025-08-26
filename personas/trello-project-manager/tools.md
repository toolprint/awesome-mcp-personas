# Trello Project Manager Tools Reference

> **⚠️ Tool Name Validation Status**: The tool names listed below are based on the persona configuration and may require verification against the actual `@modelcontextprotocol/server-trello` implementation.

## Available Tools

All tools are prefixed with `trello.` as they belong to the Trello MCP server.

### Backlog Management Tools

#### `trello.get_cards_by_list`
Retrieve all cards from a specific list on the board.

**Purpose**: View cards in specific lists (backlog, to-do, in-progress, etc.)
**Use Cases**:
- Review backlog items before sprint planning
- Check progress of current sprint items
- Audit completed work in "Done" list

#### `trello.add_card`
Create a new card on the board.

**Purpose**: Add new tasks, features, or bug reports
**Use Cases**:
- Create user stories during backlog grooming
- Add urgent bug reports to appropriate list
- Document new feature requests from stakeholders

#### `trello.update_card`
Modify existing card details (title, description, labels, etc.).

**Purpose**: Keep cards current with latest information
**Use Cases**:
- Update card descriptions with acceptance criteria
- Modify card titles for clarity
- Add or update card labels for categorization

#### `trello.move_card`
Move cards between different lists on the board.

**Purpose**: Progress cards through workflow stages
**Use Cases**:
- Move cards from "To Do" to "In Progress"
- Progress completed work to "Done"
- Return blocked items to appropriate previous state

#### `trello.change_card_members`
Assign or unassign team members to/from cards.

**Purpose**: Manage task assignments and ownership
**Use Cases**:
- Assign cards to team members during sprint planning
- Reassign cards when team members are unavailable
- Remove assignments when work is completed

### Board Operations Tools

#### `trello.get_lists`
Retrieve all lists currently on the board.

**Purpose**: View board structure and available workflow stages
**Use Cases**:
- Audit board organization before sprint planning
- Identify lists that need archiving
- Plan new list creation for project phases

#### `trello.add_list`
Create a new list on the board.

**Purpose**: Expand board structure for new workflows
**Use Cases**:
- Create sprint-specific lists (e.g., "Sprint 15")
- Add specialized lists for different project phases
- Create temporary lists for special project needs

#### `trello.archive_list`
Archive a list (remove from active board view but preserve data).

**Purpose**: Clean up board by removing obsolete lists
**Use Cases**:
- Archive completed sprint lists
- Remove temporary project lists after completion
- Clean up experimental workflow lists

### Activity and Reporting Tools

#### `trello.get_recent_activity`
Fetch recent activity and changes on the board.

**Purpose**: Track what has changed recently for reporting
**Use Cases**:
- Generate daily standup summaries
- Create weekly progress reports
- Monitor team activity and productivity

#### `trello.get_my_cards`
View cards assigned to the current user.

**Purpose**: Personal task management and workload visibility
**Use Cases**:
- Review personal assignment before standups
- Track individual progress and commitments
- Identify potential workload balancing needs

## Tool Usage Patterns

### Workflow Progression Pattern
```
1. trello.get_lists → View available workflow stages
2. trello.get_cards_by_list → Review current items
3. trello.move_card → Progress items to next stage
4. trello.update_card → Add completion notes or updates
```

### Sprint Planning Pattern
```
1. trello.get_cards_by_list (backlog) → Review available work
2. trello.update_card → Add story points and acceptance criteria
3. trello.move_card → Move prioritized items to sprint list
4. trello.change_card_members → Assign work to team members
```

### Board Maintenance Pattern
```
1. trello.get_lists → Review current board structure
2. trello.add_list → Create new sprint or phase lists
3. trello.archive_list → Clean up completed lists
4. trello.get_recent_activity → Verify changes were applied
```

### Reporting Pattern
```
1. trello.get_recent_activity → Gather recent changes
2. trello.get_my_cards → Check individual assignments
3. trello.get_cards_by_list (done) → Review completed work
4. Generate reports based on collected data
```

## Integration Notes

- All tools require proper Trello API authentication (API key and token)
- Board ID must be specified in environment configuration
- Tools respect Trello's API rate limits and permissions
- Some operations may require specific board permissions for the authenticated user

## Troubleshooting Tools

If tool execution fails:
1. Verify environment variables are correctly set
2. Check API key and token permissions
3. Ensure board ID is valid and accessible
4. Confirm user has appropriate board permissions for the requested operation

## Tool Name Validation Required

**⚠️ Important**: These tool names are based on the persona configuration and may not match the actual implementation of `@modelcontextprotocol/server-trello`. Before using this persona in production:

1. Verify actual tool names against the official server documentation
2. Test each tool to confirm functionality
3. Update the persona configuration if tool names differ
4. Report any discrepancies for persona improvement