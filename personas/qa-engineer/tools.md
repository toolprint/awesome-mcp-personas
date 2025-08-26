# QA Engineer Tools Reference

This document provides a comprehensive reference for all tools available in the QA Engineer persona.

## Playwright Server Tools

**Server**: `@modelcontextprotocol/server-playwright`  
**Purpose**: Browser automation and web testing

| Tool | Description | Example Usage |
|------|-------------|---------------|
| `playwright.navigate` | Navigate to a specified URL | Navigate to login page |
| `playwright.fill` | Fill form fields with specified values | Enter username and password |
| `playwright.click` | Click on elements using selectors | Click login button |
| `playwright.screenshot` | Capture screenshots of pages | Take screenshot for evidence |
| `playwright.evaluate` | Execute JavaScript in browser context | Check page state or extract data |

## Docker Server Tools

**Server**: `docker-mcp`  
**Purpose**: Container lifecycle management and testing

| Tool | Description | Example Usage |
|------|-------------|---------------|
| `docker.list_containers` | List all containers (running and stopped) | Check test environment status |
| `docker.create_container` | Create new container from image | Set up test environment |
| `docker.start_container` | Start an existing container | Launch test suite container |
| `docker.stop_container` | Stop a running container | Clean up after test run |
| `docker.get_container_logs` | Retrieve logs from container | Get test execution logs |
| `docker.remove_container` | Delete a container | Clean up test artifacts |

## Slack Server Tools

**Server**: `slack-mcp-server`  
**Purpose**: Team communication and test reporting

| Tool | Description | Example Usage |
|------|-------------|---------------|
| `slack.channels_list` | List available Slack channels | Find appropriate reporting channel |
| `slack.conversations_add_message` | Send message to channel or user | Post test results summary |
| `slack.conversations_history` | Retrieve message history from channel | Check previous test reports |
| `slack.conversations_replies` | Get replies to specific messages | Follow up on test failure discussions |

## Tool Usage Examples by Workflow

### Browser Regression Testing
```
1. playwright.navigate → Open application URL
2. playwright.fill → Enter test data into forms  
3. playwright.click → Trigger actions (submit, navigate)
4. playwright.screenshot → Capture results for comparison
5. playwright.evaluate → Verify expected page state
```

### Containerized Test Execution
```
1. docker.create_container → Create test environment
2. docker.start_container → Launch the container
3. docker.get_container_logs → Monitor test execution
4. docker.stop_container → Clean up after completion
5. docker.remove_container → Remove temporary containers
6. docker.list_containers → Verify cleanup
```

### Test Reporting and Team Updates
```
1. slack.channels_list → Find relevant team channels
2. slack.conversations_add_message → Post test summary
3. slack.conversations_history → Review previous reports
4. slack.conversations_replies → Respond to questions about failures
```

## Environment Requirements

### Playwright
- No additional environment variables required
- Requires browsers to be installed (handled automatically by Playwright)

### Docker
- Requires Docker daemon to be running
- User must have Docker permissions
- No additional environment variables required

### Slack
- `SLACK_BOT_TOKEN`: Bot User OAuth Token (required)
- `SLACK_TEAM_ID`: Workspace Team ID (required)

## Common Tool Combinations

### End-to-End Test with Reporting
```
docker.create_container + docker.start_container
→ playwright.navigate + playwright.fill + playwright.click
→ playwright.screenshot + docker.get_container_logs  
→ slack.conversations_add_message
→ docker.stop_container + docker.remove_container
```

### Visual Regression Testing
```
playwright.navigate → playwright.screenshot → playwright.evaluate
→ (compare with baseline) → slack.conversations_add_message
```

### Test Environment Health Check
```
docker.list_containers → docker.get_container_logs
→ slack.conversations_add_message (status report)
```