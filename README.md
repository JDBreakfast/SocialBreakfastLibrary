# Social Breakfast — Deployment & Usage

## Deploy on GitHub Pages (free)
1. Create a new public GitHub repository (e.g. `social-breakfast`).
2. Add the following files at the repository root: `index.html`, `videos.json`, `README.md`.
3. Commit and push to the `main` (or `master`) branch.
4. In the repository Settings -> Pages, set the source to the `main` branch (root). GitHub will provide a URL like `https://yourusername.github.io/social-breakfast/`.

## Updating the gallery
- To add new Instagram posts, edit `videos.json` and append new Instagram post URLs (one per array item). Commit and push the change. GitHub Pages will serve the updated file immediately.
- The site also attempts to auto-refresh every 60s; otherwise reload the page in the browser.

## Notes & troubleshooting
- Instagram embed rendering is done via Instagram's official embed script (`https://www.instagram.com/embed.js`). If Instagram changes their embed policy or requires login for certain content, some posts may not display.
- If posts don’t show, check the browser console for errors (e.g. CORS, blocked content, or embed errors).
- For local testing without a server, some browsers block `fetch('videos.json')` due to file:// restrictions. Use a simple static server (e.g. `npx http-server` or `python -m http.server`) or push to GitHub Pages.
