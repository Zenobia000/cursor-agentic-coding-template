# Schema for runbook.md

The `runbook.md` file provides operational procedures and troubleshooting guides for the project. It's designed to help maintainers and support staff quickly diagnose and resolve common issues, or perform routine maintenance tasks.

## File Structure

The file should use Level 2 (`##`) Markdown headers for main sections (e.g., "Deployment", "Troubleshooting") and Level 3 (`###`) for specific procedures.

## Key Sections and Fields:

- **`## Section Title`**:
  - **Purpose:** A high-level category for procedures (e.g., "Deployment Procedures").

- **`### Procedure Title`**:
  - **Purpose:** The title of a specific operational procedure (e.g., "Deploying to Production").

- **`#### Description`**:
  - **Purpose:** A brief overview of what the procedure achieves.

- **`#### Prerequisites`**:
  - **Purpose:** Any conditions or tools required before starting the procedure.

- **`#### Steps`**:
  - **Purpose:** A numbered list of actions to perform. Each step should be clear and actionable.

- **`#### Verification`**:
  - **Purpose:** How to confirm the procedure was successful.

- **`#### Rollback`**:
  - **Purpose:** (Optional) Steps to revert the changes if the procedure fails.

## Example:

```markdown
# Project Runbook: AI Code Review Assistant Operations

## Deployment Procedures

### Deploying to Production

#### Description
This procedure outlines the steps to deploy a new version of the AI Code Review Assistant to the production environment.

#### Prerequisites
- Access to the production AWS account.
- Latest Docker images pushed to ECR.
- All CI/CD pipelines for the release branch are green.

#### Steps
1. Log in to the AWS console.
2. Navigate to the ECS service for the AI Assistant.
3. Update the service to use the latest Docker image tag.
4. Monitor the deployment status in the ECS console.
5. Check application logs for any errors.

#### Verification
- Access the production health endpoint (e.g., `https://api.example.com/health`) and confirm a 200 OK response.
- Verify latest features are available in the staging environment after deployment.

#### Rollback
1. If errors occur, revert the ECS service to the previous stable Docker image tag.
2. Monitor application logs during rollback.

## Troubleshooting Guides

### High CPU Utilization on Backend Service

#### Description
Guide to diagnose and resolve high CPU utilization issues on the backend API service.

#### Prerequisites
- Access to Prometheus/Grafana dashboard.
- Access to backend service logs in CloudWatch.

#### Steps
1. Check Grafana dashboard for CPU usage over time.
2. Examine CloudWatch logs for recent error spikes or unusual traffic patterns.
3. Identify top CPU-consuming endpoints or database queries via APM tools.
4. If a specific query is identified, check database query plans.

#### Verification
- CPU utilization returns to normal levels in Grafana.
- No new errors related to high CPU appear in logs.
```
