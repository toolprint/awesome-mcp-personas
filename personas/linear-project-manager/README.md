# Linear Project Manager Pro Persona

## Overview
The Linear Project Manager Pro persona provides a comprehensive project management suite that integrates Linear with Slack, GitHub, time tracking, and documentation management. It enables end-to-end project coordination, from issue tracking to team communication and code deployment.

## Purpose
This enhanced persona is designed for project managers, engineering leads, and team coordinators who need to:
- Manage issues, projects, and teams within Linear
- Coordinate team communication through Slack
- Track code changes and deployments via GitHub
- Monitor time spent and team velocity
- Maintain comprehensive project documentation
- Create a unified project management workflow

## Target Audience
- Project Managers
- Engineering Managers
- Scrum Masters
- Team Leads
- Product Owners
- DevOps Coordinators
- Technical Program Managers

## Prerequisites
- Linear account with API access
- Slack workspace with bot permissions
- GitHub account with repository access
- Time tracking system API access (optional)
- Local filesystem access for documentation

## Installation

1. Set up your environment variables:
   ```bash
   # Linear Configuration
   export LINEAR_API_TOKEN="your_linear_api_token_here"
   
   # Slack Configuration
   export SLACK_BOT_TOKEN="your_slack_bot_token_here"
   export SLACK_TEAM_ID="your_slack_team_id_here"
   
   # GitHub Configuration
   export GITHUB_PERSONAL_ACCESS_TOKEN="your_github_pat_here"
   
   # Time Tracking Configuration (optional)
   export TIME_TRACKING_API_KEY="your_time_tracking_key_here"
   
   # Documentation Root (optional, defaults to ./project-docs)
   export PROJECT_ROOT="./project-docs"
   ```

2. Install the persona configuration in your Claude Desktop MCP settings

## Included MCP Servers

### 1. linear
The Linear MCP server provides comprehensive access to Linear's project management features:
- **Source**: @modelcontextprotocol/server-linear (official MCP server)
- **Transport**: stdio
- **Authentication**: Requires LINEAR_API_TOKEN environment variable

### 2. slack
The Slack MCP server enables team communication and notifications:
- **Source**: @modelcontextprotocol/server-slack
- **Transport**: stdio
- **Authentication**: Requires SLACK_BOT_TOKEN and SLACK_TEAM_ID

### 3. github
The GitHub MCP server provides repository and code management:
- **Source**: @modelcontextprotocol/server-github
- **Transport**: stdio
- **Authentication**: Requires GITHUB_PERSONAL_ACCESS_TOKEN

### 4. time_tracker
Time tracking server for monitoring work hours and velocity:
- **Source**: @modelcontextprotocol/server-time-tracking
- **Transport**: stdio
- **Authentication**: Requires TIME_TRACKING_API_KEY

### 5. filesystem
Local filesystem access for documentation management:
- **Source**: @modelcontextprotocol/server-filesystem
- **Transport**: stdio
- **Configuration**: Restricted to project documentation paths

## Available Toolsets

### 1. intake-triage-assignment
Tools for creating and classifying issues, assigning to team members, and linking to projects.

**Tools:**
- `linear.create_issue` - Create new issues with details
- `linear.add_comment` - Add comments to existing issues
- `linear.list_members` - List team members for assignment
- `linear.list_projects` - View available projects
- `linear.list_teams` - List teams for assignment

**Common Workflows:**
- Create a new bug report and assign to developer
- Add priority and labels to incoming issues
- Link issues to appropriate projects and milestones

### 2. progress-queries-and-reports
Tools for querying issues, fetching details, and generating project status reports.

**Tools:**
- `linear.list_issues` - Query issues with filters
- `linear.get_issue` - Get detailed issue information
- `linear.list_projects` - View project scope
- `linear.get_project` - Get project details

**Common Workflows:**
- Generate weekly status reports
- Track issues by status or assignee
- Review project health and progress

### 3. roadmap-and-team-operations
Tools for managing teams, projects, and coordinating upcoming work.

**Tools:**
- `linear.list_teams` - View team structure
- `linear.list_projects` - Explore project landscape
- `linear.list_issues` - Review team backlogs
- `linear.add_comment` - Communicate with stakeholders

**Common Workflows:**
- Review team capacity and workload
- Plan sprint content and priorities
- Coordinate cross-team dependencies

### 4. slack-communication
Tools for team communication, notifications, and coordination through Slack.

