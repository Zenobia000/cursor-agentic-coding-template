# Schema for techContext.md

The `techContext.md` file provides a detailed overview of the technical environment, technology stack, and key tools used in the project. It serves as a central reference for all AI Agents and human developers to understand the technological landscape and make informed decisions.

## File Structure

The file should use Level 2 (`##`) Markdown headers for main sections, covering different aspects of the technology stack.

## Key Sections and Fields:

- **`## Section Title`**:
  - **Purpose:** A high-level category for technology components (e.g., "Backend Technologies", "Frontend Frameworks").

- **`### Technology/Tool Name`**:
  - **Purpose:** The name of a specific technology or tool (e.g., "Python 3.10", "React 18", "PostgreSQL").

- **`#### Version`**:
  - **Purpose:** The specific version being used.

- **`#### Purpose/Role`**:
  - **Purpose:** Explains why this technology was chosen and what role it plays in the project.

- **`#### Key Libraries/Frameworks`**:
  - **Purpose:** Lists important libraries or frameworks built on top of this technology.

- **`#### Configuration Details`**:
  - **Purpose:** (Optional) Provides high-level configuration notes or links to detailed config files.

## Example:

```markdown
# Technical Context: AI Code Review Assistant

## Backend Technologies

### Python 3.10

#### Version
3.10.x

#### Purpose/Role
Primary language for backend services and AI model integration. Chosen for its rich ecosystem and ease of development.

#### Key Libraries/Frameworks
- FastAPI (for REST APIs)
- SQLAlchemy (ORM for database interaction)
- Pydantic (data validation)
- Transformers (for AI model inference)

#### Configuration Details
Virtual environments managed with `poetry`.

### PostgreSQL 14

#### Version
14.x

#### Purpose/Role
Primary relational database for persistent data storage (e.g., user data, review history, project configurations).

#### Key Libraries/Frameworks
- pgAdmin (database management tool)
- psycogreen (for asynchronous database operations)

#### Configuration Details
Managed via Docker Compose in development, AWS RDS in production.

## Frontend Technologies

### React 18

#### Version
18.x

#### Purpose/Role
JavaScript library for building user interfaces. Chosen for its component-based architecture and large community support.

#### Key Libraries/Frameworks
- Next.js 13 (React framework for server-side rendering and routing)
- Tailwind CSS (utility-first CSS framework)
- Zustand (state management)

#### Configuration Details
TypeScript is used for all frontend code.

## Cloud Infrastructure

### AWS

#### Version
N/A (using various services)

#### Purpose/Role
Cloud provider for hosting and managing services.

#### Key Services
- ECS (Elastic Container Service) for service deployment.
- RDS (Relational Database Service) for PostgreSQL.
- S3 (Simple Storage Service) for static assets and backups.
- Lambda (serverless functions for event-driven tasks).

## Development Tools

### Docker

#### Version
24.x

#### Purpose/Role
Containerization platform for consistent development and production environments.

### VS Code

#### Version
Latest stable

#### Purpose/Role
Primary IDE for all development work.
```
