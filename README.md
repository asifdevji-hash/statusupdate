# StatusUpdate

A self-contained time-tracking and task-management web app. Group work into **projects**, break projects into **tasks**, and track time per task with start/stop timers, per-session notes, and monthly rollups you can export to Excel.

Built by **Asif Devji Solutions**.

## Live app

If this repo is published with GitHub Pages, the app is available at:

```
https://<your-username>.github.io/<repo-name>/
```

You can also just download `index.html` and open it in any browser — it runs entirely on its own, no server or internet connection required.

## Features

- **Projects and tasks** — projects contain tasks; each has a Name, Requirements, rich-text Resources/Notes, and an auto-populated Created date.
- **Time tracking** — start/stop stopwatch on each task. Every tracking session records its date, start, end, duration, and notes. Resume tracking on a past session to add more time to it.
- **Editable logs** — session Date, Start, End, Duration, and Notes can all be edited after the fact.
- **Kanban boards** — Deferred / Triage / Open / Complete, with drag-and-drop, for both projects and tasks.
- **List views** — drag to reorder; sort by last-modified or a custom order.
- **Rollups** — a per-project time log and an all-projects time log, scoped by month (totals reset each month while history stays browsable).
- **Excel export** — export any month's time log to a `.xlsx` file.
- **Backup / restore** — Export downloads a full JSON backup; Import restores it.

## Important: where your data lives

**All data is stored locally in your own browser** (using `localStorage`). There is no server, no account, and no syncing.

This means:

- Each person who opens the app has their **own private, separate** data. Nothing is shared between visitors.
- Your data stays on your device and is never uploaded anywhere.
- Clearing your browser data, switching browsers, or using a different computer will **not** carry your data over — and can erase it.

**Because of this, back up regularly:** click **↓ Export** to download a JSON file and keep it somewhere safe (e.g. a cloud drive). Use **↑ Import** to restore. Treat the app as your working copy and your exports as the real archive.

## Publishing with GitHub Pages

1. Put `index.html` in the root of a **public** repository.
2. Go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**, select your `main` branch and the `/ (root)` folder, and save.
4. Wait a minute; your app will be live at the URL shown on that settings page.

To update the app later, replace `index.html` and the site redeploys automatically.

## Tech

Single HTML file with React bundled in (no build step, no external CDN dependencies). Excel export uses SheetJS, also bundled.

## License

MIT — see [LICENSE](LICENSE).
