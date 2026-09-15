# Sources

## Filing / company disclosure

Store sales in this dashboard follow Amazon’s **Physical stores** net sales line. Whole Foods is nearly all of that number (Amazon Fresh and Amazon Go were small and were closed in 2026).

| Year | Physical stores ($B) | Source |
|------|----------------------|--------|
| 2018 | 17.22 | Amazon Form 10-K |
| 2019 | 17.19 | Amazon Form 10-K |
| 2020 | 16.23 | Amazon Form 10-K |
| 2021 | 17.08 | Amazon Form 10-K |
| 2022 | 18.96 | Amazon Form 10-K |
| 2023 | 20.03 | Amazon Form 10-K ($20,030M) |
| 2024 | 21.22 | Amazon Form 10-K ($21,215M) |
| 2025 | 22.56 | Amazon Form 10-K year ended 31 Dec 2025 ($22,561M) |
| 2026 | 23.40 | YTD annualized through August 2026 — **not** a full-year 10-K |

Amazon 10-K footnote: product sales where customers physically select items in a store. Orders placed online for **pickup or delivery from a store are booked in Online stores**, not Physical stores. That is why pickup and delivery are modeled separately.

Other disclosures used:

- Whole Foods Market, Inc. Form 10-K FY2016 — last independent filing: net sales $15.72B, 456 stores.
- Amazon acquisition of Whole Foods closed 28 August 2017, $13.7B.
- Amazon, 27 January 2026 — close Amazon Fresh and Amazon Go; grocery GMV more than $150B; Whole Foods sales up more than 40% since 2017; 550+ stores.

## Third party

- Numerator, June 2026 — 17 million U.S. households shopped both Amazon and Whole Foods in the 12 months ending 30 April 2026.
- Public store locators / ScrapeHero (July 2026) — store counts by state (CA 93, FL 39, NY 36, TX 36, MA 33, …).

## Modeled (not internal POS)

Category mix, 365 rates, Prime share, pickup/delivery split, state sales shares, and the 12-item price basket are a reconstructed operating model so the dashboard can be shown without Whole Foods POS or Nielsen. They are labeled as modeled in the CSVs. Replace with warehouse tables if using this as a working scorecard.
