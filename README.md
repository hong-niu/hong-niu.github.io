# Site scaffold

Plain HTML/CSS, no build step. Pages: `index.html` (About), `research.html`, `publications.html`, `cv.html`, `contact.html`, styles in `css/style.css`.

## Preview locally

Open `index.html` directly in a browser, or run a local server from this folder:

```
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Deploy on GitHub Pages (free)

1. Create a GitHub account if you don't have one, and a new repository named `<your-username>.github.io` (this exact name gives you a root-level URL like `hongniu.github.io`; any other repo name works too but serves from a subpath).
2. From this folder, initialize git and push:
   ```
   git init
   git add .
   git commit -m "Initial site scaffold"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. On GitHub: repo → Settings → Pages → under "Build and deployment," set Source to "Deploy from a branch," branch `main`, folder `/ (root)`. Save.
4. Wait 1-2 minutes, then visit `https://<your-username>.github.io`.
5. Optional custom domain (e.g. `hongniu.com`): buy the domain from any registrar, add a `CNAME` file to this repo containing just the domain name, and point the registrar's DNS to GitHub Pages (A records to GitHub's IPs, or a CNAME record if using a subdomain). GitHub's docs walk through this under Settings → Pages → Custom domain.

## Next steps

- Replace all `[bracketed placeholders]` with real content.
- Add a headshot photo (drop an image in the folder, reference it with `<img src="photo.jpg">` in `index.html`).
- Add your CV as `cv.pdf` in this folder — the CV page already links to it.
- Consider swapping this hand-built scaffold for a template like [al-folio](https://github.com/alshedivat/al-folio) later if you want a more built-out academic theme; the file structure and GitHub Pages steps above still apply.
