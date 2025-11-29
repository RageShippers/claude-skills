---
description: Create branch, commit, push, and open PR linked to Linear task
allowed-tools: Bash(git *)
---

# Linear PR Creation

I'll help you create a properly formatted branch, commit, and PR linked to your Linear task.

**Steps I'll take:**

1. Fetch the Linear task details to get the ID and title
2. Create a branch named `feature/TASK-ID-description` (e.g., `feature/BUILD-123-add-auth-flow`)
3. Stage and commit changes with Linear ID in commit message
4. Push branch with upstream tracking (`-u` flag)
5. Create GitHub PR with:
   - Title matching the Linear task
   - Description including "Closes BUILD-XXX" for automation
   - Link to the Linear task
6. Optionally add a completion comment to Linear (only if the last build comment is >1 day old)
7. **Do NOT** change the Linear task status - GitHub workflow handles this

**Usage:**

- `/linear-pr BUILD-123` - Create PR for task
- `/linear-pr BUILD-123 "Custom commit message"` - With custom commit message
- `/linear-pr BUILD-123 --comment` - Create Linear completion comment

**What to provide:**

- The Linear task ID (e.g., BUILD-123)
- Optional: custom commit message (defaults to task title)
- Optional: `--comment` flag to add a completion comment

**Before git workflow:**
- Ensure the lint has been run with `pnpm lint:fix`
- Ensure the typecheck is passing with `pnpm typecheck`
- Ensure the tests are passing with `pnpm test`

**Git workflow:**

- Branch name format: `feature/TASK-ID-kebab-case-description`
   - Follow git flow conventions (`feat`, `fix`, `docs`, `chore` etc.)
- Commit message format: `[TASK-ID] Description` or custom message with task ID
- PR description includes: `Closes TASK-ID` for GitHub automation
- Task status remains "In Progress" - GitHub Actions updates it on merge

**PR workflow:**

- PR title: Use a descriptive title that does NOT include the Linear task ID
- Include the task ID in the PR description (e.g., "Closes BUILD-123")
- Many tasks can be linked via comma separated list (e.g., "Closes BUILD-123, BUILD-456")

**Before running:**

- Ensure you're on the correct base branch (usually `main` or `develop`)
- Stage your changes with `git add`
- Pull latest changes if needed

Let me know the task ID and I'll create the PR via the workflow.
