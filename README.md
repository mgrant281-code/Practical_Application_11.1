# README.ipynb

# What Drives the Price of a Used Car?
### A CRISP-DM Data Science Project Using 426,000 Used Vehicles

## Overview
This project explores what determines the price of a used vehicle using a large dataset of over 426,000 used cars sourced from Kaggle. The goal is to identify the characteristics that most influence resale value and build a reliable pricing model that can support a used-car dealership’s inventory and pricing decisions.

## Repository Contents
vehicles.7z
> - vehicles.csv
- CRISP-DM overview.pdf
**- vehicle_price_analysis.ipynb**
- README.ipynb
- Executive_Summary.pdf
- client_facing_narrative.pdf
- images.7z
> - Folder/images
>> - crisp.png
>> - kurt.jpeg

## 1. Business Understanding
Dealerships need to understand what features make a used car more valuable, which cars are worth acquiring, and how to price vehicles competitively.

## 2. Data Understanding
Includes age, mileage, make, model, trim, body type, drivetrain, condition, and more. Issues: skewed data, missing values, high-cardinality fields, outliers.

## 3. Data Preparation
Steps:
- Cleaning invalid records
- Engineering vehicle age and high-mileage flag
- Log-transforming price
- One-hot encoding categorical variables
- Standardizing numeric fields
- Preprocessing pipeline using scikit-learn

## 4. Modeling
Used a TruncatedSVD + Ridge Regression pipeline:
- Handles high-dimensional sparse data
- Controls overfitting
- GridSearchCV for tuning
- Evaluated with RMSE in log and real price

## 5. Evaluation & Insights
Key findings:
- Age and mileage are strongest predictors
- Brand & model strongly affect value
- SUVs, trucks, AWD/4WD priced higher
- High-mileage thresholds reduce price

## 6. Deployment
Options:
- Batch pricing
- Real-time pricing assistant
- CRM/MIS integration
- Quarterly retraining recommended

## 7. Executive Summary
Consumers value newer, low-mileage vehicles with reliable brands and desirable drivetrains. Model provides data-driven pricing guidance for purchasing and trade-in strategy.

## 8. How to Run
pip install numpy pandas scikit-learn matplotlib
Place dataset and run vehicle_price_analysis.ipynb

## 9. References
Reference appendix included in notebook.
