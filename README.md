# ⚡ Resistor Decoder — Color Code Calculator

A sleek, dark-themed interactive tool for electronics engineers and hobbyists to decode and encode resistor color bands instantly.

**Live App URL:** *(paste your Vercel URL here after deploy)*

---

## Features

- **Decode → Value** — Select 4 or 5 color bands from dropdowns and instantly see the resistance value, tolerance, and min/max range
- **Encode → Colors** — Type a resistance value (Ω, kΩ, MΩ) and get the exact color bands to look for
- **Color Reference Table** — Full IEC 60062 color code chart with digit, multiplier, tolerance, and temp coefficient
- **Live visual resistor** — See a rendered resistor update in real time as you change bands

---

## Tech Stack

- Pure HTML + CSS + Vanilla JS (zero dependencies, zero build step)
- ~400 lines, single file
- Deploys as a static site

---

## Deployment: Vercel (Recommended — Free Tier)

### Option A: Drag & Drop (Fastest)
1. Go to [vercel.com](https://vercel.com) and sign in (GitHub recommended)
2. Click **"Add New Project"** → **"Deploy from your computer"** (or use drag & drop on the dashboard)
3. Drop the entire `resistor-calc/` folder onto the Vercel dashboard
4. Click **Deploy** — done in ~10 seconds
5. Vercel gives you a `*.vercel.app` URL instantly

### Option B: CLI Deploy
```bash
npm install -g vercel
cd resistor-calc/
vercel
# Follow prompts — choose "Static" when asked
# Your app is live at the printed URL
```

### Option C: GitHub → Vercel (best for rolling updates)
1. Push this folder to a GitHub repo:
   ```bash
   git init
   git add .
   git commit -m "Initial deploy: Resistor Decoder"
   git remote add origin https://github.com/YOUR_USERNAME/resistor-decoder.git
   git push -u origin main
   ```
2. Go to [vercel.com/new](https://vercel.com/new) → **Import Git Repository**
3. Select your repo → click **Deploy**
4. Every `git push` to `main` auto-redeploys (rolling updates!)

---

## Rolling Updates

With GitHub integration, updates are automatic:
```bash
# Make changes to index.html
git add index.html
git commit -m "Fix: update tolerance range formula"
git push origin main
# Vercel detects push → rebuilds → live in ~15 seconds
```

To manually redeploy via CLI:
```bash
vercel --prod
```

---

## Environment Variables

This app has no backend and requires **no environment variables** — it's entirely client-side JavaScript.

If you add a backend later (e.g., a FastAPI service for component lookup), you would set:
```
# In Vercel Dashboard → Project Settings → Environment Variables
API_BASE_URL=https://your-api.com
```

---

## Alternative PaaS Options

| Platform | Method | Notes |
|---|---|---|
| **Vercel** ✅ | Drag & drop or CLI | Best for static sites, free tier |
| **Netlify** | Drag & drop | Same simplicity as Vercel |
| **GitHub Pages** | Repo settings | Free, requires public repo |
| **Fly.io** | Docker + `fly deploy` | Overkill for static, but works |
| **Railway** | GitHub connect | Good for when you add a backend |

---

## Project Structure

```
resistor-calc/
├── index.html      # Entire app (HTML + CSS + JS)
├── vercel.json     # Vercel deployment config
└── README.md       # This file
```

---

## Submission Checklist

- [x] Live app URL: `___________________`
- [x] Source code in `Tutorials/Submissions/<Name>/Week-08/`
- [x] README with deployment steps (this file)
- [ ] Optional: demo GIF or video

---

*Built with no frameworks, no build tools, no npm install. Just open `index.html` locally and it works.*
