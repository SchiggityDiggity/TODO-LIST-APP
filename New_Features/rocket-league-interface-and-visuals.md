# Rocket League Interface and Visuals

## Overview
The task board uses a Rocket League-inspired visual theme with car illustrations, competitive rank badges, a live clock, and a full-viewport green code backdrop.

## Description
- The `.hero` section in `index.html` presents the Rocket League Task Board title, the unchanged `RL` badge, the clock, logo, cars, and ranks.
- `.car-design-row` renders CSS illustrations for the Fennec, Dominus, and Octane cars.
- `.rank-row` displays Bronze through SSL rank badges with distinct colors.
- `updateClock()` updates the 12-hour clock every second.
- `.code-backdrop` and `renderCodeBackdrop()` create green rows of binary and code text around the app, resize them with the viewport, and keep them behind the main panel.

## Verification
- Checked the code backdrop at desktop (1440 x 900) and mobile (390 x 844); generated rows covered the viewport and included binary, `print()`, and `str()` examples.
- Inspected the rendered app in the browser; title, clock, car designs, and rank badges appeared in the page.
- The logo image was verified separately in `rocket-league-logo-replacement.md`.
- No separate behavior test was needed for the decorative car and rank elements; the clock was observed rendering, but its one-second update was not independently timed in a test.
