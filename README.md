# shaziyatambawala.com

Personal portfolio — static site hosted on GitHub Pages.

## File structure

```
portfolio/
├── index.html              ← WHAT (homepage)
├── how.html                ← HOW (project index)
├── who.html                ← WHO (about)
├── css/
│   └── style.css           ← all styles
├── what/
│   ├── ai-scorecards.html
│   ├── call-summary-templates.html
│   ├── automation-for-confluence.html
│   └── external-collaboration.html
└── assets/                 ← add your images + resume PDF here
    └── (logo.png, resume.pdf, project screenshots...)
```

## Setup — GitHub Pages

1. Create a GitHub account at github.com
2. Create a new repository named exactly: `YOUR-USERNAME.github.io`
   - e.g. `shaztam.github.io`
3. Upload all files from this folder (maintain the folder structure)
4. Go to Settings → Pages → Source: Deploy from branch → main → / (root)
5. Your site will be live at `https://YOUR-USERNAME.github.io` within a minute

## Custom domain

1. Buy your domain at namecheap.com or cloudflare.com (~$15/yr)
2. In your registrar's DNS settings, add these records:
   - A record → 185.199.108.153
   - A record → 185.199.109.153
   - A record → 185.199.110.153
   - A record → 185.199.111.153
   - CNAME → www → YOUR-USERNAME.github.io
3. In GitHub repo Settings → Pages → Custom domain → enter your domain
4. Check "Enforce HTTPS" (free SSL, handled by GitHub)

## Using Cursor to edit

1. Download Cursor from cursor.com (free tier works great)
2. Sign in with GitHub
3. File → Open Folder → select this portfolio folder
4. Use Cmd+K (Mac) or Ctrl+K (Windows) to ask Cursor's AI to help:
   - "Update the stats in ai-scorecards.html"
   - "Add a new project card to how.html"
   - "Make the nav sticky on mobile"
5. Save → git commit → git push → GitHub Pages auto-publishes

## Things to customize

- [ ] Replace `ST` logo text in nav with your actual logo image
- [ ] Add resume PDF to `assets/` and update the href in index.html + who.html
- [ ] Update the email address in nav mailto links
- [ ] Add project images to `assets/` and reference them in case study pages
- [ ] Update copyright year in footers if needed

## Adding project images

In each case study file, add an image like this after the `.lead` paragraph:

```html
<img
  src="../assets/ai-scorecards-hero.png"
  alt="AI scorecard suggestion UI"
  style="width:100%;border-radius:12px;margin:2rem 0;border:0.5px solid var(--color-border);"
/>
```

Recommended image sizes: 1400px wide, exported at 2x for retina.
