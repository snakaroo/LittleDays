# Little Days

A gentle habit tracker, focus timer, and decorated diary prototype for mobile and desktop.

## Files

- `dist/index.html` — app shell
- `dist/style.css` — responsive themes and layout
- `dist/app.js` — habit tracking, timer, diary, stamps, settings, and backup export
- `dist/sw.js` — offline service worker
- `dist/manifest.webmanifest` — installable web app manifest
- `dist/icon.svg`, `dist/icon-192.png`, `dist/icon-512.png` — app icons

No package installation or build step is required.

## Upload to GitHub

1. Extract this ZIP.
2. Open your GitHub repository and choose **Add file → Upload files**.
3. Upload the `dist` folder, this README, and `.gitignore` to the repository root. Keep the folder structure intact.
4. Commit the changes. Upload the extracted contents, not just the ZIP.

## Run locally

With Python 3 installed, run this from the repository folder:

```sh
python3 -m http.server 8000 --directory dist
```

Open http://localhost:8000. Use a local server rather than opening index.html directly so offline support can work.

## Hosting

Deploy `dist` as the static site directory. HTTPS is required for installation and service workers outside localhost.

For GitHub Pages without a build workflow, copy the contents of `dist` into a `docs` folder in your repository. In **Settings → Pages**, choose **Deploy from a branch**, then your branch and `/docs`. Alternatively, configure a GitHub Actions Pages workflow that uploads `dist` as its artifact.

## Prototype limitations

- Entries are stored in browser localStorage on the current device. This ZIP contains app source, not your personal diary data. Use the app's **Make it yours → Export backup** option for that data.
- Account creation, cloud backup, cross-device sync, and conflict resolution are not implemented.
- Artwork and stamps are starter placeholders. Stamps currently use system emoji, so their appearance can vary by device.
- Google Fonts requires an internet connection; fallback fonts are provided.
- Timers calculate elapsed time when the app is reopened. Background alerts are not guaranteed.

Sites hosting configuration, Git history, credentials, and personal diary data are excluded from this export.
