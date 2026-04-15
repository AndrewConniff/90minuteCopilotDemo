
# GH-300 "Day in the Life" Developer Demo – C# Edition (Live Instructions)

This file contains the step-by-step technical instructions for delivering the GH-300 Copilot demo using C# and ASP.NET Core Minimal API in GitHub Codespaces. Each step is designed to be executed live. No narration or speaking scripts are included — only technical actions and Copilot prompts.

---

## Segment 1: Plan with Copilot Chat

- Open GitHub Codespace for your demo repo.
- Open Copilot Chat.
- Prompt:
  > Create a development plan for an ASP.NET Core 'Team Task Tracker' web app. Include work items for project setup, task list page, task creation form, in-memory storage, database migration, unit testing, and a second microservice.

- Prompt:
  > Create GitHub Issues for each of the work items you just listed.

---

## Segment 2: Scaffold Base Application

- Open Program.cs.
- Comment:

```csharp
  // Set up a minimal ASP.NET Core web application that listens on port 3000 and returns "Hello, World!" at the root URL.
````

- Accept Copilot suggestion.

- Run the app with:

    ```bash
    dotnet run
    ```

- Open the forwarded port to verify "Hello, World!" is displayed.

---

## Segment 3: Build Task List Page

- Define TaskItem model:

    ```csharp
    // Define a record to represent a task item with Id, Title, DueDate, IsDone.
    ```

- Create in-memory list of tasks.

- Comment:

    ```csharp
    // Map a GET endpoint "/tasks" that returns an HTML page showing all tasks in a styled table.
    ```

- Use Copilot Chat:
    > Improve the HTML table with CSS: add a border, cell padding, and alternating row colors.

- Run and verify /tasks page.

---

## Segment 4: Add Task Creation Form

- Use Copilot Chat:
    > Provide the HTML for a form that posts to /tasks with fields: Title (text), DueDate (date), and a submit button.

- Insert form into /tasks page.

- Comment:

    ```csharp
    // Map a POST endpoint "/tasks" to handle form submission: read form data, validate, add task, redirect to /tasks.
    ```

- Use Copilot Chat:
    > How to validate that Title is not empty and DueDate >= today?

- Run and test form submission.

---

## Segment 5: Integrate Persistent Storage

### SQLite

- Use Copilot Chat:
    > Refactor to use SQLite with Microsoft.Data.Sqlite. Create a Tasks table and update GET/POST endpoints to use the database.

- Install package:

    ```bash
    dotnet add package Microsoft.Data.Sqlite
    ```

- Run and verify persistence.

### PostgreSQL

- Create docker-compose.yml:

    ```yaml
    # Define a PostgreSQL service with POSTGRES_USER, POSTGRES_PASSWORD, POSTGRES_DB
    ```

- Use Copilot Chat:
    > Migrate from SQLite to PostgreSQL using Npgsql. Use async/await and update all database operations.

- Install package:

    ```bash
    dotnet add package Npgsql
    ```

- Run:

    ```bash
    docker-compose up -d
    dotnet run
    ```

- Verify PostgreSQL integration.

---

## Segment 6: Testing & Debugging

- Create test project if needed.

- Write test:

    ```csharp
    [Fact]
    public void AddingTask_IncreasesTaskCount() { ... }
    ```

- Run:

    ```bash
    dotnet test
    ```

- Introduce bug (e.g., comment out INSERT).

- Re-run test to fail.

- Use Copilot Chat:
    > Test failed with error X. What is the likely cause?

- Fix and re-run test.

---

## Segment 7: Copilot Agent Mode

- Open Copilot Chat in Agent Mode.

- Prompt:
    > Create a new ASP.NET Core Minimal API in 'QuotesService' folder that returns a random quote at GET /quote. Modify main app to fetch and display quote. Update Docker Compose.

- Run:

    ```bash
    docker-compose up --build
    ```

- Verify quote appears in main app.

---

## Segment 8: Extend with MCP (Optional)

- Use Copilot Chat:
    > Create a tool named 'getTaskStats' that queries the PostgreSQL database and returns total, completed, overdue task counts and completion percentage.

- Register MCP tool in VS Code.

- Test via Copilot Chat:
    > What are the current task statistics?

---

## Segment 9: Custom Copilot Agent (Optional)

- Create file: `TaskBot.agent.md`
- Define agent behavior and tools.
- Use Copilot Chat:
    > @TaskBot How many tasks are incomplete and past due?

---

## Segment 10: Pull Request & Wrap-Up

- Commit changes:

    ```bash
    git add .
    git commit -m "Final demo state"
    ```

- Create PR:

    ```bash
    gh pr create --fill
    ```

- Use Copilot Chat:
    > Summarize the changes in this pull request.

- Optionally:
    > Review these changes for potential issues.

---

End of live demo instructions.

```

Let me know if you'd like this as a downloadable .md file or if you'd like me to generate a version with embedded code snippets or links.
```
