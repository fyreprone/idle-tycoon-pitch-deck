# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Idle Tycoon: Pitch Deck** - A mobile idle/incremental game in initial planning phase.

## Current State

No code implementation exists yet. The repository contains:
- Claude Code agent configurations (`.claude/agents/`)
- Basic project documentation
- Git version control setup

## Next Steps Required

### 1. Technology Stack Decision
Choose one of the following approaches:

**Web-Based Options:**
- **Phaser.js**: JavaScript game framework, good for 2D games
- **React/Next.js**: Component-based with state management
- **Vue.js + Canvas**: Reactive framework with custom rendering

**Mobile-First Options:**
- **React Native**: Cross-platform JavaScript solution
- **Flutter**: Google's cross-platform framework
- **Unity**: C# based, good for complex games

### 2. Project Initialization

Once stack is selected, run appropriate initialization:

```bash
# For JavaScript/TypeScript projects:
npm init -y && npm install [framework]

# For Flutter:
flutter create idle_tycoon_pitch_deck

# For React Native:
npx react-native init IdleTycoonPitchDeck
```

### 3. Development Commands (To Be Defined)

After initialization, update this section with actual commands:
- Build command: `[TBD based on stack]`
- Dev server: `[TBD based on stack]`  
- Test runner: `[TBD based on stack]`
- Linting: `[TBD based on stack]`

## Architecture Guidelines

### Game State Structure (Pending Implementation)
```
src/
├── core/           # Game logic and calculations
├── ui/             # Interface components
├── state/          # State management
├── services/       # Backend/storage services
└── assets/         # Images, sounds, configs
```

### Design Principles
- **Progress Display as Hero**: Idle income and key metrics should be prominently displayed
- **Minimal Cognitive Load**: Interface should be immediately understandable
- **Mobile-First**: Touch targets minimum 44x44px
- **Performance**: Initial load < 3s, interactions < 100ms

## Available Claude Agents

Specialized agents in `.claude/agents/`:
- `ux-designer-developer`: UI/UX implementation for game interfaces
- `backend-api-developer`: Server-side logic and APIs
- `test-first-developer`: TDD enforcement
- `docs-maintainer`: Documentation updates
- `regression-test-guardian`: Test suite maintenance

## Repository Info

- **GitHub**: https://github.com/fyreprone/idle-tycoon-pitch-deck
- **Branch**: master
- **Status**: Awaiting technology stack selection and initial implementation