# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Git Operations

After every code change, commit and push to GitHub:

```powershell
git add <changed-files>
git commit -m "describe the change"
git push
```

- Always push to the remote after each commit — do not batch multiple changes before pushing.
- If the repository has no remote yet, set one up with `git remote add origin <url>` before pushing.
- Never force-push to `main`/`master` without explicit user approval.

## Deployment

- **Production URL:** `https://mi5chi5run-del.github.io/task-board/`
- Push to `main` triggers automatic deployment via GitHub Actions (`.github/workflows/deploy.yml`).
- `vite.config.js` sets `base: '/task-board/'` — required for GitHub Pages to resolve assets correctly.

## Tech Stack

| Layer | Technology |
| ----- | ---------- |
| UI framework | React 18 |
| Build tool | Vite 6 |
| Styling | Plain CSS (component-scoped `.css` files) |
| State persistence | `localStorage` |
| CI/CD | GitHub Actions |

## Naming Conventions

- **Components:** PascalCase ファイル名・関数名（例: `App.jsx`）
- **CSS files:** コンポーネントと同名（例: `App.css`）
- **State updater functions:** `addTask` / `toggleTask` / `deleteTask` のように動詞 + 対象の形
- **localStorage キー:** `'tasks'`（現状1種類）
