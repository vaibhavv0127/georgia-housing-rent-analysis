# Georgia County Rent and Affordability Analysis

This notebook keeps the original workflow visible while correcting errors and extending the analysis.

## Project files

- `GeorgiaHousingProject_Sectioned.ipynb` — notebook with 48 original code cells in order, targeted fixes, and 14 added analysis cells
- `DP03_EconomicCharacteristics.csv` — Census economic profile table
- `DP04_HousingCharacteristics.csv` — Census housing profile table
- `requirements.txt` — required Python packages
- `figures/` and `results/` — output folders for generated files

## Notebook organization

The notebook has six broad sections: prepare county data; explore the original rent and income measures; run the original regression models; add rent burden and compare rent models; check model reliability; and model affordability and conclude.

The original summaries, rankings, scatterplots, and model steps remain in place. Seven original cells have targeted corrections for Census row selection, county-name cleanup, merges, and plot-line ordering. Fourteen new analysis cells add renter burden, comparable complete-case regression models, robust standard errors, VIF, shape and interaction checks, residual diagnostics, influential-county sensitivity, weighted regression, and saved results.

## Run it

Open Terminal in this folder and run:

1. `python3 -m venv .venv`
2. `source .venv/bin/activate`
3. `pip install -r requirements.txt`
4. `jupyter notebook`

Open `GeorgiaHousingProject_Sectioned.ipynb` and run the cells from top to bottom. Start Jupyter from this project folder so it can find the two CSV files.

## Interpretation notes

The rent-burden outcome is the DP04 share of renter households spending at least 30% of income on rent. The annual median-rent divided by median-income ratio is retained as a rough county comparison, not as an individual household burden rate.

The models describe county-level associations; they do not establish causation or describe individual households. ACS margins of error are not included.
