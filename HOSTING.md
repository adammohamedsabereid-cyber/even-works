# Hosting — already live on GitHub Pages

The site is published at:
**https://adammohamedsabereid-cyber.github.io/even-works/**

- Repo: `adammohamedsabereid-cyber/even-works` (public, branch `main`, root)
- Downloads live in `downloads/` — currently `Even-Tweaker.exe`.
  When the other apps ship, drop their .exe files in this folder and add
  the matching `href` on each card in `index.html`.
- To update the site: edit files, then `git add -A && git commit -m "update" && git push`
  — GitHub Pages rebuilds automatically in ~1 minute.

## Alternatives (if you ever want to move it)

### Netlify Drop
1. Go to **https://app.netlify.com/drop**
2. Drag the whole `even-site` folder onto the page
3. Live URL instantly; sign up free to keep + rename it

### Vercel
1. **vercel.com** → import the `even-works` repo
2. Deploy — done.

---

## Files that ship

```
downloads/
└── Even-Tweaker.exe   (27 MB — the one released app; license key required)
```

The other four apps (Macro, Driver Updater, Password Vault, Stats) are
still in development — their cards show "IN DEVELOPMENT" until their
builds are ready.


---

## 1. Netlify Drop — live in 60 seconds, no account needed at first

1. Go to **https://app.netlify.com/drop**
2. Drag the whole `even-site` folder onto the page
3. Done — you get a live URL like `https://random-name.netlify.app`
4. Sign up (free) to claim the URL permanently and rename it
   (Site settings → Change site name → `even-apps.netlify.app`)

## 2. GitHub Pages — best for keeping it forever

1. Create a free account at github.com, then a new repository
   (name it anything, e.g. `even-site`, keep it **Public**)
2. Click **uploading an existing file** and drag all the site files in
   (index.html must be in the root, not inside a subfolder)
3. Repo → **Settings → Pages** → Source: *Deploy from a branch* →
   Branch: `main` / `/ (root)` → Save
4. Wait ~1 minute → your site is at
   `https://YOUR-USERNAME.github.io/even-site/`

## 3. Vercel — same drag-and-drop idea

1. Go to **vercel.com** → sign up free with GitHub
2. **Add New → Project** → import the repo (or use the CLI:
   `npm i -g vercel` then `vercel` inside the folder)
3. Live URL like `even-site.vercel.app`

---

## Which one?

| | Netlify Drop | GitHub Pages | Vercel |
|---|---|---|---|
| Setup time | 60 sec | ~5 min | ~3 min |
| Needs git? | No | Yes (upload UI) | No |
| Custom domain | Free | Free | Free |
| Bandwidth | 100 GB/mo | 100 GB/mo (soft) | Generous |

All three are free for a download page like this. **Tip:** big .exe files
(github hard-caps at 100 MB/file) may be better on a release/CDN link —
if an app is huge, host the exe on GitHub **Releases** and point the
button's `href` at that direct link instead.
