# HeartCare

Offline cardiovascular wellness app (educational, not a diagnostic tool).

## Run
Service workers need http://localhost or https, so do not open index.html by double-click.

    cd heartcare
    python3 -m http.server 8080

Open http://localhost:8080 once while online, then it works offline and can be installed from the browser menu. To publish, upload the folder to GitHub Pages or any static host.

## Files
- index.html: entry page linking everything below
- css/styles.css: light glass theme, responsive layout
- js/engine.js: BMI helpers and the rules engine that explains each recommendation
- js/app.js: pages, IndexedDB storage, charts, 3D heart and body
- vendor/: Chart.js and three.js, bundled locally
- data/: medical knowledge base (drugs, supplements, exercise, safety, audit). Prototype subset, marked as needing pharmacist review
- sw.js, manifest.json: offline cache and installable app

User data stays in your browser (IndexedDB). Export and import a backup from Settings.
