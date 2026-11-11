# Bandung Family Trip Planner (React + Vite)

A premium, mobile-first React travel dashboard for the Bandung family trip, **22–27 November 2026** (2 adults + Melissa, age 4).

## Included

- Shared trip data across Overview, Itinerary, Travel, Budget, Packing, Ideas and Settings.
- Actual planning details: Scoot outbound (07:55–08:50), Garuda Indonesia return (18:45–21:45), Bobocabin Signature Sukawana (22–24 Nov), and voco Bandung Setiabudi (24–27 Nov).
- Editable flight information, Whoosh notes, accommodation details, driver estimates and day-by-day itinerary.
- Budget allocation, SGD/IDR converter, expense log and editable budget categories.
- Packing checklist, activity ideas and food ideas.
- Automatic local saving plus an explicit Save button, JSON export/import, undo/redo, light/dark/system theme and reset-to-original-plan.
- iPhone safe-area spacing and a PWA service worker for app-shell offline use after the first successful online visit.

## Run locally

Requires Node.js 20.19+ or 22.12+.

```bash
npm install
npm run dev
```

Open the local URL printed by Vite.

## Build

```bash
npm run build
npm run preview
```

The production site is generated in `dist/`.

## Deploy to GitHub Pages

1. Create a GitHub repository, for example `bandung-family-trip`.
2. Upload the **contents of this project folder** to the repository root (or push this folder using Git).
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, select **GitHub Actions**.
5. The project already includes `.github/workflows/deploy.yml`. Commit and push the project to the `main` branch.
6. In **Settings → Pages**, set the source to **GitHub Actions** if it is not selected already.
7. When the workflow finishes, the site will be available at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.
8. Open the URL in Safari on iPhone → Share → Add to Home Screen.

The deployment workflow is already included at `.github/workflows/deploy.yml`. It installs dependencies, builds the Vite app and publishes the `dist/` folder whenever you push to `main`. No manual workflow file creation is needed.

## Data, privacy and backups

- Trip edits are stored in local browser storage on the device and browser where you use the app.
- The app does **not** currently sync data between devices or store it in a cloud database.
- Use **Settings → Export backup** before changing devices, clearing Safari data or making major edits. Use Import backup to restore.
- The exchange rate is an editable estimate; the refresh action requests an indicative public rate when online. Verify the actual rate and card fees before spending.
- Flight, hotel, Whoosh, driver, opening-hour, child-fare and payment details should be checked against the providers before travel. Whoosh and driver arrangements are deliberately marked as not yet confirmed where appropriate.

## Project structure

```text
bandung-family-trip/
├── index.html
├── package.json
├── vite.config.js
├── public/
│   ├── icon-192.png
│   ├── icon-512.png
│   ├── manifest.webmanifest
│   └── sw.js
└── src/
    ├── App.jsx
    ├── main.jsx
    └── styles.css
```
