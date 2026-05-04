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
