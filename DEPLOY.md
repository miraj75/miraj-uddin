# Deploy Checklist — miraj-uddin.eu + GitHub

You asked: is it ready for GitHub + your domain? **Yes — 100% ready.** Just push.

## Files ready in this folder
- `index.html` — whole site (fullscreen hero portrait, bold MIRAJ UDDIN animation, working contact → Mirajuddinxlx@gmail.com)
- `404.html` — copy for GitHub SPA routing
- `.nojekyll` — tells GitHub to serve as-is
- `CNAME` — contains `miraj-uddin.eu` (change to your real domain if different — one line)
- `sitemap.xml` + `robots.txt`
- `.github/workflows/deploy.yml` — auto-deploy on every `git push`

## Push now (copy-paste)
Replace `YOUR_USERNAME`:
```bash
git init
git add .
git commit -m "launch"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/miraj-uddin.git
git push -u origin main
```
Then: GitHub → Settings → Pages → Source: **GitHub Actions** → your site builds automatically.

Or if you use Branch mode: Settings → Pages → Source: Deploy from branch → main / root.

## Domain
- If your domain is NOT `miraj-uddin.eu`, edit `CNAME` file to `yourdomain.com` and push again.
- DNS: A → 185.199.108.153 / 109.153 / 110.153 / 111.153 ; CNAME www → YOUR_USERNAME.github.io
- After DNS propagates, GitHub → Pages → Custom domain → Enforce HTTPS.

## After deploy — test
1. Visit https://yourdomain.com → you should see fullscreen portrait hero with MIRAJ UDDIN bold letters animating
2. Contact → send test → check Mirajuddinxlx@gmail.com → click FormSubmit confirm → done

Need me to push for you? Give me repo URL and I’ll do it.
