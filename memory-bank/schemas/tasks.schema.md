# Schema for tasks.md

The `tasks.md` file is the single source of truth for all planned work in the project. It follows a Markdown-based Work Breakdown Structure (WBS).

## File Structure

The file should be organized into sections using Level 2 (`##`) Markdown headers. Suggested sections include:

- `## Epics`
- `## Current Sprint`
- `## Future Ideas`
- `## Technical Debt`

## Task Item Format

Each task item should be a list item (`-`) and follow this structure:

```markdown
- [ ] **[Task ID (Optional)]:** [Task Title] - `Status: [pending|in-progress|completed|blocked]`
  - **Description:** (A brief, one-sentence description of the task.)
  - **Depends on:** `[Task ID]` or `N/A`
  - **Deliverable:** (What is the expected output? e.g., "A new React component `Button.tsx`", "API documentation for /users endpoint")
  - **Design Doc:** `[path/to/creative-doc.md]` or `N/A`
```

### Key Fields:

- **Checkbox:** `[ ]` for pending/in-progress, `[x]` for completed.
- **Task ID:** A unique identifier (e.g., `AUTH-01`, `TASK-123`). Optional for smaller tasks.
- **Task Title:** A clear, concise title.
- **Status:** Must be one of `pending`, `in-progress`, `completed`, or `blocked`.
- **Description:** A brief explanation of the task's goal.
- **Depends on:** Crucial for dependency mapping. Lists the ID(s) of tasks that must be completed first.
- **Deliverable:** The tangible output of the task.
- **Design Doc:** A link to the relevant `creative-*.md` document in the memory bank.

### Example:

```markdown
## Current Sprint: User Authentication

- [ ] **AUTH-01:** Design Authentication API - `Status: pending`
  - **Description:** Design the RESTful endpoints for user registration, login, and logout.
  - **Depends on:** `N/A`
  - **Deliverable:** An OpenAPI specification file.
  - **Design Doc:** `N/A`

- [ ] **AUTH-02:** Implement Authentication API - `Status: pending`
  - **Description:** Write the backend code for the user authentication service.
  - **Depends on:** `AUTH-01`
  - **Deliverable:** Running endpoints on the dev server.
  - **Design Doc:** `memory-bank/current/creative-auth-api.md`
```
