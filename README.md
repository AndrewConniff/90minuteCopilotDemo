# GitHub Copilot + Spaces + Agent Workflow Demo

## Table of Contents
1. Create Repository
2. Start Codespaces
3. Create Copilot Space
4. Attach Repository to Space
5. Generate Application Plan
6. Convert Plan to Issues
7. Create Issues
8. Create Project Board
9. Create Sprint Structure
10. Assign Issues to Sprints
11. Execute Issues with Copilot (Agent Mode)
12. Full Application Build Prompt (.NET Fluent UI)

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

## Workflow Summary

```
Repository → Codespaces → Space → Plan → Issues → Project → Sprints → Execution
```
