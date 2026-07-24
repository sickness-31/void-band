# VO!D — Band Website

Official site for VO!D. Built as a single HTML file, hosted free on GitHub Pages.

---

## How to update the site

Open `index.html` in VS Code. Every piece of content you'd want to change is marked with a `<!-- CHANGE: -->` comment. Search for `CHANGE:` to jump between them.

Save the file, commit, push — the site updates within about 60 seconds.

---

## Common updates

### Add a show date
Find `<!-- COPY FROM HERE -->` in the Live section.
Copy the entire `<div class="show-row">` block beneath it.
Paste it below, update the date, venue, city, and ticket link.

### Remove a show
Delete the `<div class="show-row">...</div>` block for that show.

### Add a new release
In the Music section, duplicate the `release-block` div.
Update the year, format, title, description, and Spotify embed.
To get a new Spotify embed: open the release in Spotify → three dots → Share → Embed → copy the iframe code.

### Update social links
Find the Social Links block in the Contact section.
Each `<a>` tag has a `href=` — replace the URL inside the quotes.

### Add a product to merch
Find the merch grid. Copy one `<div class="merch-card">` block, paste it, update the title, description, and price.

---

## File structure

```
void-band/
├── index.html              ← entire site
├── CNAME                   ← custom domain (add your domain name here)
├── README.md               ← this file
└── assets/
    └── images/
        ├── logo-hero.png       ← shrapnel explosion logo (voidalt_01)
        ├── logo-footer.png     ← block logo (voidalt_02)
        ├── photo-live.jpg      ← full band shot
        ├── photo-silhouette.jpg ← fluorescent silhouette shot
        ├── photo-guitar.jpg    ← 8-string close-up
        ├── photo-vocalist.jpg  ← vocalist from behind
        ├── photo-drums.jpg     ← drummer B&W
        └── release-residual.jpg ← RESIDUAL album art
```

---

## Setting up GitHub Pages

1. Push this repo to GitHub (must be **public**)
2. Go to the repo → Settings → Pages
3. Source: Deploy from branch → `main` → `/root` → Save
4. Site goes live at `https://yourusername.github.io/void-band`

## Adding a custom domain

1. Buy a domain (namecheap.com is good, ~$15/year)
2. Open the `CNAME` file in this repo and type your domain name (e.g. `voidband.com`)
3. In your domain registrar's DNS settings, add these records:
   - A record → `185.199.108.153`
   - A record → `185.199.109.153`
   - A record → `185.199.110.153`
   - A record → `185.199.111.153`
4. Back on GitHub → Settings → Pages → Custom domain → enter your domain → Save
5. Check "Enforce HTTPS" once it activates (takes up to 24 hours)

---

## Changing colors

Open `index.html`, find the `:root {` block near the top of the `<style>` section.
The color variables are all there with comments explaining each one.

---

*Site built and maintained by Sickness Studios*
