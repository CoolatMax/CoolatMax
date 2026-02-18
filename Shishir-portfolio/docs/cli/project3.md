# Documentation & CLI Manpage Integration

### Purpose of Issue


The goal of this task ([#68](https://www.google.com/search?q=https://github.com/sp29174/GreenhousePython/issues/68)) was to bridge the gap between the application's functionality and user accessibility. Before this PR, the **GreenhousePython CLI** lacked formal system documentation, making it difficult for users to understand command structures, configuration requirements, and hardware control modules without diving directly into the source code.

### How the Solution Solves the Issue


I implemented a dual-format documentation strategy that ensures the project is both developer-friendly and Linux-compliant:

*   **System Integration:** Created a compiled **Roff-formatted manpage** (`greenhouse.1`), allowing users to access help directly via the standard Linux `man` command.
    
*   **Maintainability:** Provided a **Markdown source file** (`greenhouse.md`) to allow for easy future updates without requiring deep knowledge of Roff syntax.
    
*   **Technical Audit:** During development, I performed a deep dive into `main.py` to uncover and document "hidden" requirements that weren't previously clear:
    
    *   Identified mandatory keys for the `cfg.txt` configuration file.
        
    *   Mapped out the four primary control modules: **Camera, Water, Light, and Misc**.
        
    *   Clarified the underlying dependencies on **GTK4** and **Typer**.
        

### GitHub Link of Solution


*   **Pull Request:** [docs: add manpage in markdown and roff format #99](https://www.google.com/search?q=https://github.com/sp29174/GreenhousePython/pull/99)
    
*   **Contributed Files:**
    
    *   [`docs/man/greenhouse.md`](https://github.com/sp29174/GreenhousePython/blob/main/docs/man/greenhouse.md)
        
    *   [`docs/man/greenhouse.1`](https://github.com/sp29174/GreenhousePython/blob/main/docs/man/greenhouse.1)