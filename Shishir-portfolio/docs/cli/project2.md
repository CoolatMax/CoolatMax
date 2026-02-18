# Comprehensive CLI Reference & System Architecture Documentation

### Purpose of the Issue


The project was functioning primarily as a web service but lacked a standardized manual for terminal-based workflows. Developers faced several friction points:

*   **Discovery Gap:** No centralized guide for configuring, building, or managing the `envm` environment.
    
*   **Path Inconsistencies:** Discrepancies between the `Dockerfile` and the actual project entry point.
    
*   **Authentication Hurdles:** Frequent SASL authentication failures during local development due to undocumented default credentials.
    
*   **Hidden Workflows:** Difficulty in identifying the correct `goose` migration paths for database schema updates.
    

### How the Solution Solves the Issue


This PR introduced a comprehensive technical reference (`CLI_REFERENCE.md`) that bridges the gap between the source code and the developer experience.

*   **Corrected Build Paths:** Identified that while the Dockerfile pointed to `./cmd/envm`, the actual entry point was `./internal/cmd/main.go`. The documentation was updated to reflect the correct path, saving developers from "file not found" errors during manual builds.
    
*   **Schema & Migration Mapping:** Explicitly mapped the `goose` migration commands to the `internal/adapters/postgresql/schema/migrations` directory, ensuring database consistency.
    
*   **Security & Environment Onboarding:** Documented required `DATABASE_URI` credentials and provided the default `admin@123` credentials to bypass SASL authentication blockers.
    
*   **System Health Verification:** Standardized the verification process by documenting the `/health` endpoint and providing validated `curl` examples.
    
*   **Data Model Clarity:** Extracted a high-level overview of system entities (Users, Orgs, Projects, Variables) from the SQL schema to give new contributors an immediate mental model of the database.
    

### GitHub Link


*   **Pull Request:** [docs: finalize verified CLI reference with correct migration paths #325](https://github.com/envm-org/envm/pull/325)
    
*   **Repository:** `envm-org/main`