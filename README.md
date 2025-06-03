![Markdown Lint Status](https://github.com/kyk-131/markdown_lint/actions/workflows/markdown-lint.yml/badge.svg)

![Random GIF](https://preview.redd.it/togame-gifs-v0-xo9jcufaibxd1.gif?width=540![Random GIF](https://media.giphy.com/media/initial-placeholder/giphy.gif)auto=webp![Random GIF](https://media.giphy.com/media/initial-placeholder/giphy.gif)s=c76794cae48a5d167d0c7f7a098ba050bb57ae90)






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
