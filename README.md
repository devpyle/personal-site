# personal-site — davidmyers.work

David Myers' personal website. A portable static site, no build step, no dependencies:

- `index.html` — single-page site (hero, about, experience, selected work, skills, education, contact)
- `resume.html` — print-optimized résumé (use the "Save as PDF" button)
- `styles.css` / `script.js` — design system and interactions

Fonts load from Google Fonts; everything else is self-contained.

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Hosting — Cloudflare Pages

The domain `davidmyers.work` is registered on Cloudflare, so DNS and SSL are automatic.

1. dash.cloudflare.com → Workers & Pages → Create → Pages → Connect to Git → pick `devpyle/personal-site`.
2. Build settings: framework preset **None**, build command **empty**, build output directory **`/`** (repo root).
3. Save and Deploy. You get a `*.pages.dev` URL to verify.
4. Custom domains → add `davidmyers.work` → Activate. Cloudflare creates the DNS record and certificate.

Every push to `main` redeploys automatically.
