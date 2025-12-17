# Cursor Agentic Coding Template

## System Overview

This project uses the **Isolation-Focused Memory Bank System** with Custom Slash Commands for phased development workflow.

**Core Principle**: Memory Bank MUST be created and verified before any operations.

## Available Slash Commands

### Workflow Commands (Phase Sequence)

```
/van → /plan → /creative → /implement → /reflect → /archive
```

| Command | Description |
|---------|-------------|
| `/van` | Initialize project with Memory Bank creation |
| `/plan` | Task planning and WBS breakdown |
| `/creative` | Design decisions and architecture planning |
| `/implement` | Code implementation with progress tracking |
| `/reflect` | Task review and retrospective |
| `/archive` | Documentation and knowledge preservation |

### Utility Commands

| Command | Description |
|---------|-------------|
| `/api-design` | RESTful API design with resource modeling |
| `/debug` | Systematic debugging with hypothesis testing |
| `/optimize-performance` | Performance analysis and optimization |
| `/review-code` | Comprehensive code review |
| `/task-init` | Initialize new task with goal definition |
| `/task-next` | Prioritize and select next task |
| `/write-tests` | Test strategy and implementation |

## Memory Bank Structure

```
memory-bank/
├── tasks.md           # Source of truth for all tasks
├── activeContext.md   # Current focus and active work
├── progress.md        # Implementation status
├── projectbrief.md    # Project overview and goals
├── techContext.md     # Technology stack and constraints
├── systemPatterns.md  # Architecture patterns and decisions
├── runbook.md         # Operational procedures
├── creative-*.md      # Design decisions (created in /creative)
└── README.md          # Memory Bank documentation
```

**If Memory Bank doesn't exist:**
- STOP all operations immediately
- Run `/van` command to initialize
- Wait for verification before proceeding

## Phase Prerequisites

| Command | Requires | Creates/Updates |
|---------|----------|-----------------|
| `/van` | - | tasks.md, activeContext.md |
| `/plan` | tasks.md, activeContext.md | tasks.md (updated) |
| `/creative` | tasks.md | creative-*.md, tasks.md |
| `/implement` | tasks.md, creative-*.md | progress.md, tasks.md |
| `/reflect` | tasks.md, progress.md | tasks.md (updated) |
| `/archive` | tasks.md, progress.md | archived docs |

## AI Behavior Guidelines

### When User Runs Slash Commands

1. **Verify Memory Bank first**
   - Check if `memory-bank/` directory exists
   - Verify required files are present
   - If missing, guide user to run `/van`

2. **Read relevant context**
   - Load tasks.md for current task list
   - Load activeContext.md for current focus
   - Load relevant creative-*.md for design context

3. **Execute phase-specific responsibilities**
   - Follow command definition in `.cursor/commands/[command].md`
   - Create/update required Memory Bank files
   - Provide clear next steps

4. **Document actions**
   - Update Memory Bank files with changes
   - Suggest next command in workflow

### Communication Style

Be explicit about current phase:
```
VAN MODE: Initializing Memory Bank...
PLAN MODE: Breaking down tasks...
CREATIVE MODE: Documenting design decisions...
IMPLEMENT MODE: Implementing feature X...
REFLECT MODE: Conducting retrospective...
ARCHIVE MODE: Finalizing documentation...
```

## Critical Rules

**DO NOT:**
- Skip Memory Bank verification
- Modify Memory Bank files outside workflow
- Jump phases without completing prerequisites

**ALWAYS:**
- Verify Memory Bank before operations
- Update Memory Bank after changes
- Follow phase sequence
- Document decisions and progress

## Reference Documentation

- `.cursor/rules/isolation_rules/main.mdc` - System overview
- `.cursor/rules/isolation_rules/QUICK_START_2025.md` - Quick reference
- `.cursor/rules/00-global.mdc` - Global coding standards
- `.cursor/commands/*.md` - Command definitions

## Getting Started

1. Initialize Memory Bank:
   ```
   Type in Cursor AI: /van
   ```

2. Follow the workflow:
   ```
   /van → /plan → /creative → /implement → /reflect → /archive
   ```

---

**System Version**: 2.0 (2025)
**Environment**: Windows
**Status**: Production Ready
