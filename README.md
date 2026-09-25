# Python for Data Science Notebooks

Three 3-hour sessions introducing Python for data analysis. Each session ships as a paired **exercises** notebook
(with `TODO`s and self-checking `assert` cells).

## Structure

```
session1-python-fundamentals/
  session1_exercises.ipynb

session2-numpy-pandas-seaborn/
  session2_exercises.ipynb
  olist_orders.csv
  olist_order_items.csv
  olist_products.csv
  product_category_translation.csv
  brl_eur_rates.csv

session3-scipy-statistics/
  session3_exercises.ipynb
  diabetes.csv
  olist_orders.csv
  olist_order_items.csv
  olist_products.csv
  product_category_translation.csv
  brl_eur_rates.csv
```

## Session overview

**Session 1 — Python fundamentals.** Idioms and comprehensions, functions, file I/O, error
handling, a first OOP pass, and querying two real, free, no-key APIs (the World Bank API and
Frankfurter for exchange rates). Requires internet access for the API section only. Ends with a
first version of an `EDAReport` class built around a plain list of dicts.

**Session 2 — NumPy / Pandas / Seaborn.** Built entirely around real data: actual orders from
Olist, a Brazilian e-commerce marketplace (Sep 2016–Oct 2018), split across several files the way
real company data usually is, plus real historical BRL→EUR exchange rates. Students merge the
files themselves, clean it, and rebuild `EDAReport` around a DataFrame, adding
`plot_distributions`, `correlation_heatmap`, and `detect_outliers`.

**Session 3 — SciPy.** Distribution fitting, hypothesis testing, and correlation, taught on the
Pima Indians Diabetes dataset (a clean, well-known real dataset chosen for the statistics
specifically). The final two sections return to the Olist data from Session 2 to finish
`EDAReport` with `test_normality`, `compare_groups`, `correlation_significance`, and an exportable
`generate_report()`, closing with an open-ended mini-project.

## Data sources

- **Olist Brazilian E-Commerce dataset** — [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **BRL→EUR exchange rates** — real historical monthly rates from the [Frankfurter API](https://www.frankfurter.dev/) (ECB data)
- **Pima Indians Diabetes Dataset** — 768 anonymized patient records (CC0)

## Running the notebooks

```
session1-python-fundamentals/
session2-numpy-pandas-seaborn/
session3-scipy-statistics/
README.md
requirements.txt
environment.yml
```

Set up the environment with either:

**pip**
```
pip install -r requirements.txt
```

**conda**
```
conda env create -f environment.yml
conda activate ds-course
```

Both install the same stack: `numpy`, `pandas`, `matplotlib`, `seaborn`, `scipy`, `requests`, plus
`jupyter`/`ipykernel` to run the notebooks. Session 1's API exercises need internet access;
everything else runs offline once each session's data files are in place.
