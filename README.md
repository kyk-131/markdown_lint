![Markdown Lint Status](https://github.com/kyk-131/markdown_lint/actions/workflows/markdown-lint.yml/badge.svg)

![Random GIF](https://i.pinimg.com/originals/54/84/8b/54848b2058ecb66d0fe033ed5a6c8669.gif)







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
