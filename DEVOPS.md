# DevOps Exam Answers

## 1. What is Azure Boards?

Azure Boards is a project management service in Azure DevOps used to plan, track, and manage work in Agile and DevOps projects.

### Features
- Work items such as Epic, Feature, User Story, Task, Bug, and Issue
- Scrum and Kanban boards
- Backlogs and sprints
- Team tracking and progress monitoring
- Integration with GitHub and Azure Repos

### Example
A team creates a User Story: “Login page should allow users to sign in.”
Then they divide it into tasks such as:
- Design UI
- Create backend API
- Write test cases
- Deploy the feature

### Simple flow
Developer → Work item → Board → Sprint → Done

---

## 2. What is Jira?

Jira is a popular project management and issue tracking tool used mainly for Agile software development.

### Features
- Scrum and Kanban boards
- Sprint planning
- Bug tracking
- Issue tracking
- Dashboards and reports
- Workflow customization

### Example
A bug: “Login button is not working” is created as an issue.
The team assigns it to a developer, sets priority, and tracks the fix until resolution.

### Use in DevOps
Jira helps teams manage software work efficiently and keeps the development process transparent.

---

## 3. What is Trello?

Trello is a simple visual management tool based on boards, lists, and cards.

### Main idea
- Board = project
- List = stage or category
- Card = task

### Features
- Drag-and-drop tasks
- Labels and due dates
- Checklists
- Comments and attachments
- Easy team collaboration

### Example
A board called “Website Redesign” can have lists:
- To Do
- In Progress
- Review
- Done

Each task is a card, and the team moves tasks from one list to another as work progresses.

### Advantage
Trello is simple, easy to learn, and useful for small teams or basic project workflows.

---

## 4. What are the different work items in Agile, such as Epic, Feature, User Story, Task, Bug, and Issue?

In Agile, work items represent the work that must be done.

| Work Item | Meaning | Example |
|---|---|---|
| Epic | Large body of work | “Create online shopping system” |
| Feature | Major functionality | “Payment feature” |
| User Story | Requirement from the user’s perspective | “As a customer, I want to add products to the cart” |
| Task | Specific action to be completed | “Develop cart API” |
| Bug | Defect or problem in the software | “Checkout button fails on mobile” |
| Issue | Problem, question, or risk | “Need clarification on API response format” |

### Relationship
Epic → Feature → User Story → Task

### Note
- Bugs usually describe problems in an existing system.
- Issues may include risks, blockers, or questions.

---

## 5. How do you organize work items on an Agile board?

Agile boards organize work according to the stage of progress.

### Typical columns
- Backlog
- To Do
- In Progress
- Review
- Done

### Steps to organize work
- Create work items
- Assign priority
- Add due dates or labels
- Assign them to team members
- Move them from left to right as work progresses
- Limit work in progress (WIP)

### Best practices
- Keep tasks small and clear
- Write descriptive titles
- Define acceptance criteria
- Review work in daily meetings or sprint planning

### Example
A project board may look like:

```text
Backlog → To Do → In Progress → Review → Done
```

This makes project status visible to everyone.

---

## 6. What are Azure DevOps dashboards?

Azure DevOps dashboards are visual pages that show project status and key metrics.

### Features
- Work item progress
- Build and release status
- Sprint reports
- Test results
- Burndown charts
- Pipeline health

### Why dashboards are important
They help managers and teams quickly understand:
- What is completed
- What is pending
- Where the project is delayed
- Which tasks need attention

### Example
A team dashboard may show:
- Number of open bugs
- Number of completed tasks this sprint
- Failed pipeline count
- Work completion trend

### Simple diagram
```text
Project Data → Azure DevOps Dashboard → Team Decision Making
```

---

## 7. What are Azure Pipelines, and how do you create a pipeline?

Azure Pipelines is a CI/CD service in Azure DevOps used to automate build, test, and deployment processes.

### Main purpose
- Build code automatically
- Run tests
- Package the application
- Deploy to a server or cloud

