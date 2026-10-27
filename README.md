# sagelab.in

Static website for Sage Lab. No build step.

- `index.html` home, about, apps, contact
- `privacy.html` privacy policy (use https://sagelab.in/privacy.html in Play Console)
- `terms.html` terms of use
- `CNAME` custom domain for GitHub Pages

## Deploy (GitHub Pages)
1. Settings → Pages → Source: Deploy from branch → `main` / root.
2. Custom domain: `sagelab.in`, then enable "Enforce HTTPS".
3. DNS at your registrar:
   - `A` records for `@`: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - `CNAME` for `www` → `<github-username>.github.io`
