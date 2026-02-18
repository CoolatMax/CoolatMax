# CLI Documentation & UX Enhancement

## 🎯 Purpose of the Issue


The project (RIGS-844) lacked a centralized, user-facing reference for its Command Line Interface (CLI). Users and developers had to dive into the source code to understand available commands, leading to a high barrier to entry and potential misuse of subcommands like `bead`, `convoy`, and `tank`.

**The goal was twofold:**

1.  **Standardize Internal Help:** Improve the strings that appear when a user runs the `--help` flag.
    
2.  **Create External Reference:** Generate a comprehensive guide for the project's documentation site.
    

* * *

## 💡 How the Solution Solves the Issue


The solution involved a dual-layered approach to improve both the developer experience (DX) and the end-user documentation:

*   **Refined Help Strings:** Updated the internal metadata for all subcommands (Resource Management, Convey, Orchestration, etc.) within the Rust codebase. This ensures that `cargo run -- --help` provides immediate, accurate guidance.
    
*   **Comprehensive CLI Reference:** Authored a new reference guide that categorizes commands by function. This allows users to understand the hierarchy of the tool at a glance.
    
*   **Verification:** Validated all changes across the command tree to ensure consistency in flag naming and parameter descriptions.
    

### Command Hierarchy Overview


The following core modules were documented and improved:

*   **Global Commands:** `init`, `status`
    
*   **Resource Management:** `bead`
    
*   **Conveyance:** `convoy`
    
*   **Orchestration Providers:** `foreman`, `goal`, `provider`, `tank`
    

* * *

## 🔗 Solution Links


*   **Pull Request:** [docs: create initial CLI reference for RIGS-844 #174](https://github.com/Fnux8890/main/pull/174)
    
*   **Repository:** [Fnux8890/main](https://github.com/Fnux8890/main)
    
*   **Related Issue:** Closes #171