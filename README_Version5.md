# Duke Energy Bill Pay — Repository Support Files

This directory holds support files you asked for to upload alongside your existing `index.html`.

Files included here
- `snippets/quick-pay-button.html` — small Quick Pay CTA snippet (replace the href with your real Quick Pay URL).
- `snippets/phone-cta.html` — phone CTA snippet (tel: link).
- `robots.txt` — basic crawler rules (edit domain & rules if needed).
- `sitemap.xml` — simple XML sitemap (replace DOMAIN placeholder with your production domain).

Before you push
1. Place your `index.html` in the repository root.
2. Replace placeholders:
   - DOMAIN in `sitemap.xml` (e.g. `https://dukebillpay.example.com`).
   - Quick Pay link in `snippets/quick-pay-button.html` (replace `YOUR_QUICK_PAY_URL`).
   - Phone number if different from `+1-877-218-4132` in the snippets.
3. Add any extra pages (privacy.html, terms.html, 404.html) to the repo and update `sitemap.xml` accordingly.
4. Test locally (open `index.html` in a browser or run a static server).

Quick local test (from repo root)
- With Node installed:
  npx http-server -c-1 .
- Or Python 3:
  python3 -m http.server 8080

Deploy
- Push to GitHub and enable GitHub Pages (if using), or deploy to a static host (Netlify, Vercel, S3+CloudFront).
- If using GitHub Pages with a custom domain, set `CNAME` and update `robots.txt`/`sitemap.xml` to match.

Snippets usage
- Include files from `snippets/` into templates or paste the HTML directly where needed.
- Example:
  - Quick-pay button: paste `snippets/quick-pay-button.html` into the top-of-page hero section.
  - Phone button: paste `snippets/phone-cta.html` wherever a click-to-call CTA is needed.

Notes & recommendations
- Replace placeholder domain and Quick Pay link before going live.
- Add a privacy policy and terms pages and include them in the sitemap.
- If you want automatic sitemap updates, ask and I can add a small script or GitHub Action to regenerate it.

If you want, I can also:
- Add GitHub Actions workflow to publish to GitHub Pages on push to `main`.
- Generate localized sitemaps for city pages.
- Add a small sitemap-generator script to auto-include new pages.