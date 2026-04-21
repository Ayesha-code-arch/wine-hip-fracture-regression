# Wine & Hip Fracture Regression Models

## Overview

This project contains two statistical modelling exercises completed as part of a data visualisation assignment. The first analysis investigates factors influencing the quality of red wine. The second analysis develops models to predict the risk of hip fracture using demographic and clinical variables. Both analyses were carried out in **R** and include exploratory data analysis (EDA), model fitting and evaluation.

## Data

* **Wine quality:** The red wine dataset contains 1 599 samples with 11 physicochemical variables (e.g. fixed acidity, pH, sulphates, alcohol) and a quality rating from 0 to 10. The distribution of quality scores is skewed toward the middle: most wines are rated 5–7 with a peak at 6【915501923067724†L14-L94】.
* **Hip fracture:** The hip fracture dataset comprises anonymised patient records with variables such as bone mineral density (BMD), height, medication use and outcome (fracture vs no fracture). BMD is the dominant predictor of fracture risk【915501923067724†L160-L229】.

## Methods

### Wine quality

* Performed exploratory analysis to understand the distribution of quality scores and correlations between predictors. Alcohol content shows a positive correlation with quality, while volatile acidity has a strong negative correlation【915501923067724†L14-L94】.
* Fitted a multiple linear regression model with eight predictors (e.g. alcohol, volatile acidity, sulphates). Model diagnostics (residual plots, Q–Q plots) indicated acceptable fit.
* Calculated the coefficient of determination (R² ≈ 0.322) indicating that the model explains about one‑third of the variability in quality【915501923067724†L14-L94】.

### Hip fracture prediction

* Built a logistic regression model using bone mineral density alone to predict fracture risk; this yielded an area under the ROC curve (AUC) of ~0.909【915501923067724†L160-L229】.
* Added height and medication variables to the model. The extended model improved the AUC to ~0.926, suggesting moderate added predictive value【915501923067724†L160-L229】.
* Assessed model performance using confusion matrices, ROC curves and calibration plots.

## Results

* **Wine quality:** Alcohol and sulphates were positively associated with quality; volatile acidity was negatively associated. The fitted model achieved R² ≈ 0.322【915501923067724†L14-L94】, indicating moderate explanatory power. Residual analysis suggested no severe violations of linear regression assumptions.
* **Hip fracture:** BMD was the strongest predictor of fracture risk. The logistic model using BMD alone achieved AUC ≈ 0.909【915501923067724†L160-L229】. Including height and medication increased the AUC to ≈ 0.926, indicating improved discrimination【915501923067724†L160-L229】.

## Repository structure

- `DataVisualisation_Assign2.pdf` — assignment report containing full analysis, tables, figures and R code.
- `README.md` — this overview file.
- (Optional) `scripts/` — a folder where you can add your R scripts to reproduce the analysis.

## Usage

1. Download the wine quality and hip fracture datasets from publicly available sources (e.g. UCI Machine Learning Repository for wine data).
2. Install required R packages, such as `tidyverse`, `ggplot2` and `caret`.
3. Run your analysis scripts to recreate the EDA, regression models and figures.

## Licence

This project is licensed under the MIT Licence — see the `LICENSE` file for details.

## Acknowledgements

* The wine quality dataset comes from the UCI Machine Learning Repository.
* The hip fracture dataset is sourced from a health study (anonymised).
* This repository contains reports and scripts from the MSc Data Science assignment.
