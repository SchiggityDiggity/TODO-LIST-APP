# Task Creation and Local Storage

## Overview
Tasks can be added through the task form, saved in browser localStorage, and restored when the app reloads.

## Description
- `addTask()` trims the task text and ignores an empty task name.
- Each new task is stored as an object with a unique ID, task text, optional `dueDate` in `YYYY-MM-DD` format, and completion state.
- The due-date input is optional. If provided, its validity is checked before the task is created; an invalid date blocks creation and displays an error.
- The date picker is constrained to today through December 31 of the year 100 years ahead.
- `saveTasks()` writes the task array under the `rocket-league-tasks` localStorage key. `loadTasks()` restores it when the page starts.
- After a successful add, both form fields are cleared and the task list is rendered again.

## Verification
- Browser-tested adding a task with a due date, confirming its ISO date was saved and survived a reload.
- Confirmed a date beyond the maximum prevented task creation, while a task without a due date was accepted.
- Confirmed invalid dates block adding and that localStorage task data could be restored after tests.
- Date boundary checks covered month lengths, leap year 2028, and the non-leap century year 2100.
- No page errors or editor diagnostics were reported during these checks.
