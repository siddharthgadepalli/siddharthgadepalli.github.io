# Personal site

A simple static site + blog for Siddharth Gadepalli.

## Preview locally

```bash
cd personal-site
python3 -m http.server 8000
```

Then open:
- Home: http://localhost:8000
- Blog: http://localhost:8000/blog/

## What’s included

- `index.html` — home / about / research / experience
- `blog/` — blog index + posts
- `blog/_template.html` — copy this to write a new post
- `profilepic.jpg` — portrait

## Add a blog post

1. Copy `blog/_template.html` → `blog/YYYY-MM-DD-short-title.html`
2. Edit the title, date, and body
3. Add a new entry at the **top** of the list in `blog/index.html`
4. Commit and push (or redeploy)

## Deployment — you do **not** need Netlify

Either works. **GitHub Pages is the simplest** for a personal `.github.io` site.

### Option A: GitHub Pages (recommended)

Free hosting directly from GitHub.

1. Create a public repo named exactly `YOUR_USERNAME.github.io`
2. Push everything in this folder to the repo **root** (`index.html` at top level)
3. Repo **Settings → Pages →** Deploy from branch `main` / `/ (root)`
4. Site live at `https://YOUR_USERNAME.github.io`

```bash
git init
git add .
git commit -m "Initial personal site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
git push -u origin main
```

### Option B: Netlify (also fine)

Good if you want drag-and-drop deploy or a custom domain UI.

1. Go to [netlify.com](https://www.netlify.com)
2. “Add new site” → deploy this folder (or connect the GitHub repo)
3. Publish directory = the folder with `index.html` (this folder)
4. You get a `something.netlify.app` URL (custom domain optional)

**Bottom line:** GitHub Pages is enough. Netlify is optional, not required.
