
# GitHub Copilot Codespaces Demo – Day in the Life

## Goal

Demonstrate a realistic end-to-end developer workflow using GitHub Copilot in Codespaces, from planning through implementation and review.

---

## Demo Constraints

- Audience is experienced developers
- No intro or tour content
- Hands-on, narrative-driven demo
- Everything happens in GitHub Codespaces
- GitHub Copilot is used intentionally at every major step

---

## Phase 0 – Pre-Demo Setup

- Create a GitHub repository named `copilot-codespaces-demo`
- Branch: `main`
- Repository can be empty or contain only a README

README content:

```text

Scenario: Build a simple API used by internal teams to manage feature requests.

```

---

## Phase 1 – Planning (Day in the Life)

- Open GitHub Issues
- Create three issues to represent planned work

Use GitHub Copilot Chat to help draft them:

```text

We're building a simple ASP.NET Core Web API for managing feature requests.
Create 3 GitHub Issues:

1.  Project scaffolding
2.  Data model + in-memory storage
3.  CRUD API endpoints

```

---

## Phase 2 – Development Environment

- From the repository select:
  Code → Codespaces → Create Codespace on main
- Wait for Codespaces to finish initializing

---

## Phase 3 – Application Creation

- Open Copilot Chat in Codespaces
- Ask Copilot:

```text

Create a new ASP.NET Core Web API targeting .NET 8 using minimal APIs.
Explain what files will be created.

```

- Create the application:

```text

dotnet new webapi -n FeatureApi
cd FeatureApi

```

---

## Phase 4 – Code Understanding

- Open Program.cs
- Ask Copilot:

```text

Explain what this Program.cs file is doing in simple terms.

```

---

## Phase 5 – Feature Implementation

### Data Model

- Ask Copilot:

```text

Create a FeatureRequest model with:

- Id (int)
- Title (string)
- Description (string)
- Status (New, Active, Done)
    Use best practices.

```

### In-Memory Storage

- Ask Copilot:

```text

Add an in-memory collection to store FeatureRequest items.
Explain where it should live and why.

```

### API Endpoints

- Ask Copilot:

```text

Add minimal API endpoints for:

- GET all feature requests
- GET by id
- POST new feature request
- PUT update
- DELETE

```

- Optionally run the application:

```text

dotnet run

```

---

## Phase 6 – Iteration and Improvements

### Validation

- Ask Copilot:

```text

Add basic validation and return appropriate HTTP status codes.

```text
/ Logging

- Ask Copilot:

```

Add structured logging for create and update operations.

```text

---

## Phase 7 – Code Review

- Ask Copilot:

```

Review this code for:

- readability
- bugs
- API design issues
    Provide suggestions only.

---

## Wrap-Up

- Copilot was used for planning, learning, coding, and review
- The developer remained in control at all times
- The same workflow works locally or in Codespaces

- # Demo 2
- Yes — here is **one single, continuous Markdown file** where **every “ask Copilot” is replaced with an explicit prompt**.  
This is copy-once, paste-once, repo-ready.

***

```markdown
# GitHub Copilot Codespaces Demo – Day in the Life

## Goal
Demonstrate a realistic end-to-end developer workflow using GitHub Copilot in Codespaces, from planning through implementation and review.

---

## Demo Constraints
- Audience is experienced developers
- No intro or tour content
- Hands-on, narrative-driven demo
- Everything happens in GitHub Codespaces
- GitHub Copilot is used intentionally at every major step

---

## Phase 0 – Pre-Demo Setup
- Create a GitHub repository named `copilot-codespaces-demo`
- Branch: `main`
- Repository can be empty or contain only a README

README content:
```

Scenario: Build a simple API used by internal teams to manage feature requests.

```

---

## Phase 1 – Planning with Planner (Outline the Work)

### Step 1: Create a Plan
- Open Planner
- Create a new plan named:
  **Feature Request API – Initial Build**

### Step 2: Generate the Initial Work Outline
In Copilot Chat, enter the following prompt:
```

We are starting a brand new software project.

Context:

*   Technology: ASP.NET Core Web API
*   Runtime: .NET 8
*   Development environment: GitHub Codespaces
*   Goal: Build an internal API to manage feature requests

Task:
Outline all of the work required from initial setup through implementation and review.
Group the work into logical phases that a developer would naturally follow.
Do not write code yet.

```

### Step 3: Create Planner Tasks
Use the Copilot-generated outline to create Planner tasks such as:
- Project scaffolding
- Review generated project structure
- Create domain model
- Implement in-memory data storage
- Build CRUD API endpoints
- Add validation and error handling
- Add logging
- Review and refine code

---

## Phase 2 – Create Work Items from the Plan

- Open GitHub Issues
- Create issues that correspond to the Planner tasks

In Copilot Chat, use this prompt:
```

Based on the planning outline we created, generate GitHub Issue descriptions.

Requirements:

*   One issue per major task
*   Clear title and short description
*   Each issue should be scoped to a single responsibility
*   Do not include implementation details yet

```

---

## Phase 3 – Development Environment

- From the repository, select:
  Code → Codespaces → Create Codespace on main
- Wait for Codespaces to finish initializing

---

## Phase 4 – Application Creation

In Copilot Chat, enter:
```

We are ready to start coding.

Task:
Describe how to scaffold a new ASP.NET Core Web API targeting .NET 8 using minimal APIs.
Explain what files and folders will be created and their purpose.

```

