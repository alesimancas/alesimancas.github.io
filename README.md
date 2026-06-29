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

## Fonts

Hanken Grotesk ships under the SIL Open Font License. **Mov is a commercial
licence (Studio Feixen)** — check its EULA before redistributing the font file
in a public repository.
