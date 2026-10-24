**Live dashboard:** https://rituneupane.github.io/whole-foods-after-amazon/

# Whole Foods after Amazon

I pulled Amazon’s public 10-K Physical stores line (2018 to 2025) and asked three questions a merchant would actually ask:

1. How big is Whole Foods now?
2. What is 365 doing as the house brand?
3. What did Amazon Prime change about who shops the store, and how orders leave it?

This is my own compilation. Not affiliated with Amazon or Whole Foods Market. Not a stock pick.

Store sales are **Whole Foods store dollars**. Amazon reports them as “Physical stores.” Whole Foods is nearly all of that line.

## What I found

- Store sales went from **$17.2B (2018)** to **$22.6B (2025)** and an estimated **$23.5B in 2026** (2026E), about **36% above 2018**. Whole Foods is now Amazon’s only physical grocery banner.
- **365** is 24.8% of grocery and only 11.6% of the whole store. A 12-item 365 basket is **$57 vs $77** for national Whole Foods brands, next to Kroger ($58). Trader Joe’s is still cheaper ($48). 365 does not need to win that race.
- **Prime members** are about **54%** of Whole Foods sales in 2026E, up from about a third in 2018. Pickup and delivery add about **$4.7B** on top of the store line, or **17%** of what the stores fill (modeled; Amazon books them in Online stores). 17 million households already shop both Amazon and Whole Foods.

Category mix, Prime share, state sales, and the basket are modeled from public store counts and grocery research. The 10-K dollars are not. Detail: [`data/SOURCES.md`](data/SOURCES.md).

**2026E method.** Amazon reports quarterly, so there is no through-August number. 2026E = H1 2026 Physical stores ($11,579M, Q2 2026 10-Q) × FY2025 / H1 2025 ($22,561M / $11,128M) = **$23.48B**, +4.1%.

**365 of all sales.** 24.8% of grocery × grocery's 24.6% of store sales is about 6.1% of the store. The modeled 11.6% therefore includes 365 items outside the grocery department (fresh, wellness). Treat it as a modeled whole-store share, not grocery × mix.

## Checks

`python analysis/build.py` runs the tie-outs and rebuilds the dashboard data (`docs/data.js`). All 56 pass (`data/checks.csv`):

- Category shares add to 100% and category dollars add to store sales, every year.
- In-store dollars equal the 10-K Physical stores line; in-store + pickup + delivery = store-fulfilled sales.
- State store counts add to 550; state sales add to 2026E.
- Prime + non-Prime = 100%; YoY % recomputed from the dollars.

## Dashboard

Live: https://rituneupane.github.io/whole-foods-after-amazon/ (source in `docs/`).

**Overview:** store sales, category, state

![Overview](screenshots/overview.png)

**365:** house brand

![365](screenshots/365.png)

**Prime’s effect:** who shops, how orders leave

![Prime](screenshots/prime.png)

## Files

```
data/wfm_annual.csv        10-K store sales, stores, 365, Prime
data/category_mix.csv      five departments × year
data/prime_channel.csv     Prime share; 10-K in-store + modeled pickup / delivery
data/state_sales.csv       top states
data/price_basket.csv      12-item basket vs peers
data/SOURCES.md            filing vs modeled
analysis/notes.md          takeaways
data/checks.csv            tie-out checks (generated)
analysis/build.py          runs checks, writes docs/data.js
docs/                      live dashboard
screenshots/               overview, 365, Prime
```

MIT License.
