# Study Hours Tracker

A single-page, frontend-only app that tracks study hours against a personal goal. One circle per hour.

## Use it

Open `index.html` in any modern browser. No build step, no dependencies.

To install it as an app (works offline), host the folder on GitHub Pages or Netlify and use the browser's "Install" / "Add to Home Screen" option. The service worker only runs over http(s), so opening the file directly still works but without offline install.

## How it works

- Set a goal (1 to 10,000 hours) on first launch.
- **Start** begins a session, **Pause** freezes it, **Stop** adds it to your total.
- Elapsed time is computed from timestamps, so background tabs, sleep and reloads never lose time.
- Settings: change goal, add or subtract minutes, export/import a JSON backup, reset (type `RESET`).
- Keyboard: `Space` starts, pauses or resumes.

All data lives in `localStorage` under the key `studyTracker.v1`. Browsers can clear storage, so export a backup now and then (the app reminds you every 20 hours studied).

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app (HTML, CSS, JS) |
| `manifest.webmanifest`, `sw.js`, `icon.svg` | Optional PWA support |
