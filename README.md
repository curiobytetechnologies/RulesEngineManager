# RulesEngineManager

A .NET-based frontend and backend application for managing environment-specific rule files, stored locally and on GitHub, with the option to upload to Snowflake (overwriting existing content).

## Features

- Manage rules, actions, and conditions (CRUD UI)
- Support for multiple environments (per environment rule file)
- Save rules locally and push to GitHub
- Upload/overwrite rules in Snowflake after confirmation

## Tech Stack

- ASP.NET Core Blazor Server (frontend + backend)
- C# models/services for business logic
- Snowflake .NET Connector (for uploading)
- Local JSON for storage, GitHub API for remote storage

## Getting Started

1. **Clone the repo:**  
   `git clone https://github.com/curiobytetechnologies/RulesEngineManager.git`
2. **Setup local environment:**  
   - .NET 8 SDK
   - [Snowflake .NET Connector](https://docs.snowflake.com/en/developer-guide/dotnet)
   - Update GitHub/Snowflake credentials in `appsettings.json`
3. **Run the project:**  
   - `dotnet run --project RulesEngineManager.Server`

## Directory Structure

```
RulesEngineManager/
├── RulesEngineManager.Server/
├── RulesEngineManager.Client/
├── RuleFiles/
└── README.md
```

## Configuration

Edit `appsettings.json` with your local paths, GitHub repo info, and Snowflake connection string.

## Notes

- For now, authentication is disabled.
- Snowflake upload will overwrite the target table.
