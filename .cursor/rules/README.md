# AI Agent Rules Manifest

This directory contains the guiding principles, rules, and best practices that all AI Agents must adhere to when operating within this project. Each command in the `.cursor/commands/` directory explicitly lists which of these rules it should follow.

## Directory Structure

- **`/principles`**: High-level, overarching principles that apply to all agents and tasks (e.g., global style, AI behavior).
- **`/process`**: Rules governing the development process and workflow (e.g., Git workflow, deployment, planning).
- **`/backend`**: Rules and best practices specific to backend development.
- **`/frontend`**: Rules and best practices specific to frontend development.
- **`/testing`**: The "testing bible". Contains all rules related to writing tests, coverage, and strategy.
- **`/patterns`**: (Optional) Can be used to store specific design pattern implementations (e.g., `singleton.mdc`, `observer.mdc`).
- **`/isolation_rules`**: **[CORE]** Fundamental rules that define the agent's core operational loop and safety procedures. These are foundational and generally applied everywhere.

## Rules Catalog

### Principles
- **`principles/global.mdc`**: Global coding standards and formatting. (Formerly `00-global.mdc`)
- **`principles/ai-behavior.mdc`**: Defines the desired behavior, tone, and personality of the AI agent. (Formerly `ai.mdc`)

### Process
- **`process/git-workflow.mdc`**: Rules for branching, committing, and creating pull requests. (Formerly `git-workflow.mdc`)
- **`process/deployment.mdc`**: Checklist and rules for deploying the application. (Formerly `deployment.mdc`)

### Backend
- **`backend/overview.mdc`**: General best practices for backend development (e.g., API design, data modeling). (Formerly `backend.mdc`)

### Frontend
- **`frontend/overview.mdc`**: General best practices for frontend development (e.g., state management, component structure). (Formerly `frontend.mdc`)

### Testing
- **`testing/overview.mdc`**: Defines the testing strategy, TDD/BDD principles, and code coverage goals. (Formerly `testing.mdc`)

### Isolation Core
- **`isolation_rules/main.mdc`**: The master file for the agent's core operational logic.
- **`isolation_rules/Core/...`**: Componentized parts of the core logic.
