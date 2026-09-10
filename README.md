# Miraj Uddin — From Bangladesh to Europe
Single-page personal website + hidden editor (same page).  
`index.html` only — no build step.

## ✨ Features
- Public mode: premium editorial single-page (Home, About, Journey, Education, Travel, Stories, Guide, Memories, Gallery, Contact)
- Hidden admin: `type "miraj"` or `5× click MU` or `Ctrl+Shift+M` or `#miraj-admin` → login `miraj / Miraj2025!` → same page becomes editor (no /admin)
- Data: Country → City → Trips → Photos (multiple trips per city, captions, bulk upload)
- Contact form: FormSubmit → **Mirajuddinxlx@gmail.com** + local Inbox (admin only)
- Fullscreen hero with your portrait covering whole first page, bold animated `MIRAJ UDDIN`

## 🚀 Deploy to GitHub Pages (2 min)

### 1) Create repo
1. Go to https://github.com/new → Name: `miraj-uddin` (or `yourname.github.io` for personal site)
2. Create (Public)
3. In this workspace, run:

```bash
git init
git add index.html sitemap.xml robots.txt .nojekyll README.md
git commit -m "launch: Miraj single-page site"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/<REPO>.git
git push -u origin main
```

### 2) Enable Pages
- Repo → Settings → Pages → **Build and deployment → Source: Deploy from a branch → Branch: main / root** → Save
- Your site will be at `https://<YOUR_USERNAME>.github.io/<REPO>/`

For `username.github.io` repo it’s `https://<YOUR_USERNAME>.github.io/`

### 3) Custom domain (your domain)
1. In your domain registrar (Namecheap / GoDaddy / Cloudflare) add DNS:
   - **A records** → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - **CNAME** → `www` → `<YOUR_USERNAME>.github.io`
2. In this repo, set `CNAME` file content to your domain, e.g. `mirajuddin.eu` or `www.mirajuddin.eu` (one line, no https)
3. Commit `CNAME`
4. Repo → Settings → Pages → Custom domain → enter `yourdomain.com` → Save → Enforce HTTPS (wait 5-30 min)

> Already included: `.nojekyll` (so GitHub serves correctly), `sitemap.xml`, `robots.txt`, `404.html`

### 4) FormSubmit activation (one time)
- Open `https://yourdomain.com` → send a test message via Contact
- Check **Mirajuddinxlx@gmail.com** inbox → open FormSubmit “Confirm your form” → Click **Confirm**
- Done — all future messages arrive instantly + are saved in Admin Inbox

### Edit content
- No separate dashboard — open your live site → hidden login (`miraj / Miraj2025!`) → edit inline → changes saved in browser `localStorage` (persistent). For true multi-device DB, later swap `localStorage` to Supabase/Firebase (code is isolated in `loadStore/saveStore`).

### Replace demo portrait
- Login → Settings → Profile Photo URL / Upload → Save. Or replace `heroImage` URL in `index.html` → commit & push.

### Local preview
```bash
python -m http.server 8000
# open http://localhost:8000
```

— Built for Miraj Uddin, Cassino 🇮🇹
