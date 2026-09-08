# Coming Soon — Dummy Site

A static, no-build "coming soon" landing page (`index.html`), ready to deploy to Vercel.

## What's inside
- `index.html` — the whole site (HTML, CSS, and a small JS handler, no dependencies)
- `vercel.json` — clean URL settings for Vercel
- No build step, no `package.json`, no framework — plain static hosting

The email form is a dummy: it doesn't send anywhere yet. It just shows a "thanks" message in the browser. Swap the JS handler for a real request to Mailchimp, Resend, a Google Form, etc. when you're ready.

## Deploy to Vercel

### Option A — Vercel CLI (fastest)
1. Install the CLI if you don't have it:
   ```bash
   npm i -g vercel
   ```
2. From inside this folder, run:
   ```bash
   vercel
   ```
   Follow the prompts (log in / create account on first run, confirm project name, keep default settings — no build command needed).
3. For a production URL:
   ```bash
   vercel --prod
   ```

### Option B — GitHub + Vercel dashboard (no CLI)
1. Push this folder to a new GitHub repo:
   ```bash
   git init
   git add .
   git commit -m "Coming soon page"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. Go to [vercel.com](https://vercel.com) → **Add New… → Project**.
3. Import the GitHub repo you just pushed.
4. Framework preset: choose **Other** (or leave as detected — Vercel auto-detects a plain static site since there's no build config). Leave the build command and output directory blank.
5. Click **Deploy**. Vercel gives you a live URL in under a minute (e.g. `your-project.vercel.app`).

### Option C — Drag and drop (no git at all)
1. Go to [vercel.com/new](https://vercel.com/new).
2. Drag the `coming-soon-site` folder straight into the browser upload area.
3. Deploy — Vercel serves `index.html` as-is.

## Custom domain (optional)
In the Vercel project → **Settings → Domains**, add your domain and follow the DNS instructions Vercel shows you (usually one CNAME or A record at your registrar).

## Editing later
Everything lives in `index.html` — headline, copy, colors, and the form are all in that one file. Change the text, save, and redeploy (`vercel --prod`, or just push to `main` if you connected GitHub — Vercel redeploys automatically on every push).
