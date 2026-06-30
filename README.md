# Lead Radar — Web3 Coin Research & Lead Generation Tool

A single-page tool for discovering, scoring, and tracking Web3 projects for exchange listing outreach, OTC deals, market making, and BD pipelines.

🔗 **Live demo:** enable GitHub Pages on this repo (see below) and it'll be live at `https://<your-username>.github.io/<repo-name>/`

## Features

- **Live Lookup** — pulls real-time data from CoinGecko and DexScreener (price, volume, liquidity, market cap, exchange coverage, social links, community size)
- **Manual Entry** — structured form for everything that can't be pulled automatically: audit status, ownership/security checks, website quality score, scam reports, partnership fit
- **Lead Scoring** — automatic 1–100 score (volume 20%, liquidity 20%, community 15%, exchange coverage 15%, website 10%, narrative strength 10%, security 10%), tiered Exceptional → High Risk
- **Risk Flags** — auto-detected (low liquidity, no audit, dead community, low holder count, etc.) plus manual flags
- **Rankings** — Top 10 Overall, CEX, DEX, by narrative (AI, Meme, DeFi, Infrastructure, RWA, etc.), highest liquidity/volume, most undervalued, newest
- **CSV Export** — for outreach lists
- **Local persistence** — leads save to your browser's local storage, no backend required

## Run it locally

No build step — it's a single static HTML file.

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
open index.html   # or just double-click the file
```

## Deploy with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, select the `main` branch and `/ (root)` folder.
4. Save — your tool will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## Notes

- Data is stored in `localStorage`, scoped per browser/device — it won't sync across devices or browsers. For a shared team database, this would need a small backend (e.g. Supabase, Firebase) — open an issue if you want that added.
- CoinGecko's free API has rate limits; if Live Lookup fails repeatedly, wait a minute and retry, or fall back to Manual Entry.
- This tool is for research aggregation only — always independently verify contract addresses, audits, and team claims before any deal or transaction.

## License

MIT — use freely, attribution appreciated.
