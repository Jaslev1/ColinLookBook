# Colin Berger — Architecture & Interior Design

Portfolio lookbook site. Single-page, fully self-contained HTML with all images embedded.

## Deploy to Vercel

### Option A: Vercel CLI (fastest)

```bash
npm i -g vercel
cd colin-berger-site
vercel
```

Follow the prompts — accept defaults. Done. Vercel gives you a live URL immediately.

To assign a custom domain afterward:

```bash
vercel domains add colinberger.com
```

### Option B: Vercel Dashboard (no CLI)

1. Go to https://vercel.com/new
2. Click **"Import Git Repository"** — or if no repo yet, use **"Deploy from template"** then swap the file
3. Alternatively: drag the `colin-berger-site` folder directly onto the Vercel dashboard import screen
4. Leave all build settings blank (it's static HTML — no framework, no build command)
5. Click **Deploy**

### Option C: GitHub + Vercel (for ongoing updates)

```bash
cd colin-berger-site
git init
git add .
git commit -m "Initial lookbook deploy"
gh repo create colin-berger --public --push --source=.
```

Then connect the GitHub repo to Vercel via the dashboard. Every push to `main` auto-deploys.

## Files

- `index.html` — complete lookbook, all images embedded as base64 (no CDN needed)
- `vercel.json` — routing config
