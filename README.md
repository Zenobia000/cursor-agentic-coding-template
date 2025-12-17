# Cursor Agentic Coding Template

A structured development workflow template for **Cursor IDE** that combines Custom Slash Commands with a Memory Bank system to maintain context across development phases.

## Overview

This template provides a systematic approach to AI-assisted development by:

- **Phased Workflow**: Six distinct phases from initialization to documentation
- **Memory Bank**: Persistent context storage between sessions
- **Custom Commands**: Pre-configured slash commands for each development phase
- **Quality Rules**: Built-in rules for code quality, security, and best practices

## Quick Start

### 1. Clone and Open in Cursor

```bash
git clone https://github.com/Zenobia000/cursor-agentic-coding-template.git
cd cursor-agentic-coding-template
```

Open the folder in Cursor IDE.

### 2. Initialize Your Project

In Cursor AI chat, type:

```
/van
```

This creates the Memory Bank structure and prepares the project.

### 3. Follow the Workflow

```
/van → /plan → /creative → /implement → /reflect → /archive
```

## Project Structure

```
cursor-agentic-coding-template/
├── .cursor/
│   ├── commands/           # Slash command definitions
│   │   ├── van.md          # Initialization
│   │   ├── plan.md         # Task planning
│   │   ├── creative.md     # Design decisions
│   │   ├── implement.md    # Code implementation
│   │   ├── reflect.md      # Retrospective
│   │   ├── archive.md      # Documentation
│   │   ├── debug.md        # Debugging helper
│   │   ├── review-code.md  # Code review
│   │   ├── write-tests.md  # Test writing
│   │   ├── api-design.md   # API design
│   │   └── ...
│   └── rules/              # Project rules
│       ├── 00-global.mdc   # Core principles
│       ├── ai.mdc          # AI guidelines
│       ├── backend.mdc     # Backend rules
│       ├── frontend.mdc    # Frontend rules
│       ├── testing.mdc     # Testing standards
│       ├── git-workflow.mdc
│       ├── deployment.mdc
│       └── isolation_rules/
│           ├── main.mdc    # System core
│           └── ...
├── memory-bank/            # Persistent context storage
│   ├── tasks.md            # Task list (Source of Truth)
│   ├── activeContext.md    # Current focus
│   ├── progress.md         # Implementation status
│   └── README.md           # Memory Bank guide
├── .cursorrules            # Auto-loaded project rules
└── README.md
```

## Workflow Phases

### Phase 1: `/van` - Initialization

Creates and verifies the Memory Bank structure.

**Creates:**
- `memory-bank/tasks.md` - Task tracking
- `memory-bank/activeContext.md` - Current context

### Phase 2: `/plan` - Task Planning

Breaks down high-level goals into actionable tasks using WBS (Work Breakdown Structure).

**Reads:** `tasks.md`, `activeContext.md`
**Updates:** `tasks.md` with detailed task breakdown

### Phase 3: `/creative` - Design Decisions

Documents architectural decisions, technical choices, and design patterns.

**Reads:** `tasks.md`
**Creates:** `creative-*.md` design documents

### Phase 4: `/implement` - Implementation

Executes the plan with progress tracking.

**Reads:** `tasks.md`, `creative-*.md`
**Updates:** `progress.md`, `tasks.md`

### Phase 5: `/reflect` - Retrospective

Reviews completed work, documents lessons learned.

**Reads:** `tasks.md`, `progress.md`
**Updates:** `tasks.md` with insights

### Phase 6: `/archive` - Documentation

Finalizes documentation and preserves knowledge.

**Archives:** All Memory Bank files to `docs/` or `archive/`

## Additional Commands

| Command | Purpose |
|---------|---------|
| `/debug` | Structured debugging workflow |
| `/review-code` | Code review checklist (functionality, security, performance) |
| `/write-tests` | Test writing with AAA pattern and coverage targets |
| `/optimize-performance` | Frontend/backend performance optimization |
| `/api-design` | RESTful API design with OpenAPI specs |
| `/task-init` | Initialize a new task with WBS |
| `/task-next` | Continue to next task |

## Memory Bank

The Memory Bank is a persistent context storage system that maintains continuity across development sessions.

### Core Files

| File | Purpose | Created By |
|------|---------|------------|
| `tasks.md` | Single source of truth for all tasks | `/van` |
| `activeContext.md` | Current phase and focus | `/van` |
| `creative-*.md` | Design decisions and architecture | `/creative` |
| `progress.md` | Implementation status and blockers | `/implement` |

### Best Practices

