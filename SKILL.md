---
name: test-skill
description: "A test skill for Hermes Agent demonstrating GitHub integration and MCP functionality"
version: 1.0.0
author: WLittleBug
license: MIT
metadata:
  hermes:
    tags: [github, mcp, test, integration]
    homepage: https://github.com/WLittleBug/test-skill
    related_skills: [github-pr-workflow, github-issues, github-repo-management]
---

# Test Skill

A demonstration skill showing how to integrate GitHub functionality with Hermes Agent using MCP (Model Context Protocol).

## Features

- GitHub repository management
- MCP server integration examples
- Cross-platform tool usage
- Skill installation and management

## Quick Start

Install this skill:
```bash
hermes skills install https://github.com/WLittleBug/test-skill/blob/main/SKILL.md
```

Or via npx:
```bash
npx skills add WLittleBug/test-skill
```

## Usage Examples

### GitHub Repository Operations
```python
# Create a new repository
mcp_github_create_repository(name="my-new-repo", description="A test repository")

# Create a file in repository
mcp_github_create_or_update_file(
    owner="WLittleBug",
    repo="test-skill",
    path="README.md",
    content="# Test Repository\n\nThis is a test repository created by Hermes Agent",
    message="Add README.md",
    branch="main"
)

# Get repository contents
mcp_github_get_file_contents(
    owner="WLittleBug", 
    repo="test-skill", 
    path="."
)
```

### Issue Management
```python
# Create an issue
mcp_github_create_issue(
    owner="WLittleBug",
    repo="test-skill",
    title="Test Issue",
    body="This is a test issue created by Hermes Agent"
)

# List issues
mcp_github_list_issues(
    owner="WLittleBug",
    repo="test-skill",
    state="open"
)
```

## MCP Integration

This skill demonstrates how to work with GitHub's MCP server to provide:

- Repository management
- File operations
- Issue tracking
- Pull request workflows
- Code search capabilities

## Configuration

Ensure you have GitHub authentication set up:

```bash
# Login with GitHub CLI
gh auth login

# Or set environment variables
export GITHUB_TOKEN=your_personal_access_token
```

## Development

To contribute to this skill:

1. Fork the repository
2. Make your changes
3. Test locally:
   ```bash
   hermes skills install ./SKILL.md
   ```
4. Submit a pull request

## License

MIT License - see LICENSE file for details.
