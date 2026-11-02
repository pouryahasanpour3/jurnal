# TradeJournal · ژورنال ترید (v1.0.0)

Crypto trade-journal PWA. Plain HTML/CSS/JS, no build step. Hosted on GitHub Pages under a subpath (all paths relative).

- `index.html` — the whole app (inline CSS + JS, i18n fa/en)
- `sw.js` — service worker, cache `tj-v1.0.0` (bump on each release)
- `manifest.webmanifest`, `icons/`

Data: one JSON state object in `localStorage` key `tj-state-v1` (`{v, ts, settings, setups, trades}`) so a Supabase sync layer can be added later. Screenshots live in IndexedDB `tj-db` / store `shots`. PIN hash in `tj-lock`.
