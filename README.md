# markuswoodson.github.io

Personal portfolio and CV site for Markus Woodson — Research Engineer, GenAI.

Built with plain HTML/CSS/JS (no framework, no build step). Hosted on GitHub Pages.
Design system: "Eco-Academic" — Hanken Grotesk type on a deep forest green / cream palette,
originally explored in Google Stitch (see the design tokens ported into `css/style.css`).

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
- [x] `images/profile.jpg` is set (600×600, square-cropped from a full-res photo). Swap it any time (same filename, or update the `src` in `index.html`)
- [ ] Add your CV PDF at `assets/markus-woodson-cv.pdf` (linked from the "CV" nav item on every page)

### Work Cards / Projects
Most cards use real images pulled from each project's official announcement (saved to `images/work/`).
- [ ] Video Background Removal still uses a gradient placeholder — no clean official image was found; add one to `images/work/` and add an `<img>` tag to that card if you find a good source
- [ ] Swap any image for a better one any time by replacing the file in `images/work/` (same filename) or updating the `src` in `projects.html`

### Photography (currently hidden)
The Photography page and its nav link / home page teaser are commented out until there's a real gallery.
To bring it back:
- [ ] Copy your `.jpg` or `.webp` photos into `images/photography/`
- [ ] In `photography.html`, replace each `photo-masonry-placeholder` block with the snippet shown in the comments
- [ ] Update the category headings to match your photo collections
- [ ] Un-comment the "Photography" nav link in every page's `<header>`, and the teaser section in `index.html`

### Branding
- [ ] If you want a favicon, add `favicon.ico` or `favicon.png` to the root and link it in `<head>` on every page

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
   git remote add origin https://github.com/mwoodson1/portfolio.git
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
├── index.html          # Home (hero/bio, photo teaser [currently commented out])
├── research.html        # Full publications list, grouped by year
├── projects.html        # Work/project cards
├── photography.html    # Full photography gallery (currently unlinked — no nav entry yet)
├── css/
│   └── style.css       # All styles (Eco-Academic design system)
├── js/
│   └── main.js         # Mobile nav, lightbox
├── images/
│   ├── profile.jpg     # Your headshot (add this)
│   ├── work/           # Work card thumbnails (optional)
│   └── photography/    # Your photos (add these)
└── assets/
    └── markus-woodson-cv.pdf  # Your CV (add this)
```
