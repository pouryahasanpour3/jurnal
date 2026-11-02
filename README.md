# TradeJournal · ژورنال ترید (v1.1.1)

Crypto trade-journal PWA. Plain HTML/CSS/JS, no build step. Hosted on GitHub Pages under a subpath (all paths relative).

- `index.html` — the whole app (inline CSS + JS, i18n fa/en)
- `sw.js` — service worker, cache `tj-v1.1.1` (bump on each release)
- `manifest.webmanifest`, `icons/`

Data: one JSON state object in `localStorage` key `tj-state-v1` (`{v, ts, settings, setups, trades}`) so a Supabase sync layer can be added later. Screenshots live in IndexedDB `tj-db` / store `shots`. PIN hash in `tj-lock`.

Numbers: every displayed number uses thousands grouping (`٬`/`٫` with Persian digits, `,`/`.` with Latin digits). Number inputs (prices, size, fees, leverage, starting balance) are grouped live while typing and parsed back to plain numbers on save. CSV/JSON exports keep raw numbers with no separators.
