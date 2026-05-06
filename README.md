# GitHub Copilot + Spaces + Agent Workflow Demo

## Table of Contents
1. Create Repository
2. Start Codespaces
3. Create Copilot Space
4. Attach Repository to Space
5. Generate Application Plan
6. Let run and do VS Code Demo
7. Convert Plan to Issues
8. Create Issues
9. Create Project Board
10. Create Sprint Structure
11. Assign Issues to Sprints
12. Execute Issues with Copilot (Agent Mode)
13. Full Application Build Prompt (.NET Fluent UI)

---

## 1. Create Repository

1. Go to https://github.com  
2. Click **New repository**  
3. Configure:
   - **Name:** `webapp-demo`
   - ✅ Add README
   - ✅ Add .gitignore (.NET)
4. Click **Create repository**

---

## 2. Start Codespaces

1. Open the repository  
2. Click **Code → Codespaces**  
3. Click **Create Codespace**  
4. Wait for environment to load  

---

## 3. Create Copilot Space

1. Open **Copilot Chat**  
2. Navigate to **Spaces**  
3. Click **Create Space**  
4. Enter:
   - **Name:** `WebApp Planner + Builder`

---

## 4. Attach Repository to Space

1. Click **Add sources**
2. Select:
   - Repository (`webapp-demo`)
   - README.md

3. Add instructions:

```text
Act as a senior software architect and project manager.

Plan and build a full-stack web application.

Break work into:
- Epics
- Features
- User stories
- Tasks

Ensure issues are implementation-ready with clear acceptance criteria.

When generating code, produce complete working files.
```

4. Click **Save**

---

## 5. Generate Application Plan

Run:

```text
Plan a modern full-stack web application for a task management system.

Include:
- Architecture
- Tech stack
- Epics
- Features
- User stories
- Task breakdown
```

---

## 6. Convert Plan to Issues

Run:

```text
Convert this plan into GitHub issues.

For each issue include:
- Title
- Description
- Acceptance criteria
- Labels
- Dependencies

Format each issue so it can be pasted directly into GitHub.
```

---

## 7. Create Issues

1. Go to **Issues**
2. Click **New Issue**
3. Paste Copilot-generated issue content
4. Save each issue

---

## 8. Create Project Board

1. Go to **Projects**
2. Click **New Project**
3. Choose:
   - Board (Kanban) or Table
4. Click **Create**

---

## 9. Create Sprint Structure

1. Open Project
2. Add field:
   - **Name:** `Sprint`
3. Add values:
   - Sprint 1
   - Sprint 2
   - Sprint 3

---

## 10. Assign Issues to Sprints

Run:

```text
Assign all issues into 3 sprints based on dependencies and priority.
```

Then:

1. Assign sprint values manually in the Project

---

## 11. Execute Issues with Copilot (Agent Mode)

For each issue:

1. Open the issue  
2. In Codespaces, run:

```text
Implement this issue.

Generate all required files and code.
```

3. Review generated code  
4. Commit changes  
5. Close the issue  

---

## 12. Full Application Build Prompt (.NET Fluent UI)

Run in Codespaces or Copilot Agent Mode:

```text
Build a modern full-stack web application using .NET (ASP.NET Core) with a clean architecture.

APPLICATION OVERVIEW:
Create a Task Management web app with a modern Fluent UI experience.

FRONTEND:
- Razor Pages or Blazor Server
- Fluent UI design
- Responsive layout

UI:
- Sidebar with icons
- Header bar
- Dashboard cards

PAGES:
- Dashboard
- Task List
- Task Details
- Create Task

BACKEND:
- ASP.NET Core API
- CRUD endpoints

DATABASE:
- EF Core
- SQLite

MODEL:
- Id
- Title
- Description
- Status
- CreatedDate

FEATURES:
- CRUD Tasks
- Filters
- Validation

DESIGN:
- Fluent UI
- Icons
- Card layouts

DELIVERABLE:
- Full working solution
- All files
- Sample data

GOAL:
Complete runnable modern web app.
```

---
## Add Testrunner

## Copilot Prompt: Add Testing, Run Tests, and Document Code

You are working in an existing .NET (ASP.NET Core) web application.

### Goal
Add a complete testing solution, generate tests for the application, execute them, and improve code quality by adding clear comments.

---

### Tasks

#### 1. Add Test Project
- Create a new test project using:
  - xUnit (preferred) or MSTest
- Name it: `<solution-name>.Tests`
- Ensure it is part of the solution
- Add necessary NuGet packages for testing

---

#### 2. Generate Tests
Create comprehensive unit and integration tests for:

- Controllers
  - API endpoints (GET, POST, PUT, DELETE)
  - Status codes and responses
- Services
  - Business logic validation
- Data Layer
  - CRUD operations
- Edge Cases
  - Invalid inputs
  - Empty states

Each test should include:
- Arrange / Act / Assert structure
- Meaningful test names
- Assertions for correctness

---

#### 3. Add Test Data
- Create mock or seeded data
- Use in-memory database for testing where applicable

---

#### 4. Execute Tests
- Run all tests using the built-in .NET test runner
- Capture:
  - Passed tests
  - Failed tests
  - Execution summary

---

#### 5. Output Results
- Display test results clearly in the terminal
- Summarize:
  - Total tests
  - Passed
  - Failed
  - Any errors encountered

---

#### 6. Improve Code with Comments
Add comments to all code files:

- Controllers:
  - Describe endpoints and purpose
- Services:
  - Explain logic and flow
- Models:
  - Describe fields and data usage
- Startup/Program:
  - Explain configuration

Guidelines:
- Use concise, meaningful comments
- Avoid redundant explanations
- Focus on clarity and maintainability

---

### Deliverables
- Fully working test project
- All tests written and passing
- Codebase updated with clear comments
- Output showing test execution results

---

### Final Step
After completion:
- Confirm all tests pass
- Show test summary output
- Ensure solution builds successfully

## Copilot Prompt: Generate Application Architecture Map and Update README

You are working in an existing .NET web application.

### Goal
Create a clear architecture diagram of the application and add it to the README using Mermaid diagrams.

---

### Tasks

#### 1. Analyze Application Structure
Identify:
- Frontend (UI / Blazor / Razor)
- Controllers / API layer
- Services layer
- Data access layer
- Database

---

#### 2. Create Application Architecture Diagram

Generate a Mermaid diagram that shows:

- User → UI → Controllers → Services → Data Layer → Database
- Flow of requests between components
- Logical layering

Use this format:

```mermaid
flowchart TD
    User --> UI
    UI --> Controller
    Controller --> Service
    Service --> Data
    Data --> Database

Key application components
Relationships between modules
Frontend vs Backend separation
```
#### 3. Generate a second Mermaid diagram showing:

```mermaid
graph TD
    UI[Frontend UI]
    API[API Controllers]
    Services[Business Services]
    DB[(Database)]

    UI --> API
    API --> Services
    Services --> DB
 ```

## Workflow Summary

```


Repository → Codespaces → Space → Plan → Issues → Project → Sprints → Execution
```
