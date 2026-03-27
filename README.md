# markuswoodson.github.io

Personal portfolio and CV site for Markus Woodson — Research Engineer, GenAI.

Built with plain HTML/CSS/JS. No build step required. Hosted on GitHub Pages.

---

## Local Development

Just open `index.html` in a browser, or use any static file server:

```bash
# Python 3
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## Customization Checklist

### Profile
- [ ] Replace `images/profile.jpg` with your headshot (recommended: 400×400px, square crop)
- [ ] Update the email address in `index.html` and `photography.html` (search for `markus@example.com`)
- [ ] Update the GitHub URL in both pages if your handle differs from `markuswoodson`
- [ ] Update the Google Scholar URL with your actual profile ID
- [ ] Add your CV PDF at `assets/markus-woodson-cv.pdf`

### Publications
- [ ] Fill in the publication entries in `index.html` (search for `<!-- TODO: Replace with your actual publications -->`)
- [ ] Each entry has: venue badge, year, title (linked to paper), authors (bold your name), and links

### Work Cards
- [ ] Optionally add real screenshots/thumbnails:
  - Save images to `images/work/` (recommended: 800×450px)
  - In each `.work-card-image` div, uncomment the `<img>` tag and update the `src`

### Photography
- [ ] Copy your `.jpg` or `.webp` photos into `images/photography/`
- [ ] In `photography.html`, replace each `photo-masonry-placeholder` block with the snippet shown in the comments
- [ ] Update the category headings to match your photo collections
- [ ] The lightbox activates automatically for any item with `data-src`

### Branding
- [ ] Update `<title>` and `<meta name="description">` in both HTML files
- [ ] If you want a favicon, add `favicon.ico` or `favicon.png` to the root and link it in `<head>`

---

## Deploying to GitHub Pages

### First-time setup

1. **Create the repo** on GitHub (suggested name: `markuswoodson.github.io` for a root domain, or any name for a project page)

2. **Initialize and push:**
   ```bash
   cd portfolio
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/markuswoodson/markuswoodson.github.io.git
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to your repo on GitHub → **Settings** → **Pages**
   - Under *Source*, select **Deploy from a branch**
   - Choose `main` branch, `/ (root)` folder
   - Click **Save**

4. **Visit your site** at `https://markuswoodson.github.io` (takes ~1 minute to deploy)

### Custom Domain (optional)

1. Buy a domain (e.g., `markuswoodson.com`) from Namecheap, Cloudflare, etc.
2. In your domain's DNS settings, add:
   ```
   Type: CNAME  Name: www   Value: markuswoodson.github.io
   ```
   Or for apex domain, add A records pointing to GitHub's IPs:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
3. In the repo → **Settings** → **Pages** → **Custom domain**, enter your domain
4. Check **Enforce HTTPS** once the cert provisions (~10 min)

### Updating the site

```bash
git add .
git commit -m "Update publications"
git push
```
GitHub Pages auto-redeploys within ~30 seconds.

---

## File Structure

```
portfolio/
├── index.html          # Main page (about, work, publications, photo teaser)
├── photography.html    # Full photography gallery
├── css/
│   └── style.css       # All styles
├── js/
│   └── main.js         # Mobile nav, lightbox, scroll behavior
├── images/
│   ├── profile.jpg     # Your headshot (add this)
│   ├── work/           # Work card thumbnails (optional)
│   └── photography/    # Your photos (add these)
└── assets/
    └── markus-woodson-cv.pdf  # Your CV (add this)
```
