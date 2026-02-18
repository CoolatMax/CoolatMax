# Project: SDK Error Handling Documentation

### Purpose of the Issue

The primary goal of this update was to bridge the information gap regarding how the SDK manages failures. Specifically, the project lacked clear guidance on:

*   **Custom Exceptions:** Identifying the specific errors raised by the library (e.g., `GPTClientInitializationError`).
    
*   **Retry Logic:** Explaining the internal `retry_with_backoff` mechanism so users understand how the SDK handles transient network issues.
    
*   **Leaky Abstractions:** Clarifying that while the SDK provides custom errors, it also allows native provider exceptions (like OpenAI’s `RateLimitError`) to propagate through, requiring users to handle both.
    

### How the Solution Solves the Issue

The solution provides a comprehensive "User Guide" section that serves as a safety manual for developers integrating the SDK.

*   **Centralized Reference:** Created `docs/user-guide/error-handling.md`, which explicitly lists triggers for `RemediationError`, `ValueError`, and initialization failures.
    
*   **Implementation Examples:** Added code snippets showing a "dual-layer" catch approach—handling both the SDK's custom exceptions and the underlying LLM provider's native errors.
    
*   **Logic Transparency:** Documented the `utils.py` backoff strategy to set expectations on execution time and automatic recovery attempts.
    
*   **Navigation Integration:** Updated `mkdocs.yml` to ensure the new documentation is easily discoverable within the project's web-based manual.
    

### GitHub Link

*   **Repository:** `netdevops/main`
    
*   **Pull Request:** [docs: error handling & expected exceptions and how to handle them #25](https://github.com/netdevops/hier-config-gpt/pull/29)