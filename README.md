# Road to 270 — deploy guide

An interactive, probabilistic 2028 election platform. To host it, upload these next to each other:

- `index.html` — the whole app
- `us-states.geojson` — US map geometry
- `history.json` — 1960–2024 election results
- `img/` — the 14 candidate photos (keep the folder name `img`)

`us-states.json` is the raw source geometry — **not needed to deploy**.

## Option A — Netlify (easiest, drag-and-drop)
1. Go to app.netlify.com → **Add new site → Deploy manually**.
2. Drag the whole `road-to-270` folder onto the page.
3. You get a public `https://<name>.netlify.app` URL instantly. Add a custom domain in Site settings if you want.

## Option B — GitHub Pages (free public URL)
1. Create a repo, e.g. `road-to-270`.
2. Upload `index.html`, `us-states.geojson`, `history.json`, and the `img/` folder.
3. **Settings → Pages → Build from branch → `main` / root → Save**.
4. Live at `https://<your-username>.github.io/road-to-270/` in ~1 minute.

Both work because the app loads its data with **relative** paths — any static host works (Vercel, Cloudflare Pages, etc.). No server code needed.

## Swapping candidate photos
Photos live in `img/<id>.jpg` (e.g. `img/vance.jpg`). Replace any file with your own square image of the same name to change it. Current photos are U.S. government official portraits (public domain) and Wikimedia Commons images; credits are listed in the app's **Data** section.

## Notes
- The CSV "download" works on your own hosted site; inside the claude.ai preview it copies to the clipboard instead (browser download is sandboxed there).
- County-level zoom and live polling/market feeds are the planned next additions.
