# Error Handling

## Overview
The app handles invalid due dates, a failed remote logo image, and errors while loading tasks from localStorage. Each area has its own behavior below.

## Due-Date Validation
- `updateDueDateError()` checks for malformed input, dates before today, and dates after the configured maximum.
- The message appears inline in an alert region associated with the date input, and the input is marked `aria-invalid` while the value is invalid.
- `addTask()` refuses to create a task when the date input is invalid and invokes native browser validation. A blank due date remains valid because the field is optional.
- The browser's native date input rejects impossible calendar dates according to month lengths and leap-year rules.

## Logo Image Failure
- The main Rocket League logo uses the provided remote PNG and descriptive alt text.
- If the image emits an error, the image is hidden and the existing CSS shield/text placeholder is revealed.
- The small `RL` badge is separate and is unaffected by the image fallback.

## Task Loading Failure
- `loadTasks()` catches errors from accessing localStorage or parsing the saved JSON.
- On failure, it logs the error and returns an empty task array so the app can initialize.

## Known Limitation
- `saveTasks()` does not currently catch localStorage write errors, such as storage quota or browser storage being unavailable. This is not covered by the load-error handling above.

## Verification
- Browser-tested past-date and after-maximum messages, invalid-date task blocking, and clearing the message after selecting a valid date.
- Tested calendar month lengths and leap-year boundaries, including February 29 in 2028 and its rejection in 2100.
- Simulated the logo image error event and confirmed the placeholder appeared while the `RL` badge remained unchanged. A real offline/network-blocking test was not performed.
- Browser-tested task persistence and reload behavior; editor diagnostics reported no errors.
