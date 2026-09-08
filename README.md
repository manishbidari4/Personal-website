# Manish Bidari — Personal Website

A single-page personal site — pure HTML/CSS/JS, no build step, no dependencies to install. Ready to deploy to Vercel as-is.

## Files in this project

```
ai-portfolio/
├── index.html      → the entire site (structure, styles, and scripts)
├── vercel.json     → tells Vercel this is a static site with clean URLs
├── .gitignore      → keeps local/Vercel junk out of git
└── README.md       → this file
```

That's genuinely all you need — `index.html` is self-contained, and Vercel auto-detects plain HTML projects with zero configuration required.

## 1. Preview locally

Just double-click `index.html`, or drag it into a browser tab. No server needed.

## 2. Deploy to Vercel

### Option A — Vercel CLI (fastest)
```bash
npm i -g vercel
cd ai-portfolio
vercel
```
Answer the prompts (set up a new project, accept the defaults — Vercel will detect "Other/Static"). When it finishes you'll get a live `https://your-project.vercel.app` URL.

To push future changes live:
```bash
vercel --prod
```

### Option B — GitHub + Vercel dashboard (recommended if you'll keep editing)
1. Create a new GitHub repository and push this folder to it:
   ```bash
   cd ai-portfolio
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. Go to [vercel.com](https://vercel.com) → **Add New... → Project** → import that repository.
3. Framework Preset: **Other** (no build command, no output directory needed).
4. Click **Deploy**.

Every future `git push` to `main` will auto-redeploy the site.

## 3. Custom domain (optional)

In the Vercel dashboard: **Project → Settings → Domains** → add your domain and follow the DNS instructions it gives you (usually a CNAME or A record at your registrar).

## 4. Personalizing further

All content lives directly in `index.html` — search for the section you want to change (`id="about"`, `id="skills"`, `id="experience"`, `id="projects"`, `id="education"`, `id="contact"`) and edit the text in place. Colors and fonts are defined once at the top of the `<style>` block under `:root` if you want to adjust the palette.