### Features
- YAML pipeline support
- Multi-stage pipelines
- Integration with GitHub and Azure Repos
- Deployment to Azure, Kubernetes, or other services

### Steps to create a pipeline
1. Open Azure DevOps
2. Go to Pipelines
3. Click New Pipeline
4. Select the repository
5. Choose YAML or classic pipeline
6. Write pipeline steps
7. Save and run the pipeline
8. Check logs and results

### Example YAML pipeline
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

This pipeline runs whenever code is pushed to the main branch.

---

## 8. What are service connections, and how do you connect Azure DevOps to external services?

A service connection is a secure link between Azure DevOps and external services such as Azure, GitHub, Docker Hub, Kubernetes, or a server.

### Purpose
- Safely store credentials
- Allow pipelines to access external systems
- Avoid hardcoding secrets in scripts

### Common examples
- Azure subscription connection
- GitHub connection
- Docker Hub connection
- Kubernetes cluster connection

### Steps to create a service connection
1. Open Azure DevOps project
2. Go to Project Settings
3. Select Service connections
4. Click New Service Connection
5. Choose the type of connection
6. Add login credentials or subscription details
7. Save it

### Example
A pipeline deploys an app to Azure App Service using an Azure service connection.

---

## 9. What is GitOps?

GitOps is a way to manage infrastructure and application deployment using Git as the single source of truth.

### Main idea
- Desired system state is written in Git
- Any changes are made through Git pull requests
- A controller automatically syncs the system to match Git

### Core principles
- Git is the source of truth
- Infrastructure is defined declaratively
- Changes are version-controlled
- Automation keeps the environment aligned with Git

### Example
A developer updates the Kubernetes deployment file in Git.
A GitOps controller sees the change and applies it to the cluster automatically.

### Simple flow
```text
Git Repo → GitOps Controller → Kubernetes/Cloud Environment
```

### Benefits
- Better control
- Easy rollback
- Clear audit history
- Consistent deployment

---

## 10. What are the advantages and disadvantages of DevOps?

DevOps combines development and operations to improve software delivery.

### Advantages
- Faster software delivery
- Continuous integration and deployment
- Better teamwork between teams
- Early detection of bugs
- Higher automation and efficiency
- Better system reliability
- Easier scaling and monitoring

### Disadvantages
- Requires training and skill development
- Initial setup cost can be high
- Complex tool integration
- Automation problems may affect deployment
- Requires team culture change

### Comparison table

| Aspect | Advantages | Disadvantages |
|---|---|---|
| Speed | Faster release cycles | Needs strong automation |
| Quality | Better testing and feedback | Setup and configuration may be complex |
| Collaboration | Better communication between teams | Requires cultural change |
| Cost | Reduces manual effort | Initial investment may be high |

### Conclusion
DevOps is highly useful, but it needs proper planning and team cooperation.

---

## 11. What is the role and importance of DevOps in full-stack development?

Full-stack development includes frontend, backend, database, APIs, and deployment work. DevOps helps manage all these layers together.

### Role of DevOps in full-stack
- Automates build and testing
- Manages version control
- Supports CI/CD pipelines
- Deploys frontend and backend applications
- Monitors apps in live environment
- Improves production stability

### Importance
- Reduces manual work
- Speeds up delivery
- Improves code quality
- Makes deployment safer and repeatable
- Helps maintain application health after release

### Example
A full-stack project may have:
- Frontend: React app
- Backend: Node.js or Java API
- Database: MySQL or MongoDB
- DevOps: Git, Docker, Jenkins/Azure Pipelines, Kubernetes

### Final point
DevOps connects all stages of software delivery in a full-stack project, making the system more efficient and reliable.

---

## 12. What is the difference between Azure DevOps, Git, GitHub, and GitOps?

| Term | Purpose | Main Use |
|---|---|---|
| Git | Version control system | Tracks changes in source code |
| GitHub | Cloud platform for Git repositories | Code hosting and collaboration |
| Azure DevOps | Complete DevOps platform | Planning, coding, CI/CD, deployment, testing |
| GitOps | Git-driven automation model | Manages infrastructure and deploys systems using Git |

