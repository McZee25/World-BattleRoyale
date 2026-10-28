# World BattleRoyale v1.7 — GitHub Pages

This is a single-file browser game. No build step, framework, or external library is required.

## Publish the game with GitHub Pages

1. Sign in to GitHub and create a **new repository** (for example, `world-battleroyale`).
2. Choose **Public** if you want the game page to be accessible to anyone.
3. Upload `index.html` and `.nojekyll` from this folder to the repository's root. You can upload the files directly, or extract this ZIP and upload the two files.
4. Open the repository's **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch **main** and folder **/(root)**, then press **Save**.
7. Wait for the Pages deployment to finish. The public game URL will look like:
   `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`

## Notes

- Open `index.html` through the published GitHub Pages URL to play in a browser.
- Progress and preferences use browser `localStorage`. They stay in that browser on that device; they do not automatically sync across devices.
- The game has no build process or required external libraries.