**Tools:**
- `slack.send_message` - Post messages to channels or DMs
- `slack.list_channels` - View available channels
- `slack.list_users` - Find team members
- `slack.get_channel_history` - Review past conversations
- `slack.create_channel` - Create new project channels
- `slack.add_reaction` - React to messages

**Common Workflows:**
- Post daily standup summaries
- Send sprint completion notifications
- Alert team about critical issues
- Coordinate emergency responses

### 5. github-integration
Tools for linking code changes with project management.

**Tools:**
- `github.create_issue` - Create GitHub issues from Linear
- `github.list_pull_requests` - Track PR status
- `github.get_pull_request` - Get PR details
- `github.create_pull_request_comment` - Add PR feedback
- `github.list_repositories` - View available repos
- `github.get_repository` - Get repo information

**Common Workflows:**
- Link Linear issues to GitHub PRs
- Track deployment status
- Monitor code review progress
- Identify technical blockers

### 6. time-tracking-analysis
Tools for tracking time, analyzing velocity, and measuring productivity.

**Tools:**
- `time_tracker.start_timer` - Begin time tracking
- `time_tracker.stop_timer` - End time tracking
- `time_tracker.log_entry` - Manual time entry
- `time_tracker.get_report` - Generate time reports
- `time_tracker.list_entries` - View time logs

**Common Workflows:**
- Track time per Linear issue
- Generate sprint velocity reports
- Identify process bottlenecks
- Measure team productivity

### 7. document-management
Tools for creating and managing project documentation.

**Tools:**
- `filesystem.read` - Read existing documentation
- `filesystem.write` - Create new documents
- `filesystem.edit` - Update documentation
- `filesystem.list` - Browse document structure
- `filesystem.create_directory` - Organize documentation

**Common Workflows:**
- Write sprint retrospectives
- Maintain project wiki
- Create onboarding guides
- Document architectural decisions

## Common Use Cases

### 1. **Sprint Management**
- Create sprint in Linear
- Assign issues to team members
- Post sprint kickoff in Slack
- Link GitHub PRs to Linear issues
- Track time spent on tasks
- Generate sprint reports

### 2. **Daily Standups**
- Query yesterday's completed issues
- Identify today's priorities
- Check PR review status
- Post summary to Slack channel
- Update team on blockers

### 3. **Release Coordination**
- Track release-tagged issues in Linear
- Monitor GitHub deployment PRs
- Communicate release status in Slack
- Document release notes
- Track release preparation time

### 4. **Cross-Team Collaboration**
- Create shared Linear projects
- Set up dedicated Slack channels
- Link related GitHub repositories
- Share documentation across teams
- Track cross-team dependencies

### 5. **Performance Analytics**
- Analyze issue completion rates
- Calculate team velocity
- Identify bottlenecks in workflow
- Generate time tracking reports
- Share insights with stakeholders

## Configuration

Required environment variables:
- `LINEAR_API_TOKEN`: Your Linear API token (required)
- `SLACK_BOT_TOKEN`: Slack bot OAuth token (required for Slack features)
- `SLACK_TEAM_ID`: Your Slack workspace ID (required for Slack features)
- `GITHUB_PERSONAL_ACCESS_TOKEN`: GitHub PAT with repo access (required for GitHub features)
- `TIME_TRACKING_API_KEY`: Time tracking service API key (optional)
- `PROJECT_ROOT`: Root directory for documentation (optional, defaults to ./project-docs)

## Best Practices

1. **Integrated Workflow**
   - Link Linear issues to GitHub PRs using issue IDs
   - Post Linear issue updates to relevant Slack channels
   - Document decisions in project wiki

2. **Communication Strategy**
   - Use Slack for immediate notifications
   - Keep Linear comments for permanent record
   - Document architectural decisions in filesystem

3. **Time Management**
   - Track time against specific Linear issues
   - Review velocity trends weekly
   - Adjust sprint capacity based on data

4. **Documentation**
   - Maintain README files for each project
   - Document sprint retrospectives
   - Create runbooks for common procedures

## Troubleshooting

### Authentication Issues
- Verify all tokens are correctly set in environment
- Check token permissions match required scopes
- Ensure tokens haven't expired

### Integration Issues
- Verify Slack bot is added to channels
- Check GitHub PAT has repo access
- Ensure Linear workspace allows API access

### Performance Issues
- Limit concurrent API calls
- Use filtering to reduce data volumes
- Cache frequently accessed data locally

## Support
For issues with:
- This persona configuration: Open an issue in the awesome-mcp-personas repository
- Individual MCP servers: Check respective @modelcontextprotocol/server-* documentation
- API services: Refer to Linear, Slack, GitHub, etc. documentation