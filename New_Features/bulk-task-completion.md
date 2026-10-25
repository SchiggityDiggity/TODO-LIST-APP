# Bulk Task Completion

## Overview
The task board lets users select tasks and mark the selected tasks completed in one action.

## Description
- Each task row has a selection checkbox; selection state is tracked separately from completion state.
- `Mark Completed` is disabled when no tasks are selected or when every selected task is already complete.
- Activating the button marks every selected task completed, clears the selection, saves the updated task array to localStorage, and re-renders the list.
- Completed tasks are visually marked with the existing line-through and muted text styling.

## Verification
- Browser-tested selecting a task and marking it completed; the completed styling appeared.
- Existing task-flow checks also confirmed localStorage persistence and no new JavaScript page errors.
- The multi-task selection case was reviewed in the handler but was not separately exercised with multiple selected tasks in the browser.
