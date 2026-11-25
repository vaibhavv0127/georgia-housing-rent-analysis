# Georgia Housing Affordability Analysis

This project examines county-level rent and housing affordability across Georgia using U.S. Census American Community Survey DP03 and DP04 data.

## Research question

How are median gross rent levels across Georgia counties associated with median household income, poverty, and rental vacancy? How does renter cost burden vary across counties?

## Project files

- `GeorgiaHousingProject.ipynb` — data preparation, exploration, regression analysis, affordability measures, and diagnostics
- `DP03_EconomicCharacteristics.csv` — income and poverty data
- `DP04_HousingCharacteristics.csv` — rent, vacancy, and renter cost-burden data
- `requirements.txt` — Python packages used by the notebook

## Analysis

The notebook cleans the Census tables and combines their county-level estimates. It explores county rent and income patterns, then estimates rent models using income, poverty, and rental vacancy. It compares models on the same complete set of counties and examines robust standard errors, predictor overlap, nonlinear terms, residuals, and influential counties.

The affordability analysis calculates the share of renter households spending at least 30% of income on rent from the DP04 cost-burden categories. It compares that measure with a median-based rent-to-income ratio and estimates both unweighted and renter-household-weighted models.

## Run the notebook

Open Terminal in the project folder and run:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Open `GeorgiaHousingProject.ipynb` and run the cells from top to bottom. Keep both CSV files in the same project folder as the notebook.

The notebook saves model-comparison tables and the cleaned county data in the `results/` folder.

## Interpretation and limitations

The models describe associations among county-level estimates; they do not establish that one factor causes another. County averages can mask differences between households. The median-based rent-to-income ratio is a rough county comparison and is not the same as the DP04 renter cost-burden measure. The analysis does not incorporate ACS margins of error.
