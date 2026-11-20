# Requirements

The CCG IIT Bombay website is a static site: one `index.html` plus the files in `assets/`. It has no build step and no package dependencies.

## To view or edit

- Any modern browser: Chrome, Edge, Firefox or Safari, from 2023 or later.
- Any text editor.
- Optional, for local preview over HTTP: Python 3. Run `python -m http.server 8000` in the project folder and open http://localhost:8000.

Opening `index.html` directly from disk also works.

## To deploy (Vercel)

- Node.js 18 or later, which provides `npx`.
- A Vercel account.
- The Vercel CLI, run through `npx`. You don't need to install it globally.

```
npx vercel login
npx vercel deploy --prod --yes
```

Hosting settings are in `vercel.json`: caching for `assets/` and security headers. `.vercelignore` keeps everything except the website out of the upload.

## Project files

| Path | What it is |
|---|---|
| `index.html` | The whole site: markup, styles, scripts and content data |
| `assets/` | Web-optimised images, logos and the self-hosted Schibsted Grotesk font |
| `vercel.json` | Vercel hosting configuration |
| `.vercelignore` | Files excluded from Vercel uploads |

## External services loaded at runtime

- Instagram profile embed (`instagram.com/ccg_iitb/embed`).
- Outbound links to Instagram, LinkedIn and Google Drive resources.