Then create the application:
```

dotnet new webapi -n FeatureApi
cd FeatureApi

```

---

## Phase 5 – Code Understanding

- Open Program.cs

In Copilot Chat, enter:
```

Explain what this Program.cs file is doing.

Requirements:

*   Use simple, clear language
*   Assume the reader is an experienced developer new to this specific project
*   Describe how the application starts and how requests are handled

```

---

## Phase 6 – Feature Implementation

### Data Model
In Copilot Chat, enter:
```

Create a FeatureRequest domain model.

Requirements:

*   Properties:
    *   Id (int)
    *   Title (string)
    *   Description (string)
    *   Status (New, Active, Done)
*   Follow C# and .NET best practices
*   Keep the model simple and appropriate for an internal API

```

### In-Memory Storage
In Copilot Chat, enter:
```

Add an in-memory data store for FeatureRequest items.

Requirements:

*   Suitable for demo and development purposes
*   Explain where this should live in the project structure
*   Explain why this approach is appropriate for now

```

### API Endpoints
In Copilot Chat, enter:
```

Add minimal API endpoints for FeatureRequest management.

Endpoints:

*   GET all feature requests
*   GET a feature request by id
*   POST a new feature request
*   PUT to update an existing feature request
*   DELETE a feature request

Requirements:

*   Use clear route naming
*   Return appropriate HTTP status codes

```

Optionally run the application:
```

dotnet run

```

---

## Phase 7 – Iteration and Improvements

### Validation
In Copilot Chat, enter:
```

Improve the API by adding basic validation.

Requirements:

*   Validate required fields
*   Return appropriate HTTP status codes and messages
*   Keep the implementation simple and readable

```

### Logging
In Copilot Chat, enter:
```

Add structured logging to the API.

Requirements:

*   Log create and update operations
*   Use logging patterns that align with .NET best practices
*   Explain briefly why these log points are useful

```

---

## Phase 8 – Code Review

In Copilot Chat, enter:
```

Review the current codebase.

Focus areas:

*   Readability
*   Potential bugs or edge cases
*   API design concerns

Output:

*   Suggestions only
*   Do not rewrite the entire solution

```

---

## Wrap-Up

- Work started with planning before coding
- Planner was used to outline and organize the work
- Work items were created from the plan
- Copilot assisted with planning, learning, coding, and review
- The developer remained in control at all times
- The same workflow works locally or in GitHub Codespaces
```

***

If you want next, I can:

*   Tune the **prompts to sound more natural when spoken live**
*   Add **“what I say vs what I type”** separation
*   Create a **short executive version** that stops after planning + scaffolding

This is now **trainer‑grade and stage‑safe**.


# Agent Mode 

You are running in Agent mode inside a GitHub Codespace.

Goal:
Create a complete “Day in the Life” demo project from scratch for an enterprise developer audience. The demo must show realistic planning → work items → implementation → improvement → review.

Hard requirements:
- Everything happens inside this Codespace.
- Use .NET 8 and an ASP.NET Core Web API with minimal APIs.
- Create the application first (so Program.cs exists) before modifying it.
- Keep the implementation simple, readable, and reliable for a live demo.
- Prefer additive, incremental edits with clear commits or checkpoints.
- If you need to choose between speed and clarity, choose clarity.
- Do not introduce databases, auth, containers, or external services (keep it local + in-memory).

What to produce:
A) Repository structure and files:
   - Create a folder "FeatureApi" containing the .NET 8 minimal API project
   - Add a top-level README.md describing scenario, how to run, and endpoints
   - Add a top-level DEMO.md containing the full step-by-step demo instructions (Planner → issues → codespaces → build → improve → review)

B) Planning artifacts as markdown (since you cannot actually create Planner plans here):
   - Create /docs/PLAN.md that contains:
       1) A concise project outline (phases)
       2) A task list representing the Planner plan
   - Create /docs/ISSUES.md that contains:
       - GitHub Issue titles + descriptions that map to the plan (one per major task)

C) Application behavior:
   - Implement a FeatureRequest domain model:
       - Id (int)
       - Title (string)
       - Description (string)
       - Status (New, Active, Done)
   - Implement an in-memory store for FeatureRequest items
   - Implement endpoints:
       - GET /featurerequests
       - GET /featurerequests/{id}
       - POST /featurerequests
       - PUT /featurerequests/{id}
       - DELETE /featurerequests/{id}
   - Return appropriate HTTP status codes (200/201/204/400/404)
   - Add basic validation:
       - Title required, min length 3
       - Description optional but max length 1000
       - Status must be one of allowed values
   - Add structured logging for create and update operations

D) Execution:
   - Run dotnet restore/build/test (if tests exist)
   - Run the API to confirm it starts successfully
   - Provide a short “verification checklist” in README.md

E) Code review output:
   - Create /docs/REVIEW.md containing:
       - 8–12 bullets of suggested improvements (readability, edge cases, API design) without rewriting the entire app

Constraints:
- Keep everything deterministic; do not use placeholders.
- If you must make an assumption, write it down in /docs/ASSUMPTIONS.md.
- Do not ask me questions unless the task cannot proceed without a decision; if so, present one default decision and continue.

Now do the work end-to-end:
1) Scaffold the project
2) Generate the planning docs
3) Implement the API
4) Add validation + logging
5) Verify the app runs
6) Generate the demo docs (DEMO.md)
7) Generate the review doc
While you work, narrate briefly what you’re doing and why at each step.
