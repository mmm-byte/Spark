# Spark Repair Estimator

This is a mobile-first repair estimator built for Spark Homes. The app is meant for acquisition agents who walk properties in the field, check off repairs room by room, add photos, and export a clean estimate without relying on a backend.

The whole thing lives in a single HTML file so it can be opened, shared, and deployed easily. Data is stored locally in the browser, so it keeps working offline once the app shell is cached.

## What it includes

- Multiple projects with local persistence
- Room-based walkthrough flow for repairs
- 19 repair groups across the required sections
- Photo capture with optional serial number parsing
- Export to Excel and ZIP
- PWA manifest and service worker for offline use
- Price overrides and custom line items

## How to run it

Open `Main.html` in a browser. For the best PWA behavior, serve the folder with any simple static server so the service worker can register properly.

## Project files

- `Main.html` is the main app
- `manifest.json` defines the PWA settings
- `sw.js` handles offline caching
- `icon-192.png`, `icon-512.png`, and `apple-touch-icon.png` are the app icons

## Libraries

The app uses a few CDN-hosted libraries:

- Tailwind CSS
- SheetJS / `xlsx-js-style`
- JSZip
- Tesseract.js

## Notes

- Photos are compressed before being stored so the app stays usable on mobile.
- Everything is designed around a fast phone workflow, not a desktop admin tool.
- `Main copy.html` and `about.html` are extra files in the folder and are not the primary submission file.
