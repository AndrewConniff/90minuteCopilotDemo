
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
