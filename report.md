# Titanic Dataset: Cleaning & Exploratory Data Analysis Report

## 1. Project Objective
The objective of this project was to take a raw, messy dataset of Titanic passengers, perform standard professional data cleaning pipelines, analyze underlying survival patterns, and generate high-impact visual assets.

## 2. Data Preprocessing & Cleaning Pipeline
To ensure the integrity of the analysis, the following structural data cleaning steps were performed:
* **Duplicate Handling:** Scanned the dataset and safely eliminated redundant records.
* **Irrelevant Feature Drop:** Dropped the `Cabin` column entirely, as over 70% of its data points were missing, making imputation statistically irresponsible.
* **Missing Value Imputation:** 
  * Filled missing values in `Age` using the column **median** (28.0) to prevent skewness from extreme age values.
  * Filled missing values in `Embarked` using the **mode** ("S"), assigning passengers to the most frequent port of entry.
* **Outlier Mitigation:** Applied the **Interquartile Range (IQR)** method to the highly skewed `Fare` column, establishing strict upper boundaries to filter out extreme premium fares and normalize the core passenger distribution.

## 3. Executive Insights & Key Findings
* **The Gender Survival Gap:** While males made up the vast majority of the passenger manifest, female passengers experienced a drastically higher survival rate. This visually confirms the historical maritime protocol of "women and children first."
* **Socioeconomic Impact (Class):** Third-class (`Pclass = 3`) passengers suffered the absolute highest number of casualties. Socioeconomic standing directly correlated with proximity to lifeboats and survival probability.
* **Demographic Concentration:** The passenger population was heavily concentrated with young adults, peaking significantly between the ages of 20 and 35.

## 4. Visualized Assets
The following visual matrices were generated and exported to the `/visualizations` directory:
1. `baseline_distributions.png` — Showcases overall survival counts alongside gender volumes.
2. `survival_insights.png` — Illustrates the deep dive of survival rates cross-referenced by gender and ticket tier.
3. `age_and_correlation.png` — Provides the continuous age spectrum distribution and a statistical feature correlation heatmap.

## 5. Conclusion
By engineering a clean data pipeline and eliminating statistical noise (missing data and extreme outliers), we translated raw tables into structural historical insights. This baseline dataset is now fully optimized and ready for predictive Machine Learning modeling.