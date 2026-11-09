# Road to 270 🇺🇸

**An AI-built, interactive probabilistic forecast of the 2028 U.S. presidential election.**

Build your own 2028 election: set the economy, pick the nominees, move turnout and dozens of other real-world signals, and watch all 50 states, the Electoral College, and the odds of winning redraw in real time.

> ⚠️ A teaching model and a hypothetical — not a prediction of record. No 2028 polling exists yet; every number is a modeled estimate. State baselines use real 2024 certified results, and the historical maps are real results 1960–2024.

## Features
- **Interactive map** — real geographic U.S. map (and a tile-map cartogram), colored by margin, win probability, or flips.
- **Probabilistic engine** — a 4-layer model (fundamentals → demographic voter blocks → 2024 calibration → 2,001-run Monte Carlo) producing win odds, an outcome range, and the tipping-point state.
- **30+ defined inputs** — economy, approval, turnout by demographic group, education polarization, event shocks, and more — each explained in plain English under the slider and in a full glossary.
- **1960–2024 history explorer** — replay every real presidential map and each state's voting record.
- **14 candidates** — real photos, profiles, and an electability matrix.
- **AI Forecast** — a written central-case call: who wins, and why.
- **Fun tools** — election-night simulator, swing-o-meter, Electoral College bias meter, "ask in plain English," Beat-the-model game, Maine/Nebraska district split, and more.

## Run it
It's a static site — no build step. Open `index.html` through any local web server (the app loads `us-states.geojson` and `history.json` with relative paths, which browsers block over `file://`):

```bash
cd road-to-270
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy it (free public URL)
Any static host works. Two easy options:
- **GitHub Pages:** repo **Settings → Pages → Branch `main` / root**. Live at `https://<username>.github.io/road-to-270/`.
- **Netlify:** drag this folder onto [app.netlify.com/drop](https://app.netlify.com/drop).

## Files
| File | What it is |
|---|---|
| `index.html` | The entire app (model, UI, visuals) |
| `us-states.geojson` | U.S. state geometry for the map |
| `history.json` | 1960–2024 state-by-state results |
| `img/` | Candidate photos |

## Credits
- Built with [Claude](https://claude.com/claude-code).
- Geography: U.S. Census cartographic boundaries (via us-atlas).
- Candidate photos: U.S. government official portraits (public domain) and Wikimedia Commons; per-candidate sources are listed in the app's **Data** section.
- Model framing after Abramowitz's "Time for Change," Hibbs's "Bread and Peace," and the simulation approach of outlets like 538 and The Economist. Coefficients are illustrative, not fitted.
