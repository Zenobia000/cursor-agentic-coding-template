# Schema for progress.md

The `progress.md` file serves as a detailed log of the AI Agent's implementation activities and overall project progress within the current work cycle. It helps track what has been done, what's in progress, and any blockers encountered.

## File Structure

The file should use Level 2 (`##`) Markdown headers for main progress categories and Level 3 (`###`) for specific updates or task groups.

## Key Sections and Fields:

- **`## Current Sprint/Phase`**:
  - **Purpose:** Overview of the current sprint or phase.
  - **Expected Value:** Brief description (e.g., "Sprint: User Onboarding", "Phase: Backend Development").

- **`## Completed Tasks`**:
  - **Purpose:** Lists tasks that have been fully implemented and verified.
  - **Expected Value:** Markdown list items, often linked to `tasks.md`.

- **`## In Progress`**:
  - **Purpose:** Details on tasks currently being worked on.
  - **Expected Value:** Markdown list items with sub-details on progress.

- **`## Blocked/Issues`**:
  - **Purpose:** Documents any obstacles preventing task completion.
  - **Expected Value:** Markdown list items, including blocker details and duration.

- **`## Notes/Decisions`**:
  - **Purpose:** General observations, minor deviations from design, or quick decisions made during implementation.
  - **Expected Value:** Free-form text.

## Example:

```markdown
# Implementation Progress

## Current Sprint/Phase
Sprint: User Authentication Module (Week 1)
Started: 2025-12-18

## Completed Tasks
- [x] AUTH-01: Design Authentication API (Ref: memory-bank/current/creative-auth-api.md)
- [x] AUTH-02: Setup Auth Database Schema

## In Progress
- [ ] AUTH-03: Implement User Registration API (70% complete)
  - Implemented: POST /register endpoint basic logic
  - Next: Add input validation
- [ ] AUTH-04: Write Unit Tests for AUTH-03

## Blocked/Issues
- [ ] AUTH-05: Integrate with OAuth2 Provider
  - Blocked by: Awaiting client ID from Google (since 2025-12-17)

## Notes/Decisions
- Decided to use bcrypt for password hashing instead of argon2 due to library compatibility.
```
