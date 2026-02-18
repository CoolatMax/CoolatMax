## Documentation: CLI Help Text & Usage Examples

## Purpose of Issue


The primary goal was to address **Issue #1**, which identified a lack of clarity in the Command Line Interface (CLI) internal documentation. Prior to this update, users lacked a structured way to understand:

*   Which mathematical operations were supported.
    
*   How to utilize environment-based configuration flags (e.g., precision and verbosity).
    
*   How to format commands correctly to avoid syntax errors.
    

### The Solution


The solution involved a significant overhaul of the `print_usage()` function within the core application. By restructuring the terminal output, the CLI now provides an intuitive, scannable interface.

**Key enhancements include:**

*   **Structured UI:** Implemented visual separators and categorized sections (Operations, Flags, Examples) to improve readability in a terminal environment.
    
*   **Flag Clarification:** Detailed the purpose of environment variables such as `CALC_PRECISION`, `CALC_VERBOSE`, and `CALC_INPUT`.
    
*   **Onboarding Examples:** Added three concrete usage scenarios—ranging from basic math to high-precision division—to reduce the learning curve for new users.
    
*   **Verified Output:** Conducted a Proof of Concept (PoC) by triggering the help menu via empty arguments to ensure the UI rendered correctly across different terminal widths.
    

### Link to Solution


*   **GitHub Pull Request:** [docs: clarify CLI help text and add usage examples #12](https://github.com/isha-1686/gitGoingFOSSRepo/pull/12)
    
*   **Contributor:** [CoolatMax](https://github.com/CoolatMax)