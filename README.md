# What Drives ER Wait Times across America?

BA780 Final Project · Cohort A · Team 4

**Team:** Hassan Imran Malik (PM), Michael, Weiran Wang, Aashna Pathi

## Overview

The same ER visit can take 2 hours or 6. This project looks at what explains the gap in ER wait times across U.S. hospitals and states.

We looked at four angles:
1. The hospital: what matters most
2. The patients: who pays the price
3. Owners (for-profit, non-profit, government)
4. Economies and states

The results can help hospital leaders decide where to add staff, and help state health departments decide where to send funding.

## Files

| File | What it is |
|------|------------|
| `A04-What-Drives-ER-Wait-Times_-_Final.ipynb` | Main Jupyter notebook: data cleaning, analysis, and charts |
| `What-Drives-ER-Wait-Times-Plain-Deck_pptx.pdf` | Final presentation slides |

## Data

We combined three sources (138,084 raw rows) into one clean table, `final_data`: **4,080 hospitals × 67 columns**, covering all 50 states.

- CMS Timely & Effective Care
- CMS Hospital General Information
- Census ACS 2024

## Key Findings

- **Typical ER visit:** median 148 min, mean 157 min. The slowest hospitals go past 400 min.
- **ER volume matters most.** It explains about 39% of the differences in wait times. Star ratings explain under 1%.
- **Busier ERs are slower.** Median wait rises from 120 min (low volume) to about 193 min (very high volume).
- **Patients leave unseen.** Hospitals with stays over 4 hours have a 5.6x higher leave rate than those under 2 hours (3.91% vs 0.70%, r = 0.52).
- **Psychiatric patients wait longest,** and their waits grow as ER volume rises.
- **Ownership:** at very high volume, for-profit ERs are about an hour faster (138 min vs about 202–204 min).
- **Rural states are faster.** A higher share of Critical Access hospitals goes with shorter stays (r = −0.72).
- **Richer states wait longer.** About +16 min per extra $10,000 of median income, but income alone explains only about 26% of state differences (R² = 0.26). With economic indicators and Critical Access share, R² rises to 0.72.
- **Case study:** Massachusetts waits 85 min longer than Minnesota. Hospital mix explains part of the gap, but MA is still slower at every ER size.

## Recommendations

1. Add capacity and fast-track care at the slowest very-high-volume ERs.
2. Review the 15 "richer & slower" states.

## Limits

- These are associations, not proof of cause.
- Staffing and bed data are not in our datasets.
- The "116,000 more patients seen" estimate assumes 142 very-high-volume ERs, 60,000 visits per ER per year, and a 1.37-point drop in leave rate.

## How to Run

1. Clone this repo.
2. Install the requirements (e.g. `pandas`, `numpy`, `matplotlib`, `plotly`, `scikit-learn`, `jupyter`).
3. Place the source data files in the project folder (see Data above).
4. Open the notebook:
   ```bash
   jupyter notebook A04-What-Drives-ER-Wait-Times_-_Final.ipynb
   ```
5. Run all cells.

## Authors

BA780 · Cohort A · Team 4
