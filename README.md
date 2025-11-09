Spanish Vocab Practice — Vercel deployment

This repository contains a single-file Spanish vocab practice web app (typing test) with per-chapter vocab, a password-protected admin panel to add vocab or import from Quizlet text, and persistence using localStorage.

Files added
- `index.html` — the single-file web app (open in browser or deploy to Vercel).
- `vercel.json` — simple Vercel config for static hosting.
- `package.json` — minimal manifest (optional for local dev with Vercel CLI).
- `.gitignore` — ignores typical files.
- `LICENSE` — MIT license.

Quick deploy to Vercel (recommended)
1. Create a GitHub repository and push these files.
2. Sign in to Vercel (https://vercel.com) and create a new Project → Import Git Repository → choose your repo.
3. Vercel will detect a static site and deploy automatically. If needed, set the Root to `/` and the build to `index.html` (the provided `vercel.json` should handle it).

Local testing
- You can open `index.html` directly in your browser for quick testing. Note: local file:// origin means the URL will be file-based; deploying to Vercel or serving via a simple static server is recommended for consistent behavior.
- Optional: install Vercel CLI and run `vercel dev` for local dev.

Admin / password
- Default admin password: `admin` (first-run). Use Admin → Change password to update.
- Password is stored in localStorage (base64-encoded). This is lightweight local protection only — not secure for shared/public threat models.

Backup / restore
- The app stores data in browser localStorage under key `svp_chapters_v1`. Consider exporting the site (or using the Admin export/backup flow if added later) to backup your vocab.

If you want I can:
- Add an Export / Import JSON backup UI to the Admin panel (recommended).
- Add per-item edit/delete UI in Admin.
- Set up a simple GitHub Actions workflow to auto-deploy to Vercel (not required; Vercel integrates directly).

