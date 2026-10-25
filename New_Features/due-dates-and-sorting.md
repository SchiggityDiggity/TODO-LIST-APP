# Due Dates and Sorting

## Overview
Tasks support optional, validated due dates shown beside task names, with a control to sort by the soonest due date.

## Description
- The date input uses local calendar dates and allows today through December 31 of the year 100 years ahead.
- The browser's native date control enforces real month lengths and leap years. Date input values are stored as ISO `YYYY-MM-DD` strings to avoid timezone shifts.
- Dated tasks display `Due: MM/DD/YYYY` beside the task title. Tasks without dates have no due label.
- Groups display the earliest member due date beside the group name, and show each member's own due date in the group list.
- The sort control offers `Manual` and `Due date (soonest first)`. Due-date sorting places dated tasks in ascending order, keeps equal-date tasks in their prior order, and places undated tasks last.
- Sorting uses a display copy and does not rewrite the task order saved in localStorage.

## Verification
- Confirmed the range bounds for the current date and that dates before today or after the maximum are invalid.
- Tested month boundaries and leap years: February 29 was accepted in 2028, rejected in 2027 and 2100; February 30/31 and April 31 were rejected.
- Verified inline due-date formatting, no label for undated tasks, and preservation/display of member dates in a group.
- Tested due-date sorting, stable ordering for ties, undated tasks last, switching back to Manual, and unchanged saved order.
- Invalid dates block task creation and show an inline error; a valid date clears the error. Browser tests passed without page errors.
