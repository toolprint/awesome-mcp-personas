# Software Development Assistant Persona

## Overview
A teammate for day-to-day engineering work: version control hygiene, lightweight reviews via diffs, and sharing updates to Slack.

## Target Audience
- Software engineers working in team environments
- Developers who use Git for version control
- Teams that communicate via Slack
- Engineers who need to manage code reviews and releases
- Developers looking to streamline their workflow automation

## Prerequisites
- Git repository setup and access
- Slack workspace with bot integration permissions
- Python environment for running MCP servers via `uvx`
- Active development workflow requiring version control and team communication

## Installation

1. Set up your environment variables:
   ```bash
   export SLACK_BOT_TOKEN="your-slack-bot-token-here"
   ```

2. The MCP servers will be automatically installed when first used.

## MCP Servers

### 1. Git
Provides comprehensive Git version control operations for repository management and code collaboration.
- **Source**: Python package
- **Package**: `mcp-server-git`  
- **Transport**: stdio
- **Authentication**: Local Git credentials

### 2. Slack
Enables Slack workspace integration for team communication and automated notifications.
- **Source**: Python package
- **Package**: `slack-mcp-server`  
- **Transport**: stdio
- **Authentication**: Bot token required
- **Environment**: Requires SLACK_BOT_TOKEN

## Toolsets

### 1. plan-build-communicate (default)
From creating a work branch to sharing progress: branch, code, diff, and broadcast updates. Examples: start a feature branch, stage/commit changes, summarize what changed, post status in #dev.

**Tools:**
- `git.git_branch` - Create, list, or switch Git branches for feature development
- `git.git_status` - Check working directory status and staged changes
- `git.git_add` - Stage files for commit in Git repository
- `git.git_commit` - Create commits with messages and staged changes
- `git.git_diff` - View differences between commits, branches, or working directory
- `slack.conversations_add_message` - Send messages to Slack channels or direct messages

**Common Workflows:**
- Create feature branch and start development work
- Stage changes, commit with descriptive messages
- Generate diff summaries and share progress updates
- Post development status updates to team channels

### 2. code-archaeology-knowledge-sharing
Explore history, pull a focused diff or file view, and share context with teammates. Examples: list recent commits, show a commit, diff two refs, post thread with key snippets.

**Tools:**
- `git.git_log` - View commit history with filtering and formatting options
- `git.git_diff` - View differences between commits, branches, or working directory
- `slack.channels_list` - List available Slack channels in the workspace
- `slack.conversations_add_message` - Send messages to Slack channels or direct messages

**Common Workflows:**
- Investigate recent changes and commit history
- Extract meaningful diffs for code review discussions
- Share code context and explanations with team members
- Post detailed technical threads with code snippets

### 3. release-prep-team-nudges
Prepare for PRs/releases with sanity checks and nudges to collaborators. Examples: verify working tree clean, generate review diff, ping reviewers in channel.

**Tools:**
- `git.git_status` - Check working directory status and staged changes
- `git.git_diff` - View differences between commits, branches, or working directory
- `slack.channels_list` - List available Slack channels in the workspace
- `slack.conversations_add_message` - Send messages to Slack channels or direct messages

**Common Workflows:**
- Verify repository state before creating pull requests
- Generate comprehensive review diffs for team evaluation
- Send automated nudges and reminders to reviewers
- Coordinate release preparation with team notifications

## Common Use Cases

### 1. Feature Development Workflow
- Create a new feature branch using Git branching tools
- Make code changes and use Git status to track progress
- Stage and commit changes with descriptive commit messages
- Generate diff summaries to review changes before pushing
- Share development progress updates in relevant Slack channels

### 2. Code Review and Collaboration
- Use Git log to investigate recent changes and commit history
- Generate focused diffs between branches or specific commits
- Share code context and technical discussions via Slack threads
- Post code snippets and explanations to facilitate team knowledge sharing

### 3. Release Preparation and Coordination
- Verify working directory is clean and ready for release
- Generate comprehensive diffs showing all changes since last release
- Send automated notifications to team channels about release status
- Ping specific team members or reviewers for final approvals
- Coordinate release activities through structured Slack communications

## Configuration

### Environment Variables
- `SLACK_BOT_TOKEN`: Slack bot token for workspace integration (required)

### Customization
To customize the persona:
1. Edit `mcp.json` to modify server configurations
2. Edit `persona.yaml` to adjust toolsets or add new tools
3. Ensure all changes comply with the MCP schema

## Best Practices

- Set up proper Git configuration with user name and email before using Git tools
- Ensure Slack bot has appropriate permissions for channels you want to post to
- Use descriptive commit messages when using the commit tools
- Test Slack integration in development channels before using in production channels
- Keep Git repository clean and organize commits logically before sharing diffs
- Use appropriate Slack channels for different types of updates (development vs. releases)
- Verify working directory status before major operations like releases or pull requests

## Troubleshooting

### Common Issues

1. **Git authentication failures**
   - Ensure Git credentials are properly configured locally
   - Check if repository access permissions are set up correctly
   - Verify SSH keys or HTTPS credentials are working

2. **Slack bot token issues**
   - Verify SLACK_BOT_TOKEN environment variable is set correctly
   - Check that bot has necessary permissions in the workspace
   - Ensure bot is added to channels where you want to post messages

3. **MCP server installation problems**
   - Ensure `uvx` is installed and available in your PATH
   - Check Python environment is properly configured
   - Verify internet connectivity for package downloads

4. **Git operations failing**
   - Ensure you're in a valid Git repository directory
   - Check if Git repository is not in a corrupted state
   - Verify you have proper file system permissions

## Support

For issues with:
- This persona configuration: Open an issue in the awesome-mcp-personas repository
- Individual MCP servers: Check respective server documentation
- API services: Refer to service provider documentation

## Contributing

To improve this persona:
1. Verify all tool names against actual MCP server implementations
2. Test each toolset with real-world scenarios
3. Document any additional tools discovered
4. Submit improvements via pull request

## License

This persona configuration is part of the Awesome MCP Personas project and follows the same licensing terms.