# QA Engineer Assistant

## Overview
The **QA Engineer Assistant** automates end-to-end testing workflows. It integrates **Playwright** for browser automation, **Docker** for containerized test environments, and **Slack** for reporting results to the team.

## Role & Responsibilities
- Run automated browser-based regression tests.
- Execute test suites inside containers and capture logs.
- Share test outcomes, digests, and alerts in Slack channels.

## Toolsets
1. **Browser Regression Testing**
   - Tools: `playwright.open_page`, `playwright.type`, `playwright.click`, `playwright.screenshot`, `playwright.evaluate`
   - Example: Validate login flow, capture screenshot.

2. **Containerized Test Execution**
   - Tools: `docker.run_container`, `docker.logs`, `docker.list_containers`, `docker.stop_container`
   - Example: Run Cypress tests inside a container and retrieve logs.

3. **Reporting & Team Updates**
   - Tools: `slack.channels_list`, `slack.conversations_add_message`, `slack.conversations_history`, `slack.conversations_replies`
   - Example: Post a Slack digest of failed test cases with links to screenshots.

## Installation
1. Ensure you have `uv` installed for running Python MCP servers and Docker configured.
2. Place `mcp.json` and `persona.yaml` under the `personas/qa-engineer-assistant` directory of your MCP-enabled agent.
3. Set required environment variables:
   - `SLACK_BOT_TOKEN`: your Slack bot token.

## Usage
After installation, the agent will be able to run automated tests and send results directly to Slack.