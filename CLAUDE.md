# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Project Name:** Idle Tycoon: Pitch Deck  
**Type:** Mobile Idle/Incremental Game  
**Status:** Initial Planning Phase - No code implementation yet

## Repository Structure

This is an early-stage repository with minimal implementation:

```
idle-tycoon-pitch-deck/
├── .claude/                    # Claude Code agent configurations
│   ├── agents/                 # Specialized development agents (7 agents available)
│   └── README.md              # Agent sync documentation
├── .git/                      # Git version control
├── CLAUDE.md                  # This file
├── README.md                  # Basic project readme
└── claude-code-permissions.yaml # Bash command permissions (1300+ lines)
```

## Available Claude Agents

The `.claude/agents/` directory contains 7 specialized agents for different development tasks:

- **backend-api-developer** (265 lines): Server-side logic, APIs, and database operations
- **docs-architecture-maintainer** (209 lines): Technical documentation and architecture decisions
- **docs-maintainer** (96 lines): General documentation management and updates
- **regression-test-guardian** (278 lines): Comprehensive test suite maintenance and validation
- **test-first-developer** (106 lines): Test-driven development enforcement
- **ux-designer-developer** (90 lines): UI/UX design and game interface implementation
- **ux-frontend-developer** (169 lines): Frontend development and user interface patterns

## Current State & Next Decisions

### Immediate Requirements
1. **Technology Stack Selection**: Choose platform (Web/Mobile/Cross-platform)
2. **Framework Decision**: Select game engine or framework
3. **Project Initialization**: Set up build system, dependencies, and tooling
4. **Architecture Planning**: Define code organization and patterns

### Key Architectural Decisions Pending
- **Platform**: Web browser, React Native, Flutter, or native mobile
- **Game Engine**: Custom implementation, Phaser.js, Unity, or Cocos2d
- **Backend Strategy**: Node.js/Express, serverless functions, or game-as-a-service
- **State Management**: Local storage, cloud saves, or hybrid approach
- **Deployment**: Static hosting, app stores, or progressive web app

## Development Workflow

### Project Initialization Process
Once technology stack is selected, the workflow will be:
1. Initialize project with chosen framework/build tools
2. Configure development environment (linting, testing, bundling)
3. Implement basic project structure and conventions
4. Update this CLAUDE.md with build commands and architecture details

### Expected Build Commands (TBD)
After project initialization, typical commands will include:
- `npm run dev` or equivalent for development server
- `npm run build` for production builds
- `npm run test` for running test suites
- `npm run lint` for code quality checks

## Repository Information

- **GitHub**: https://github.com/fyreprone/idle-tycoon-pitch-deck
- **Branch Strategy**: Currently on master branch
- **Primary Language**: TBD (will be JavaScript/TypeScript, Dart, C#, or other based on stack choice)
- **Created**: September 2025
- **Initial Commit**: 7b52623 "Initial commit"

## Agent Sync Strategy

Agents are version-controlled via Git and automatically synced across environments. The `.claude/agents/` directory uses GitHub as the primary source for agent definitions, ensuring consistency across all development environments.