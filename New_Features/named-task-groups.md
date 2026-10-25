# Named Task Groups

## Overview
Selected tasks can be combined into a named group while keeping their original task names and due dates visible as group members.

## Description
- `Group Tasks` is enabled when at least two tasks are selected.
- Selecting it opens a dialog that asks for a group name. The name is trimmed and must not be blank; canceling or submitting only whitespace leaves the selected tasks unchanged.
- Creating a group replaces the selected task rows with one group task using the entered title.
- The group shows the selected tasks as member entries. Member due dates are retained and displayed where present.
- The group inherits a due date from the earliest dated selected task and is marked complete only if every selected task was complete.
- Group changes are saved through the existing localStorage task array. Grouping a group flattens its members into the new group.

## Verification
- Browser-tested creating a named group and confirmed its title, member names, member due dates, and earliest group due date.
- Confirmed canceling the dialog and submitting a blank name do not alter the tasks.
- Confirmed the group flow completed without page errors; temporary browser test data was restored afterward.
