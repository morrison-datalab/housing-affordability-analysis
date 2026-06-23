# Northeast Housing Affordability: A 50-Year Price-to-Income Analysis

## Overview
This project examines how housing affordability in the Northeast Census Region has changed over five decades, using a price-to-income ratio as the core analytical benchmark. The goal was to move beyond raw home prices, which inflation makes misleading across a 50-year span, and instead measure affordability relative to what an individual actually earns.

## The Question
How many years of individual income would it take to match the cost of a median home, and how has that relationship shifted between 1974 and 2024? Rather than using household income, this analysis deliberately uses individual income to test affordability from a single earner's perspective, a more realistic lens for understanding what one person, working alone, can actually afford.

## Data Sources
- FRED: Median Sales Price of Houses Sold, Northeast Census Region
- FRED: Median Personal Income, Northeast Census Region

## Methodology
Both datasets were imported into a SQLite database. A SQL JOIN combined median sales price and median individual income by year, followed by a calculated field generating the affordability ratio (price divided by income) for each year. A second calculated field modeled the dollar cost of a 20% conventional down payment, testing whether even the upfront barrier to homeownership has kept pace with income growth.

## Key Findings
- The price-to-income ratio rose from approximately **6.6x in 1974 to 17x in 2024**
- Median home prices increased **2,064%** over the period
- Median individual income increased only **743%** over the same period
- Even the 20% down payment alone now represents several years of individual income, before a single dollar of principal or interest is repaid

## Tools Used
SQL (SQLite), Tableau

## Files in This Repository
- `housing_data_to_income.db` — SQLite database containing both datasets and joined query results
- `housing_data_to_income.sqbpro` — DB Browser for SQLite project file
- `affordability_results.csv` — Final exported results, including price, income, ratio, and down payment calculations by year
- `Northeast Housing Affordability.twb` — Tableau workbook
- Dashboard PNG — Static export of the final visualization

## Conclusion
The data supports what many single-income individuals already feel: homeownership has become significantly less attainable for someone earning on their own. A median home in 2024 demands roughly 2.5 times more of a single income, relative to 1974, than it once did. Single-income individuals, including single parents, are increasingly being priced out of a market that, fifty years ago, was substantially more within reach on one income alone.
