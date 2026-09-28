# World's Eye

See the world live — free public cameras from everywhere on Earth.

## ⚠️ Important: it will NOT install from a local file

You **must** host this on HTTPS (GitHub Pages is free and works).

Opening `index.html` from Downloads / Files will show the page but:
- Install to Home Screen will not work
- Service worker will not register

## Install on phone (GitHub Pages)

### 1. Create the repo
1. Go to https://github.com/new
2. Repository name: `worlds-eye` (or any name)
3. Public → Create repository

### 2. Upload files
Upload **all** of these (keep the folder structure):

```
index.html
manifest.json
sw.js
README.md
icons/
  favicon.ico
  favicon-16.png
  favicon-32.png
  icon-180.png
  icon-192.png
  icon-512.png
  … (rest of icons)
```

Do **not** put them inside an extra folder.  
`index.html` must be at the **root** of the repository.

### 3. Turn on GitHub Pages
1. Repo → **Settings** → **Pages** (left sidebar)
2. Source: **Deploy from a branch**
3. Branch: **main** (or master) → folder **/ (root)** → Save
4. Wait 1–2 minutes

Your site will be:
`https://YOUR_USERNAME.github.io/worlds-eye/`

### 4. Add to Home Screen

**iPhone**
1. Open the link above in **Safari** (not Chrome)
2. Tap the **Share** button
3. Scroll and tap **Add to Home Screen**
4. Tap **Add**

**Android**
1. Open the link in **Chrome**
2. Tap menu **⋮**
3. Tap **Install app** or **Add to Home screen**

You should see the eye + Earth icon on your home screen.

## Troubleshooting

| Problem | Fix |
|--------|-----|
| No "Add to Home Screen" | Must use Safari on iPhone; must be HTTPS |
| Icon is blank / generic | Wait for Pages deploy; hard-refresh; check `icons/` uploaded |
| Page 404 | `index.html` must be at repo root, not in a subfolder |
| "Does not work" after install | Open the GitHub Pages URL once in browser first |

## Local test (optional)

```bash
cd worlds-eye
python3 -m http.server 8080
```
Then open `http://localhost:8080` — still not installable as PWA unless you use HTTPS.
