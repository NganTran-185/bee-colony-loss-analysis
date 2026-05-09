
# 🐝 Honey Bee Colony Loss Analyser
Analysing USDA honey bee colony loss rates across US states using stressor correlation, regression modelling, and seasonal trend analysis — Python + pandas + scikit-learn + plotly.

## Overview
This project investigates why US honey bee colonies are dying and which factors best predict colony loss rates. Using USDA NASS survey data covering all 50 US states from 2015 to 2021, the analysis explores seasonal patterns, regional differences, stressor
correlations, and builds a machine learning model to predict colony loss rate.

## Research Questions

1. Which US states consistently lose the most bee colonies?
2. Is colony loss getting worse over time nationally?
3. What stressors (varroa mites, pesticides, disease) correlate most strongly with loss rates?
4. Are there seasonal patterns — do bees die more in winter?
5. Can we predict colony loss rate from stressor levels?

## Dataset: 
Source: USDA National Agricultural Statistics Service (NASS)
Files:
1. NASS_Bee-Colony_2015-2021.csv — quarterly colony counts and loss rates per US state
2. NASS_Bee-Stressors_2015-2021.csv — percentage of colonies affected by each stressor type per state and quarter
Coverage: All 50 US states, quarterly (Q1–Q4), 2015–2021
Download: Search "USDA Honey Bee Colony" on Kaggle
https://www.kaggle.com/datasets/kyleahmurphy/us-bee-colony-2015-2022


Note: CSV files are included in this repo. 

## Key Findings
1. Varroa mites are the strongest predictor of colony loss. Consistent with published beekeeping research worldwide.
2. Winter is the most dangerous season for bees
Q1 (January–March) consistently shows the highest colony loss rates across all regions and years. Cold temperatures, food scarcity, and accumulated varroa mite loads over winter are the likely drivers.

## Model Results
An R² of 0.46 means the model explains 23.4% of colony loss
variance. The remaining 46% is likely driven by unmeasured
factors: beekeeper management practices, local climate, and
hive genetics.

## Project Structure
bee-colony-loss-analysis/
  Bees.ipynb     Complete analysis notebook (all 5 days)
  README.md      This file
  .gitignore     Excludes CSV files and local outputs
The full analysis — data loading, cleaning, visualisation,
correlation analysis, and modelling — is in a single notebook
Bees.ipynb. Click it on GitHub to view all cells and outputs
without downloading anything.

## How to Run
1. Clone the repo
bashgit clone https://github.com/NganTran-185/bee-colony-loss-analysis.git
cd bee-colony-loss-analysis
2. Install dependencies
bashpip install pandas numpy matplotlib seaborn scipy scikit-learn plotly pymannkendall jupyter ipykernel
3. Download the dataset
Place both files in the project folder.
4. Open the notebook
bashjupyter notebook Bees.ipynb
Or open in VS Code and select your Python environment as the kernel.
5. Run all cells top to bottom
Each day's section is marked with a markdown heading. Run them
in order — each day saves output that the next day loads.


## Interactive Map
The US choropleth map (day5_us_map.html) is generated locally by running Cell 3 in Day 5 of the notebook. GitHub cannot render HTML files of this size — run the notebook to generate it, then open the file in any browser to explore the interactive map.

## Limitations
1. USDA stressor percentages are beekeeper estimates, not precise measurements — survey noise reduces model signal
2. The model under-predicts extreme loss events (30%+) due to limited training examples at the high end
3. Unmeasured factors (weather, beekeeper skill, local flora)likely explain the majority of remaining variance
4. Data covers 2015–2021 only — longer time series would improve trend detection and forecasting reliability

## Author
Ngan Tran
github.com/NganTran-185

