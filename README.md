# DevOps Study Notes

This repository contains a practical overview of core DevOps concepts, Agile project tracking tools, Azure DevOps services, CI/CD pipelines, GitOps, and containerization. These notes are useful for learning, revision, and interview-style questions.

For the full detailed answers, see [DEVOPS.md](./DEVOPS.md).

## Overview

DevOps is a culture and practice that connects software development and IT operations. Its goal is to deliver software faster, with higher quality, better automation, and smoother collaboration between teams.

### Main goals of DevOps
- Automate repetitive tasks
- Improve software quality
- Speed up deployment and release cycles
- Reduce manual work and errors
- Enable continuous integration and delivery
- Improve system monitoring and reliability

### Core DevOps lifecycle

```text
Plan → Code → Build → Test → Deploy → Monitor → Improve
```

---

## 1. Azure Boards

Azure Boards is a project management and tracking service in Azure DevOps used to plan, organize, and monitor work in Agile teams.

### Key features
- Work items such as Epic, Feature, User Story, Task, Bug, and Issue
- Scrum and Kanban boards
- Backlogs and sprint planning
- Team collaboration and progress tracking
- Integration with GitHub and Azure Repos

### Example flow
A team creates a user story, breaks it into tasks, assigns ownership, and tracks progress from backlog to completion.

```text
Developer → Work item → Board → Sprint → Done
```

---

## 2. Jira

Jira is one of the most widely used issue and project tracking tools in Agile software development.

### Features
- Scrum and Kanban boards
- Backlog and sprint management
- Bug tracking
- Workflow customization
- Dashboards and reports

### Common usage
Teams use Jira to create issues, set priorities, assign developers, and monitor the status of bugs and features until they are resolved.

---

## 3. Trello

Trello is a lightweight board-based project management tool that uses cards and lists for task tracking.

### Structure
- Board = project
- List = stage or category
- Card = task

### Common features
- Drag-and-drop task movement
- Labels, due dates, and checklists
- Comments and attachments
- Easy collaboration for small teams

### Example
A project board could contain:
- To Do
- In Progress
- Review
- Done

---

## 4. Agile Work Items

Agile teams organize work using different types of work items.

| Work Item | Purpose | Example |
|---|---|---|
| Epic | Large initiative | Build online shopping platform |
| Feature | Major functionality | Payment processing |
| User Story | Requirement from user perspective | As a customer, I want to add items to my cart |
| Task | Specific action | Implement cart API |
| Bug | Defect in system | Checkout button fails on mobile |
| Issue | Risk, blocker, or question | Request API response clarification |

### Relationship
```text
Epic → Feature → User Story → Task
```

---

## 5. Agile Board Organization

Agile boards help teams visualize work and keep progress transparent.

### Typical board columns
- Backlog
- To Do
- In Progress
- Review
- Done

### Best practices
- Keep work items small and clear
- Define acceptance criteria
- Limit work in progress (WIP)
- Assign priority and owners
- Review progress in sprint meetings

---

## 6. Azure DevOps Dashboards

Azure DevOps dashboards show live project metrics, work status, and health indicators for a team.

### Typical dashboard data
- Open bugs
- Completion rate
- Build and release status
- Sprint progress
- Pipeline failures
- Test results

These dashboards help managers and developers quickly understand what is happening and where action is needed.

---

## 7. Azure Pipelines

Azure Pipelines is Azure DevOps' CI/CD service for automating build, test, and deployment.

### Main purpose
- Build source code automatically
- Run unit/integration tests
- Package artifacts
- Deploy to Azure, Kubernetes, or other targets

### Sample pipeline flow
```yaml
trigger:
- main

pool:
  vmImage: 'ubuntu-latest'

steps:
- script: echo "Hello Azure DevOps"
- script: dotnet build
- script: dotnet test
```

This ensures that every change pushed to the repo can be validated automatically.

---

## 8. Service Connections

