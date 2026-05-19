# Egyptian Real Estate Analytics Pipeline

## Overview
This repository contains a data pipeline designed to scrape, process, and engineer real estate data from the Egyptian market. It transforms raw web data into a highly optimized, scalable dataset ready for machine learning predictive models.

## Key Features
* **Automated Data Extraction**: Utilizes Selenium to scrape detailed property listings, including prices, areas, room counts, and amenities from Aqarmap.
* **Advanced Feature Engineering**: Parses raw text to extract geographical data, temporal metrics (e.g., property age, off-plan status), and spatial ratios (e.g., area per room).
* **Robust Preprocessing**: Handles missing values using Random Forest-based Iterative Imputation and applies Target Encoding for high-cardinality categorical variables like city names.
* **Dimensionality Reduction & Selection**: Employs Variance Thresholds, Principal Component Analysis (PCA) for spatial features, and SelectKBest with mutual information regression to isolate the most predictive variables.

https://github.com/user-attachments/assets/fc7b636a-eff0-4927-ab12-89cc3aaf8f07

## Repository Structure
* `aqarmap.ipynb`: The web scraping module using Selenium to gather raw real estate data.
* `preprocessing.ipynb`: The core data processing notebook handling cleaning, EDA, feature engineering, imputation, and feature selection.

## Technologies Used
* **Data Collection**: Python, Selenium
* **Data Processing**: Pandas, NumPy, Category Encoders
* **Machine Learning & Selection**: Scikit-Learn (IterativeImputer, PCA, SelectKBest, RandomForestRegressor)

## Getting Started
1. Clone the repository.
2. Install the required dependencies: 
   ```bash
   pip install pandas numpy selenium scikit-learn category_encoders matplotlib seaborn
   ```
3. Run `aqarmap.ipynb` to generate the raw dataset or donwanload the data from data folder.
4. Execute `preprocessing.ipynb` to clean, engineer, and export the final training and testing datasets (X_train_processed.csv, X_test_processed.csv, etc.).
