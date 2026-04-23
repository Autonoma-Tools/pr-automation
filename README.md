# PR Automation: The Complete 7-Layer Stack for GitHub Actions

Companion code for the Autonoma blog post 'PR Automation: The Complete 7-Layer Stack for GitHub Actions'.

> Companion code for the Autonoma blog post: **[PR Automation: The Complete 7-Layer Stack for GitHub Actions](https://getautonoma.com/blog/pr-automation)**

## Requirements

Node.js >=20, npm, a GitHub repo with branch protection configured on your default branch, and the following GitHub Actions secrets: VERCEL_TOKEN, AUTONOMA_API_KEY, CHROMATIC_PROJECT_TOKEN, GITHUB_TOKEN (provided automatically).

## Quickstart

```bash
git clone https://github.com/Autonoma-Tools/pr-automation.git
cd pr-automation
Copy the files into the matching paths in your Next.js/React project, install the listed devDependencies (eslint, typescript, vitest, @eslint/js, eslint-plugin-react), add your Vercel, Autonoma, and Chromatic tokens as GitHub Actions secrets, and open a pull request. The 7-layer stack runs automatically on every PR.
```

## Project structure

```
.
├── .github/
│   └── workflows/
│       ├── autonoma-e2e.yml
│       └── pr.yml
├── eslint.config.js
├── LICENSE
├── package.json
└── README.md
```

- `.github/workflows/` — the GitHub Actions workflows that implement the 7-layer PR stack.
- `package.json` — minimal scripts (lint, type-check, test) that the workflows invoke.
- `eslint.config.js` — flat-config ESLint setup referenced by the lint layer.

## About

This repository is maintained by [Autonoma](https://getautonoma.com) as reference material for the linked blog post. Autonoma builds autonomous AI agents that plan, execute, and maintain end-to-end tests directly from your codebase.

If something here is wrong, out of date, or unclear, please [open an issue](https://github.com/Autonoma-Tools/pr-automation/issues/new).

## License

Released under the [MIT License](./LICENSE) © 2026 Autonoma Labs.
