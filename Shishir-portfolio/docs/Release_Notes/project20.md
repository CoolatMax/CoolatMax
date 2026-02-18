# Valkey Search 1.2.0 RC1 Release Documentation

### What was the purpose of the issue?


The project was transitioning from a specialized vector engine to a comprehensive search solution (Valkey Search). There was a critical need for a formal `RELEASE-NOTES.md` for the **v1.2.0 RC1** release to communicate major architectural shifts, new indexing capabilities, and performance optimizations to developers and stakeholders.

### How does the solution solve the issue?


I authored and verified the official release notes, ensuring that complex backend changes were accurately represented for end-users. The solution involved:

*   **Feature Documentation:** Detailed the implementation of **Full-Text Search (FTS)** including fuzzy matching and wildcard support, as well as new **Geospatial (R-tree)** indexing.
    
*   **Operational Guidance:** Documented the new `FT.AGGREGATE` command and its multi-stage pipeline (Filter, GroupBy, Apply), providing a roadmap for complex data analysis.
    
*   **Performance Metrics:** Highlighted a **30% reduction in memory usage** achieved through Radix Tree optimizations.
    
*   **Technical Validation:** Beyond writing, I validated the documentation by:
    
    *   Resolving environment-specific build issues (installing `ninja-build` and upgrading `pip`).
        
    *   Managing resource constraints by using restricted build flags (`--jobs=1`) to prevent Out of Memory (OOM) errors.
        
    *   Cross-referencing RFCs to ensure the schema accurately supported the documented field types.
        


### GitHub Link of Solution

**[PR #736: docs: add Release Notes for v1.2.0 RC1](https://github.com/valkey-io/valkey-search/pull/736)**