# Claude Code Agents Configuration

This directory contains Claude Code agent definitions that are synced across all development environments via GitHub.

## Agent Sync Policy

**GitHub is the default and primary source for Claude Code agent configuration.**

### Why GitHub Sync?

- **Version Control**: Track changes to agent behavior over time
- **Team Collaboration**: Share specialized agents across development team
- **Backup & Recovery**: Agents are backed up with your code
- **Environment Consistency**: Same agent behavior on every machine
- **Portability**: Take your agents to any development environment

### Agent Management Workflow

1. **Create/Edit Agents**: Modify `.md` files in this directory
2. **Test Locally**: Verify agent behavior in your current environment
3. **Commit Changes**: Add agent files to git and create descriptive commits
4. **Push to GitHub**: Share changes with all environments
5. **Pull on Other Devices**: Other environments get updates via `git pull`

### Agent File Structure

Each agent is defined as a markdown file with YAML frontmatter:

```yaml
---
name: agent-name
description: Brief description of what this agent does and when to use it
model: sonnet  # or opus, haiku
color: blue    # optional UI color hint
---

# Agent Instructions

Detailed instructions for the agent in markdown format...
```

### Current Agents

- **test-first-developer.md**: Enforces Test-Driven Development (TDD) approach
- **ux-designer-developer.md**: Handles UI/UX implementation following design specs  
- **docs-maintainer.md**: Manages documentation updates and archival

### Creating New Agents

```bash
# Create new agent
touch .claude/agents/my-agent.md

# Edit with your preferred editor
nano .claude/agents/my-agent.md

# Commit and sync
git add .claude/agents/my-agent.md
git commit -m "Add new agent: my-agent for specific task"
git push
```

### Agent Naming Conventions

- Use lowercase with hyphens: `my-new-agent.md`
- Be descriptive but concise: `api-testing-specialist.md`
- Avoid spaces or special characters: `backend_validator.md` ❌ → `backend-validator.md` ✅

### Best Practices

1. **Specific Purpose**: Each agent should have a clear, focused responsibility
2. **Clear Descriptions**: Make it obvious when to use each agent
3. **Consistent Format**: Follow the established YAML frontmatter pattern
4. **Version Comments**: Document major changes in commit messages
5. **Test Before Pushing**: Verify agent behavior before sharing with team

### Syncing Across Environments

#### New Environment Setup
```bash
git clone https://github.com/fyreprone/idle-tycoon-pitch-deck.git
cd idle-tycoon-pitch-deck
# Agents are automatically available in .claude/agents/
```

#### Regular Updates
```bash
git pull  # Gets latest agent updates from team
```

#### Sharing Agent Updates
```bash
git add .claude/agents/
git commit -m "Update agent configurations"
git push  # Shares with all environments
```

### Troubleshooting

- **Agent Not Found**: Ensure you've pulled latest changes with `git pull`
- **Agent Conflicts**: Use git merge tools to resolve conflicting agent definitions
- **Missing Agents**: Check if `.claude/agents/` directory exists and contains `.md` files

### Integration with Project Workflow

Agents are automatically loaded by Claude Code when:
- Starting a new session in the repository
- Running `/agents` command to list available agents
- Using specialized agent tasks during development

The `.claude/` directory is part of your project's version control and follows the same branching/merging strategies as your code.