1. **Always start with `/van`** to verify Memory Bank exists
2. **Update frequently** after completing significant work
3. **Keep tasks.md as source of truth** for all task status
4. **Include Memory Bank in Git** for team collaboration

## Built-in Rules

### Code Quality (`00-global.mdc`)

- TypeScript strict mode, Python 3.10+
- No `any` types - explicit typing required
- Functional programming preferred
- Single responsibility principle
- DRY (Don't Repeat Yourself)

### Security

- No hardcoded secrets - use environment variables
- SQL injection prevention - parameterized queries
- XSS protection - sanitize all user input
- Input validation - never trust client data

### Naming Conventions

| Type | Convention | Example |
|------|------------|---------|
| Variables/Functions | camelCase | `getUserData` |
| Classes/Types | PascalCase | `UserService` |
| Constants | UPPER_SNAKE_CASE | `MAX_RETRIES` |
| Files | kebab-case | `user-service.ts` |

### Git Workflow

```
type(scope): subject

# Types: feat, fix, docs, style, refactor, test, chore
# Example: feat(auth): add OAuth2 login support
```

## Platform Support

The system auto-detects the operating system and uses appropriate commands:

| Action | Linux/Mac | Windows |
|--------|-----------|---------|
| Create file | `touch file.txt` | `echo. > file.txt` |
| Create directory | `mkdir -p dir` | `mkdir dir` |
| View content | `cat file.txt` | `type file.txt` |
| List files | `ls -la` | `dir` |

## Requirements

- **Cursor IDE** version 2.0+
- Custom Slash Commands support (enabled by default in Cursor 2.x)

## Verification

Run the setup verification script:

```bash
# Linux/Mac
./.cursor/rules/isolation_rules/verify_setup.sh

# Windows (Git Bash)
bash ./.cursor/rules/isolation_rules/verify_setup.sh
```

## Customization

### Adding Custom Commands

Create a new file in `.cursor/commands/`:

```markdown
---
description: Your command description
---

# Command Name

Your command instructions here...
```

### Adding Custom Rules

Create a new `.mdc` file in `.cursor/rules/`:

```markdown
---
description: "Rule description"
alwaysApply: true
---

# Rule Title

Your rules here...
```

## Workflow Diagram

```
                    ┌─────────────────────────────────────────┐
                    │           Development Workflow          │
                    └─────────────────────────────────────────┘
                                        │
                    ┌───────────────────▼───────────────────┐
                    │              /van                      │
                    │         Initialize Project             │
                    │    Create Memory Bank Structure        │
                    └───────────────────┬───────────────────┘
                                        │
                    ┌───────────────────▼───────────────────┐
                    │              /plan                     │
                    │          Task Planning                 │
                    │     Break down into WBS tasks          │
                    └───────────────────┬───────────────────┘
                                        │
                    ┌───────────────────▼───────────────────┐
                    │            /creative                   │
                    │        Design Decisions                │
                    │   Architecture & technical choices     │
                    └───────────────────┬───────────────────┘
                                        │
                    ┌───────────────────▼───────────────────┐
                    │           /implement                   │
                    │       Code Implementation              │
                    │    Write code with tracking            │
                    └───────────────────┬───────────────────┘
                                        │
                    ┌───────────────────▼───────────────────┐
                    │            /reflect                    │
                    │          Retrospective                 │
                    │   Review & lessons learned             │
                    └───────────────────┬───────────────────┘
                                        │
                    ┌───────────────────▼───────────────────┐
                    │            /archive                    │
                    │         Documentation                  │
                    │    Finalize & preserve knowledge       │
                    └───────────────────────────────────────┘
```

## Troubleshooting

### Commands not working

1. Verify Cursor version >= 2.0
2. Check `.cursor/commands/` directory exists
3. Restart Cursor IDE

### Memory Bank creation fails

1. Check directory permissions
2. Manually create `memory-bank/` directory
3. Run `/van` again

### Rules not loading

1. Verify `.cursorrules` file exists in project root
2. Check `.cursor/rules/` directory structure
3. Review Cursor AI error messages

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit changes: `git commit -m "feat: add your feature"`
4. Push to branch: `git push origin feature/your-feature`
5. Open a Pull Request

## License

MIT License - See [LICENSE](LICENSE) for details.

## References

- [Cursor Documentation](https://docs.cursor.com/)
- [Custom Slash Commands](https://docs.cursor.com/commands)
- [Rules System](https://docs.cursor.com/rules)

---

**System Version**: 2.0 (2025)
**Architecture**: Custom Slash Commands + Memory Bank
**Status**: Production Ready
