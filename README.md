## 🧪 CI/CD Workflow Overview

```mermaid
sequenceDiagram
  participant Dev as Developer
  participant GitHub
  participant GitHubActions as GitHub Actions
  participant Linter as Markdown Linter

  Dev->>GitHub: Push .md change
  GitHub->>GitHubActions: Trigger markdown-lint.yml
  GitHubActions->>Linter: Run markdownlint
  Linter-->>GitHubActions: Success ✔ or Issues ❌
  GitHubActions-->>Dev: Report result in Actions tab