### Basic differences
- Git is the technology used for code versioning.
- GitHub is a hosting service built on Git.
- Azure DevOps is a complete toolchain for development lifecycle management.
- GitOps is a deployment strategy based on Git.

### Example
- Developers write code in Git.
- They push it to GitHub or Azure Repos.
- Azure Pipelines builds and deploys it.
- GitOps keeps the cluster aligned with Git configuration.

### Simple diagram
```text
Git → GitHub/Azure Repos → Azure DevOps Pipelines → Deployment
Git → GitOps Controller → Kubernetes/Cloud
```

---

## 13. What is the difference between Docker and containers? How do they help in DevOps?

Docker is a tool used to create, manage, and run containers.
A container is a lightweight, portable package that includes the application and its dependencies.

### Difference
| Term | Meaning |
|---|---|
| Docker | Tool/platform used to build and run containers |
| Container | Isolated environment containing app + dependencies |

### Example
An application may need:
- Node.js
- Libraries
- Config files
- OS dependencies

Docker packages all of them into a container, so the application runs consistently everywhere.

### How they help in DevOps
- Same environment across dev, test, and production
- Faster deployment
- Easier scaling
- Less environment mismatch issues
- Better automation in CI/CD pipelines

### Benefits
- Lightweight compared to virtual machines
- Quick to start
- Portable and reusable
- Good for microservices and cloud deployment

### Simple flow
```text
Application + Dependencies → Docker Container → Run Anywhere
```

---

## 14. What is the DevOps process? How does it work, and what are the architectures of Azure DevOps and GitOps?

### DevOps process
DevOps is a continuous workflow that connects planning, coding, testing, deployment, and monitoring.

### Typical lifecycle
1. Plan
2. Code
3. Build
4. Test
5. Release
6. Deploy
7. Monitor
8. Improve

### How it works
- Developers write code and store it in Git
- A CI pipeline runs tests and builds the project
- Deployment pipeline publishes the app
- Monitoring tools track health and performance
- Feedback is used to improve the product

### Simple flow
```text
Plan → Code → Build → Test → Deploy → Monitor → Feedback → Improve
```

### Azure DevOps architecture
```text
Developer
   |
   v
Git Repo / Azure Repos
   |
   v
Azure Pipelines (CI/CD)
   |
   v
Build + Test + Package
   |
   v
Deploy to Azure / Kubernetes / Cloud
   |
   v
Monitoring and Feedback
```

### GitOps architecture
```text
Git Repository (Desired State)
   |
   v
GitOps Controller / Agent
   |
   v
Kubernetes / Cloud Cluster
   |
   v
Running Application
   |
   v
Continuous reconciliation with Git
```

### Key difference
- Azure DevOps focuses on end-to-end software lifecycle automation.
- GitOps focuses on managing infrastructure and deployment state using Git.

### Final Conclusion
DevOps helps teams deliver software quickly, reliably, and efficiently. Azure DevOps gives complete lifecycle management, while GitOps provides a modern Git-based way to manage deployments and infrastructure.

---

# Short Revision Summary

- Azure Boards: project tracking and Agile work management.
- Jira: issue and sprint tracking tool.
- Trello: simple board-based task management.
- Agile work items: Epic, Feature, User Story, Task, Bug, Issue.
- Agile board: organizes work by progress status.
- Azure DevOps dashboards: visual project status tracking.
- Azure Pipelines: automation for build, test, and deployment.
- Service connection: secure link to external services.
- GitOps: deployment using Git as source of truth.
- DevOps advantages: speed, collaboration, automation, quality.
- DevOps disadvantages: cost, complexity, training needs.
- DevOps in full-stack: manages all app layers together.
- Difference between Git, GitHub, Azure DevOps, and GitOps.
- Docker vs container: Docker is the tool; container is the runtime package.
- DevOps process: plan, code, build, test, deploy, monitor, improve.
