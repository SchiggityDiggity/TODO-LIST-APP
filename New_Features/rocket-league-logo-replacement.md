# Rocket League Logo Replacement

## Overview
The main placeholder logo was replaced with the Rocket League PNG while preserving the existing layout and small `RL` badge.

## Feature Details
- Image source: https://mb.cision.com/Public/18576/3153803/a3a14109ca17940d_org.png
- Updated `index.html` to place the accessible logo image inside the existing `.logo-design` container.
- Added `.rocket-league-logo` sizing with `object-fit: contain` so the image keeps its aspect ratio.
- Kept the existing shield and text as a hidden fallback that appears if the image fails to load.
- Left `.logo-mark`, task interactions, and localStorage behavior unchanged.

## Verification
- Confirmed the PNG loaded successfully; its natural dimensions were 1293 x 1690.
- Confirmed the image fits the existing 154 x 104 logo container without distortion at desktop and mobile viewport widths.
- Triggered the image error handler to confirm the placeholder fallback appears and the `RL` badge remains unchanged. This was a simulated error event, not a real offline test.
- Browser-tested adding, editing, completing, deleting, and reloading tasks; all passed, and the original saved task data was restored afterward.
- No new JavaScript page errors or editor diagnostics were reported.
