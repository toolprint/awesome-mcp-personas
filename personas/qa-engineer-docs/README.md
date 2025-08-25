# QA Engineer Docs

## Overview
The **QA Engineer Docs** persona automates testing workflows and generates structured test reports. It integrates **Playwright** for browser automation, **filesystem** operations for report generation, and **Brave Search** for researching testing best practices.

## Role & Responsibilities
- Automate and run browser-based tests using Playwright
- Generate structured test reports and documentation
- Research testing frameworks, patterns, and best practices
- Capture screenshots and evidence during test execution
- Create organized test report directories

## Toolsets

### 1. Browser Automation
- **Tools**: `playwright.navigate`, `playwright.screenshot`, `playwright.click`, `playwright.fill`, `playwright.evaluate`, `playwright.wait`
- **Purpose**: Automate browser interactions, navigate pages, capture screenshots, and validate UI behavior
- **Example**: Navigate to login page, fill credentials, click submit, verify successful login

### 2. Test Reporting
- **Tools**: `filesystem.read_file`, `filesystem.write_file`, `filesystem.create_directory`, `filesystem.list_directory`, `filesystem.delete`
- **Purpose**: Generate and manage test reports, save screenshots, create structured documentation
- **Example**: Create test report directory, write HTML/Markdown reports, save screenshot evidence

### 3. Test Research
- **Tools**: `brave-search.search`
- **Purpose**: Research testing best practices, find documentation, discover testing patterns
- **Example**: Search for Playwright best practices, find testing framework comparisons

## Installation

1. Ensure you have Node.js installed for running MCP servers
2. Place the persona files in the `personas/qa-engineer-docs` directory of your MCP-enabled agent
3. Set the `BRAVE_API_KEY` environment variable for search functionality (optional)
4. The filesystem server will create test reports in the `./test-reports` directory

## Configuration Files

- **mcp.json**: Contains the MCP server configurations for Playwright, filesystem, and search
- **persona.yaml**: Defines the toolsets and capabilities of this persona

## Usage

After installation, the persona can:
- Run automated browser tests with Playwright
- Generate test reports in HTML or Markdown format
- Organize test artifacts and screenshots
- Research testing solutions and best practices

## Example Workflow

1. Navigate to application under test
2. Perform user interactions (clicks, form fills)
3. Capture screenshots at key points
4. Generate test report with results
5. Save report and artifacts to filesystem

## Requirements

- Node.js 16+ for MCP servers
- Optional: Brave API key for search functionality
- Write access to `./test-reports` directory