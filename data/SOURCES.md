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
| 2026E | 23.35 (23.348) | Estimate, **not** a full-year 10-K: first nine months 2026 Physical stores $17,289M (Q1 $5,785M, Q2 $5,794M ([Q2 2026 10-Q](https://www.sec.gov/Archives/edgar/data/1018724/000101872426000026/R24.htm)), Q3 $5,710M ([Amazon Q3 2026 results, Oct 28 2026](https://ir.aboutamazon.com/news-release/news-release-details/2026/Amazon-com-Announces-Third-Quarter-Results/default.aspx))) × FY2025 / first nine months 2025 ($22,561M / $16,706M) |

Amazon 10-K footnote: product sales where customers physically select items in a store. Orders placed online for **pickup or delivery from a store are booked in Online stores**, not Physical stores. That is why pickup and delivery are modeled separately and added **on top of** Physical stores, not carved out of it (`prime_channel.csv`: `instore_b` = the 10-K line, `store_fulfilled_b` = in-store + pickup + delivery).

Other disclosures used:

- Whole Foods Market, Inc. Form 10-K FY2016, last independent filing: net sales $15.72B, 456 stores.
- Amazon acquisition of Whole Foods closed 28 August 2017, $13.7B.
- Amazon, 27 January 2026: close Amazon Fresh and Amazon Go; grocery GMV more than $150B; Whole Foods sales up more than 40% since 2017; 550+ stores.

## Company tab (fetched October 24, 2026, updated October 29, 2026)

- Amazon Form 10-K FY2025: Physical stores $20,030M / $21,215M / $22,561M (2023 to 2025). https://www.sec.gov/Archives/edgar/data/1018724/000101872426000004/amzn-20251231.htm
- Kroger Form 10-K (fiscal year ended Jan 31 2026): sales $147.6B. Sprouts Farmers Market Form 10-K (fiscal year ended Dec 28 2025): sales $8.8B. SEC XBRL company facts. Used for the peer sales view.
- Amazon, Jan 27 2026: close Go and Fresh stores, 100+ new Whole Foods stores planned, 550+ locations. https://www.aboutamazon.com/news/company-news/amazon-fresh-go-stores-closing-expanding-whole-foods
- Whole Foods Market, May 13 2026: Daily Shop leases in Boston, Chicago and Philadelphia. https://www.wholefoodsmarket.com/company-info/newsroom/news-releases
- Grocery Dive, Mar 12 2026: six London Daily Shops opening April to June 2026, UK stores to 12.
- ICSC, Sep 2026: 12 Daily Shop stores (6 US, 6 London).
- Yahoo Finance, Sep 3 2026: Physical stores sales up 4% in Q2 2026.
- Amazon Q3 2026 results, Oct 28 2026: Physical stores $5,710M vs $5,578M in Q3 2025 (+2.4%). https://ir.aboutamazon.com/news-release/news-release-details/2026/Amazon-com-Announces-Third-Quarter-Results/default.aspx
- Whole Foods Market newsroom, Oct 6 to 21 2026: six store openings Nov 5 to 19 2026 (Bradenton, Simi Valley, Los Angeles 3rd and Fairfax flagship of 63,082 square feet on Nov 11, Scottsdale, West Chester, Midlothian). https://www.wholefoodsmarket.com/company-info/newsroom/news-releases
- Share price: Amazon (AMZN), Yahoo Finance daily closes, Oct 30 2025 to Oct 29 2026.

## Third party

- Numerator, June 2026: 17 million U.S. households shopped both Amazon and Whole Foods in the 12 months ending 30 April 2026.
- Public store locators / ScrapeHero (July 2026): store counts for the top 10 states (CA 93, FL 39, NY 36, TX 36, MA 33 and others). "All other states" is the remainder to Amazon's 550 stores.

## Modeled (not internal POS)

Category mix, 365 rates, Prime share, pickup/delivery split, state sales shares, and the 12-item price basket are a reconstructed operating model so the dashboard can be shown without Whole Foods POS or Nielsen. They are labeled as modeled in the CSVs. Replace with warehouse tables if using this as a working scorecard.
