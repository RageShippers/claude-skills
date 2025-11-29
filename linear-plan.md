---
description: Prepare Linear task with implementation plan, estimates, and labels
---

# Linear Task Planning

I'll help you prepare this Linear task for implementation.

**Steps I'll take:**

1. Fetch the task details and recent comments to understand current requirements
2. Draft an implementation plan based on the task requirements
3. Present the plan in markdown for your review
4. Once approved, update the task description with the plan
5. Add appropriate labels if specified
6. Update estimates if provided

**Usage:**

- `/linear-plan BUILD-123` - Plan a specific task
- `/linear-plan BUILD-123 estimate:3` - Include time estimate
- `/linear-plan BUILD-123 labels:backend,api` - Add labels

**What to provide:**

- The Linear task ID (e.g., BUILD-123)
- Optional: time estimate in points or hours
- Optional: comma-separated labels to add

**What I'll ask you:**

- Review of the implementation plan before updating the task
- Confirmation of labels and estimates if not specified
- *IMPORTANT*: Confirm the plan with the user before updating the task
- Accepting the plan should only update the task description/state, not start implementation

**Best practices:**

- Don't include a pseudo title like "Implementation Plan for Linear task...", that's implied
- **DO NOT** attempt to move into implementation of the task until prompted
- Don't change the status of the task after the plan is drafted and reviewed
- Keep the existing content of the task description for record, but add new information above a horizontal rule (`---`)
    - Take care when editing the description to not lose existing content or formatting
- When available, include a highlight of the acceptance criteria in the main task description
- Always provide a link to the task in the summary of your implementation plan/task update
- The plan is only created to be reviewed, we will not implement until the user uses `/linear-build`

Let me know the task ID and any additional details you'd like to include.
