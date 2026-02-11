# Wrangling and EDA

This repo contains my work for **A Data Wrangling EDA**.  
The goal of this assignment was to practice cleaning messy variables, defining observations/variables, and doing basic exploratory data analysis (EDA) with tables and plots.

---

## Files

- `assignment1.ipynb` (or your notebook name)  
  Main notebook containing all answers, code, plots, and written explanations.

- `q6_work.pdf` / `q6_work.jpg` (optional, if included)  
  Handwritten derivations for Q6 (linear transformations of mean/covariance/variance/median/IQR).

---

## Data

All datasets are stored in the `data/` (or `scratchpad/data/`) folder:

- `airbnb_NYC.csv`
- `mn_police_use_of_force.csv`
- `metabric.csv`
- `GSAF5.xls` (shark attack dataset)
- `ForeignGifts_edu.csv`
- `college_completion.csv`
- `ames_prices.csv`

Note: Some CSVs are not UTF-8, so I load them with `encoding="latin1"`.

---

## Questions Completed

### Q1 — Cleaning common variable issues
- cleaned a numeric `Price` column (Airbnb) and checked missing values
- cleaned a categorical variable `subject_injury` (MN police use of force), measured missingness, and cross-tabbed with `force_type`
- converted a survival status variable (METABRIC) into a 0/1 dummy variable
- counted missing values in `Review Scores Rating` (Airbnb) and created a median-imputed version, with a note on bias

### Q2 — Shark attack data cleaning and analysis
- loaded the dataset using `pd.read_excel()` (since it is not a CSV)
- removed empty columns
- defined an observation as one shark attack incident (one row)
- cleaned `Year` and analyzed attacks since 1940 over time
- cleaned `Age` and made a histogram
- cleaned `Type` into {Provoked, Unprovoked, Unknown} and computed proportions
- cleaned `Fatal Y/N` into {Y, N, Unknown}
- compared fatality rates by provoked vs unprovoked attacks

### Q3 — Wickham "Tidy Data" short responses
- answered questions based on the abstract and key sections about tidy vs messy data
- summarized definitions of values/variables/observations and why melting is useful

### Q4 — Foreign gifts to U.S. universities
- made a histogram for gift amounts and described distribution
- computed gift type proportions
- found top countries by number of gifts and by total amount
- found top institutions by total amount and plotted distribution
- found top giftors by total amount

### Q5 — College completion EDA
- summarized dataset dimensions and inspected first rows
- cross-tabbed `control` vs `level` and described patterns
- KDE + describe tables for graduation rates overall and by control type
- scatterplot of graduation rate vs aid, plus covariance/correlation overall and by control

### Q6 — Linear transformation properties (handwritten)
- showed how mean/covariance/variance change under linear transformations
- discussed median and IQR under linear transforms (with b > 0)
- gave examples showing nonlinear transforms do not preserve the same mean behavior

### Q7 — Ames housing prices EDA
- KDE + describe for prices overall and by building type
- ECDF and 5-number summary
- boxplots (overall and by building type) and outlier discussion
- created an outlier dummy via IQR rule
- winsorized prices and compared distributions before/after winsorizing

---

## How to Run

1. Install Python packages:
```bash
pip install pandas numpy matplotlib
