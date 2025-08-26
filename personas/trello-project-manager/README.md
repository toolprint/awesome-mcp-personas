# Trello Project Manager Assistant Persona

## Overview
Manages Trello boards for planning, backlog curation, and stakeholder updates. Streamlines project management workflows by providing tools for board operations, card management, and activity tracking.

## Target Audience
- Project managers using Trello for team coordination
- Scrum masters managing agile workflows
- Development team leads organizing sprints
- Product owners maintaining backlogs
- Team coordinators tracking project progress

## Prerequisites
- Active Trello account with API access
- Trello API key and token (generate from https://trello.com/app-key)
- Trello board ID for the board you want to manage
- Node.js (for npx command execution)

## Installation

1. Set up your environment variables:
   ```bash
   export trelloApiKey="your-trello-api-key"
   export trelloToken="your-trello-token"
   export trelloBoardId="your-board-id"
   ```

2. The MCP servers will be automatically installed when first used.

## MCP Servers

### 1. Trello
Official Atlassian Trello board management server
- **Source**: Official Atlassian/Model Context Protocol
- **Package**: `@modelcontextprotocol/server-trello`
- **Transport**: stdio
- **Authentication**: API key and token required
- **Environment**: trelloApiKey, trelloToken, trelloBoardId

## Toolsets

### 1. backlog-management
Organize and groom backlog by list; add/update cards and assign members.

**Tools:**
- `trello.get_cards_by_list` - Retrieve cards from specific list
- `trello.add_card` - Create new cards
- `trello.update_card` - Modify card details
- `trello.move_card` - Move cards between lists
- `trello.change_card_members` - Assign/unassign team members

**Common Workflows:**
- Review backlog items in "To Do" list
- Add new feature requests from stakeholder feedback
- Update card descriptions with acceptance criteria
- Move cards from "In Progress" to "Review"
- Assign team members to specific tasks

### 2. board-operations-and-hygiene
Inspect lists, add or archive lists, and keep the board tidy.

**Tools:**
- `trello.get_lists` - View all board lists
- `trello.add_list` - Create new lists (e.g., sprint lists)
- `trello.archive_list` - Archive completed/obsolete lists

**Common Workflows:**
- Set up new sprint lists for upcoming iterations
- Archive completed sprint lists to maintain board clarity
- Reorganize board structure for improved workflow
- Create specialized lists for different project phases

### 3. activity-digests
Pull recent activity for standups and stakeholder notes.

**Tools:**
- `trello.get_recent_activity` - Fetch recent board changes
- `trello.get_my_cards` - View cards assigned to current user

**Common Workflows:**
- Generate daily standup summaries
- Create weekly progress reports for stakeholders
- Track team productivity and card completion rates
- Identify blocking issues requiring attention

## Common Use Cases

### 1. Sprint Planning Preparation
- Retrieve all cards from "Backlog" list
- Review and update card descriptions with latest requirements
- Assign story points or effort estimates
- Move prioritized items to "Sprint Ready" list

### 2. Daily Standup Coordination
- Get recent activity to identify completed work
- View each team member's assigned cards
- Check for blocked items requiring discussion
- Generate summary of yesterday's progress

### 3. Stakeholder Reporting
- Fetch recent board activity for progress updates
- Compile list of completed features and bug fixes
- Track cards moved to "Done" status
- Prepare executive summary of project status

### 4. Board Maintenance
- Archive old sprint lists to reduce clutter
- Create new lists for upcoming project phases
- Update card assignments based on team changes
- Reorganize board structure for better workflow

## Configuration

### Environment Variables
- `trelloApiKey`: Your Trello API key (required) - Generate from https://trello.com/app-key
- `trelloToken`: Your Trello API token (required) - Generate from https://trello.com/app-key
- `trelloBoardId`: Target board ID (required) - Found in board URL

### Customization
To customize the persona:
1. Edit `mcp.json` to modify server configurations or environment variables
2. Edit `persona.yaml` to adjust toolsets or add new tools
3. Ensure all changes comply with the MCP schema

## Best Practices

- Keep API credentials secure and never commit to version control
- Use descriptive card titles and detailed descriptions for better team communication
- Regularly archive completed lists to maintain board performance
- Assign team members appropriately to maintain accountability
- Use consistent naming conventions for lists across projects
- Regular board cleanup prevents information overload

## Troubleshooting

### Common Issues

1. **Authentication Errors**
   - Verify API key and token are correctly set in environment variables
   - Check that the API key and token have not expired
   - Ensure the token has appropriate permissions for the target board

2. **Board Not Found**
   - Verify the board ID in the trelloBoardId environment variable
   - Ensure you have access permissions to the specified board
   - Check that the board has not been deleted or archived

3. **Tool Execution Failures**
   - Ensure Node.js is installed for npx command execution
   - Verify internet connectivity for API calls
   - Check Trello API rate limits if experiencing frequent failures

## Support

For issues with:
- This persona configuration: Open an issue in the awesome-mcp-personas repository
- Trello MCP server: Check the official Model Context Protocol servers documentation
- Trello API: Refer to Trello's official API documentation

## Contributing

To improve this persona:
1. Verify all tool names against actual MCP server implementations
2. Test each toolset with real-world Trello scenarios
3. Document any additional tools discovered in the server
4. Submit improvements via pull request

## License

This persona configuration is part of the Awesome MCP Personas project and follows the same licensing terms.