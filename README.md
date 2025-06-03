![Markdown Lint Status](https://github.com/kyk-131/markdown_lint/actions/workflows/markdown-lint.yml/badge.svg)

![Random GIF](https://media.giphy.com/media/initial-placeholder/giphy.gif)






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
