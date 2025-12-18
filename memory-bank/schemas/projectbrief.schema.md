# Schema for projectbrief.md

The `projectbrief.md` file serves as the overarching guide for the entire project. It contains the high-level vision, goals, scope, and key stakeholders. It acts as the primary reference for all AI Agents to align their work with the project's strategic direction.

## File Structure

The file should use Level 1 (`#`) or Level 2 (`##`) Markdown headers for main sections.

## Key Sections and Fields:

- **`# Project Title`**:
  - **Purpose:** The official name of the project.

- **`## Vision`**:
  - **Purpose:** A concise statement describing the long-term desired future state that the project aims to achieve.
  - **Expected Value:** 1-2 sentences.

- **`## Mission/Goals`**:
  - **Purpose:** Specific, measurable, achievable, relevant, and time-bound (SMART) objectives for the project.
  - **Expected Value:** A list of bullet points.

- **`## Scope`**:
  - **Purpose:** Defines what is included and, crucially, what is *excluded* from the project.
  - **Expected Value:** A list of bullet points for in-scope and out-of-scope items.

- **`## Target Audience`**:
  - **Purpose:** Description of the primary users or beneficiaries of the project.

- **`## Key Deliverables`**:
  - **Purpose:** The main outputs or results the project is expected to produce.

- **`## Success Metrics`**:
  - **Purpose:** Quantifiable indicators that will be used to determine if the project is successful.

- **`## Constraints & Assumptions`**:
  - **Purpose:** Limitations (time, budget, resources) and beliefs taken for granted.

## Example:

```markdown
# Project Brief: AI-Powered Code Review Assistant

## Vision
To significantly reduce code review cycles and improve code quality by providing an intelligent, context-aware AI assistant that can identify potential issues and suggest improvements.

## Mission/Goals
- Automate 50% of routine code review comments by Q2 2026.
- Improve average code quality score by 15% (measured by SonarQube) by end of 2026.
- Reduce average code review time by 2 hours per PR.

## Scope
### In Scope:
- Static analysis for common code smells (e.g., God Objects, N+1 queries).
- Integration with Git-based platforms (GitHub/GitLab).
- Suggestion of code refactoring patterns.

### Out of Scope:
- Runtime performance analysis.
- Full security vulnerability scanning (will integrate with existing tools).
- Natural language generation for conversational code review.

## Target Audience
Software development teams using Git-based version control.

## Key Deliverables
- Functional AI agent integrating with GitHub PRs.
- Detailed code review reports.
- Comprehensive documentation for setup and usage.

## Success Metrics
- Average PR review time (baseline: 4h) reduced to 2h.
- Code quality metric (baseline: 70) increased to 85.
- User satisfaction score > 4/5.

## Constraints & Assumptions
- **Constraint:** Max 2 full-time developers allocated.
- **Assumption:** Existing codebase is primarily in Python/TypeScript.
```
