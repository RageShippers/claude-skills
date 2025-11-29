---
description: Start active work on Linear task and track progress
---

# Linear Build and Implementation

I'll help you implement this Linear task.

**Steps I'll take:**

1. Fetch the task details using `mcp__linear-server__get_issue`
2. Update task status to "In Progress" if not already
3. Add a progress comment documenting:
   - Current work and implementation decisions
   - File paths and line numbers for code changes
   - Any blockers, discoveries, or scope changes
4. Check for linked issues or parent/child relationships
5. Get started on implementation

**Usage:**

- `/linear-build BUILD-123` - Start tracking work on a task
- `/linear-build BUILD-123 The authentication flow is now using JWT tokens instead of sessions. Modified src/auth/handler.ts:45-67` - With specific progress notes

**What to provide:**

- The Linear task ID (e.g., BUILD-123)
- Optional: specific progress notes, decisions, or file references

**What I'll document:**

- Files modified in this session (if working actively)
- Implementation approach and key decisions
- Any deviations from the original plan
- Blockers or discoveries that affect scope
- **IMPORTANT:** Do *NOT* update the linear task to any status after In Progress - this will be done automatically by the Github workflow

**Best practices:**

- Call this periodically during implementation, not just at the start
- Include file paths with line numbers when referencing specific changes
- Encourage the user to use `/linear-pr` to create after the implementation is reviewed
- Only add additional comments if there are significant changes or deviations from the original plan or if previous comments are older than 1 day

Let me know the task ID and I'll get started on implementation.
