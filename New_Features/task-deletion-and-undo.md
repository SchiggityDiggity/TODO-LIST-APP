# Task Deletion and Undo

## Overview
Tasks can be removed individually, in bulk, or all at once, with a one-level Undo action to restore the most recent deletion.

## Description
- Each task has an individual delete button.
- `Delete Selected` removes all selected tasks; the action is disabled when nothing is selected.
- `Clear All Tasks` asks for confirmation before removing all tasks.
- All three deletion paths use the shared deletion handler, which keeps the removed task records and their original ordering for Undo.
- `Undo Delete` restores the most recently deleted tasks in their prior relative positions and persists the restored task array to localStorage.
- Undo is one-level, is available only for the current page session, and is replaced by a later deletion. It is not persisted across a page reload.

## Verification
- Browser-tested individual deletion and Undo restoration.
- Browser-tested Delete Selected, Clear All confirmation, and Undo restoration for both paths.
- Confirmed deletion and restoration update the task list and persist through localStorage; temporary test data was removed afterward.
- No JavaScript page errors were reported during the deletion tests.