A service connection is a secure link between Azure DevOps and external systems such as Azure, GitHub, Docker Hub, or Kubernetes.

### Why they matter
- Store credentials safely
- Allow automation to access external resources
- Prevent secrets from being hardcoded into scripts

### Example use
A pipeline deploys an application to Azure App Service through an Azure service connection.

---

## 9. GitOps

GitOps is a modern deployment model where Git acts as the single source of truth for the system's desired state.

### Main concept
- Application and infrastructure configuration are stored in Git
- Changes happen through pull requests and version control
- A controller automatically reconciles the cluster with the Git state

### Benefits
- Better traceability
- Simple rollback
- Consistent deployments
- Stronger automation and governance

```text
Git Repo → GitOps Controller → Kubernetes / Cloud Environment
```

---

## 10. DevOps Advantages and Challenges

### Advantages
- Faster software delivery
- Continuous integration and deployment
- Improved team collaboration
- Better quality through automated testing
- Reduced manual effort and operational errors
- Easier scaling and monitoring

### Challenges
- Requires training and skill development
- Initial setup may be expensive
- Toolchain integration can become complex
- Cultural change is often required

---

## 11. DevOps in Full-Stack Development

Full-stack development includes frontend, backend, database, APIs, and deployment tasks. DevOps supports all these layers together.

### Role of DevOps in full-stack projects
- Automates builds and deployments
- Manages version control
- Supports CI/CD pipelines
- Monitors production systems
- Improves release reliability

### Example stack
- Frontend: React
- Backend: Node.js, Java, or .NET
- Database: MySQL, PostgreSQL, or MongoDB
- DevOps: Git, Docker, Azure Pipelines, Kubernetes

---

## 12. Git vs GitHub vs Azure DevOps vs GitOps

| Tool/Concept | Purpose |
|---|---|
| Git | Version control system |
| GitHub | Cloud-based Git repository hosting and collaboration |
| Azure DevOps | End-to-end DevOps platform |
| GitOps | Git-driven deployment and infrastructure automation |

### Summary
- Git tracks code changes.
- GitHub hosts repositories and supports collaboration.
- Azure DevOps provides lifecycle management and deployment automation.
- GitOps manages infrastructure using Git as the source of truth.

---

## 13. Docker and Containers

Docker is a tool used to build, package, and run containers. A container is a lightweight runtime environment containing the application and all necessary dependencies.

### Why they matter in DevOps
- Consistent environments across development and production
- Faster deployment
- Easier scaling
- Reduced environment mismatch errors

### Example
```text
Application + Dependencies → Docker Container → Run Anywhere
```

---

## 14. DevOps Process and Architecture

### Typical DevOps workflow
```text
Plan → Code → Build → Test → Deploy → Monitor → Feedback → Improve
```

### Azure DevOps architecture
```text
Developer
   ↓
Git Repo / Azure Repos
   ↓
Azure Pipelines
   ↓
Build + Test + Package
   ↓
Deploy to Azure / Kubernetes / Cloud
   ↓
Monitoring and Feedback
```

### GitOps architecture
```text
Git Repository (Desired State)
   ↓
GitOps Controller / Agent
   ↓
Kubernetes / Cloud Cluster
   ↓
Running Application
   ↓
Continuous Reconciliation
```

---

## Quick Revision Summary

- Azure Boards: manages Agile work and project tracking.
- Jira: issue and sprint tracking tool.
- Trello: simple visual task management board.
- Agile work items: Epic, Feature, User Story, Task, Bug, Issue.
- Azure DevOps dashboards: visualize project health and progress.
- Azure Pipelines: automate build and deployment processes.
- Service connections: secure access to external services.
- GitOps: use Git as source of truth for deployment.
- Docker/containers: package apps for portable, consistent deployment.
- DevOps benefits: faster delivery, better quality, automation, collaboration.

This repository is intended as a practical DevOps study guide and quick reference for understanding the main tools and practices used in modern software delivery.
