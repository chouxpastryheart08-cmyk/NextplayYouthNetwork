[README.md](https://github.com/user-attachments/files/30029395/README.md)
# Nextplay Youth Network — Website

Single-page static site. No build step, no dependencies — just one `index.html` file.

## 1. Push to GitHub

```bash
# In a new folder containing index.html and this README:
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/nextplay-website.git
git push -u origin main
```

Or, on GitHub.com: create a new repo → "uploading an existing file" → drag in `index.html` → commit.

## 2. Deploy on Vercel (via GitHub import — not the API)

1. Go to vercel.com → **Add New → Project**
2. Choose **Import Git Repository** and select the repo you just pushed
3. Framework preset: choose **Other** (it's a static file, no build needed)
4. Leave Build Command / Output Directory blank
5. Click **Deploy**

This import flow uses your normal Vercel login session, so it should work even if the API-based deploy hit permission errors.

## 3. Connect nextplayyouthnetwork.org

Once deployed, in the Vercel project: **Settings → Domains → Add** → enter `nextplayyouthnetwork.org`.

Vercel will give you DNS records (typically an `A` record for the root domain and a `CNAME` for `www`). Add those in **Squarespace → Domains → nextplayyouthnetwork.org → DNS Settings**.

**Important:** only add/change the records Vercel gives you for the website. Leave your existing `MX` records (Google Workspace email) untouched — those are separate and unaffected.

DNS changes can take a few hours to fully propagate.

## Notes
- Contact info (email/phone) and social links in the footer are placeholders — search `[ email address ]`, `[ phone number ]`, and the `#` hrefs in the social row to fill in real values.
- Fonts (Playfair Display, Poppins) load from Google Fonts via CDN — no local font files needed.
