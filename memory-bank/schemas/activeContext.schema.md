# Schema for activeContext.md

The `activeContext.md` file serves as a dynamic snapshot of the AI Agent's current operational state and focus. It's updated by various commands to ensure continuity and clarity across different modes.

## File Structure

The file should use Level 2 (`##`) Markdown headers for main sections.

## Key Sections and Fields:

- **`## Current Phase`**:
  - **Purpose:** Indicates the currently active command/mode (e.g., `PLAN MODE`, `IMPLEMENT MODE`).
  - **Expected Value:** A string representing the active command.

- **`## Current Focus`**:
  - **Purpose:** A brief description of the specific task or objective the AI Agent is currently working on within the active phase.
  - **Expected Value:** A descriptive string.

- **`## Last Action`**:
  - **Purpose:** Records the last significant action taken by the AI Agent. Useful for resuming work or understanding recent history.
  - **Expected Value:** A descriptive string (e.g., "Updated tasks.md", "Generated PM Briefing").

- **`## Notes`**:
  - **Purpose:** Any additional relevant context or temporary information.
  - **Expected Value:** Free-form text.

## Example:

```markdown
# Active Context

## Current Phase
IMPLEMENT MODE

## Current Focus
Implementing user authentication module

## Last Action
Wrote failing test for user login (TDD cycle started)

## Notes
Considering OAuth2 for social logins later.
```
