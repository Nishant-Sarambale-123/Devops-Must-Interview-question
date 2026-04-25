### **Interview‑Style Answer: How do you integrate basic static code analysis into CI?**

I integrate basic static code analysis into CI by making it an **automated quality gate** that runs on every code commit or pull request.

In practice, I add a static code analysis step early in the CI pipeline—right after the build or before unit tests. Tools like SonarQube, ESLint, Checkstyle, or Bandit are configured to scan the codebase for issues such as code smells, security vulnerabilities, and coding standard violations. The CI pipeline captures the analysis results and **fails the build if predefined thresholds are not met**, like critical issues or minimum code quality scores.

This ensures developers get **fast feedback** during development and issues are caught early, without requiring manual reviews for basic quality checks.

**Example:**  
In a CI pipeline, every pull request triggers a build followed by a SonarQube scan. If the scan detects new critical issues or fails the quality gate, the pipeline stops and the pull request cannot be merged. Only code that meets the quality standards moves forward.

**One‑line summary:**

> *Static code analysis is integrated into CI by automating scans on every commit and enforcing quality gates that prevent poor‑quality or insecure code from progressing.*
