# alejandra.tech — portfolio

Personal portfolio of Alejandra Chevey. Static **HTML + CSS** — no build step,
no JavaScript framework, no CMS. Served as static files (GitHub Pages or any
static host).

## Structure

- `index.html` — home (project grid)
- `about.html`, `contact.html`, `404.html`
- project pages: `paris-web.html`, `meet.html`, `mail.html`, `wallet.html`,
  `pass.html`, `web-summer-camp.html`
- `template.html` — reusable scaffold for a new project page (not linked)
- `css/base.css` — all styles, tokenized via `:root`
- `fonts/` — Hanken Grotesk (SIL OFL) + Mov variable (licensed)
- `assets/svg/` — project tile icons · `favicons/` · `images/`

The animated project tiles use the **Mov** variable font (Studio Feixen),
animated in pure CSS via `@keyframes` on `font-variation-settings` (no JS).
Motion is frozen under `prefers-reduced-motion`.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy / publishing changes

This repo **is** the live site. It's a GitHub Pages user site: the repo
`alesimancas/alesimancas.github.io` publishes from the `main` branch, and the
`CNAME` file points it at the custom domain **alejandra.tech** (HTTPS via
GitHub's managed certificate).

There's no build step — whatever HTML/CSS is on `main` is what goes live.
Publishing a change = commit and push to `main`; Pages rebuilds automatically,
usually within a minute or two:

```bash
git add -A
git commit -m "Describe the change"
git push origin main
```

Or in GitHub Desktop: review the change, commit to `main`, then **Push origin**.

Notes:

- Don't delete the `CNAME` file — it binds the site to alejandra.tech. Removing
  it drops the custom domain and can force GitHub to re-issue the SSL cert.
- If the live site ever stops updating, check the source under repo
  **Settings → Pages** (should be: Deploy from branch → `main`, root folder).

## Fonts

Hanken Grotesk ships under the SIL Open Font License. **Mov is a commercial
licence (Studio Feixen)** — check its EULA before redistributing the font file
in a public repository.
