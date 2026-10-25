# In-Place Task Editing

## Overview
Task names can be edited directly in the list without removing and recreating the task.

## Description
- Clicking a task title replaces it with a focused text input containing the current name.
- Pressing Enter or leaving the input saves a non-empty trimmed name and persists the change through localStorage.
- Pressing Escape cancels the edit and leaves the previous name unchanged.
- Empty or whitespace-only edits are not saved; the task keeps its existing name.

## Verification
- Browser-tested editing a task title and confirmed the updated title rendered and persisted after reload.
- No JavaScript page errors were reported during the task-flow checks.
- Escape cancellation and empty-name handling were reviewed in the implementation but were not separately exercised in the browser.
