# Rossman store sales prediction

## Background

Rossmann, established in 1972, stands as Germany's largest grocery store chain, extending its presence across over 3000 stores in 7 European countries. The company periodically launches short-term and continuous promotions to boost sales. Moreover, sales figures are influenced by various factors including promotions, competition, school and state holidays, as well as seasonality and cyclicality.

## Data Presentation

The dataset encompasses sales data from 1115 Rossmann chain stores, totaling 1017209 entries (spanning 27 characteristics) from January 1, 2013, to July 2015, distributed across four files:

- `train.csv`: Historical data featuring sales volumes.
- `test.csv`: Historical data excluding sales figures.
- `sample_submission.csv`: A sample submission file in the correct format.
- `store.csv`: Additional information pertaining to each store.

### train.csv

Contains 9 columns of data:

- `Store`: ID number of the store.
- `DayOfWeek`: Number of the weekday.
- `Date`: Date of sales data.
- `Sales`: Historical sales data.
- `Customers`: Number of customers.
- `Open`: Indicates if the store was open.
- `Promo`: Indicates if there was a promotion.
- `StateHoliday` & `SchoolHoliday`: Indicate state and school holidays, respectively.

### test.csv

Similar to `train.csv` but lacks `Sales` and `Customers` data. The objective is to predict the missing `Sales` data.

### sample_submission.csv

Contains `Id` and `Sales` columns, serving as a template for submitting predictions to Kaggle.

### store.csv

Provides details on store IDs including location and promotional information, with fields like `StoreType`, `Assortment`, `CompetitionDistance`, `CompetitionOpenSince[Year/Month]`, `Promo2`, `Promo2Since[Year/Week]`, and `PromoInterval`.

## Project Objectives

The goal is to forecast sales using historical data from `train.csv` for supervised learning, enhancing model accuracy with additional information from `store.csv`, and submitting predictions in the `sample_submission.csv` format for Kaggle evaluation.

## Evaluation Criteria

Kaggle recommends using the Root Mean Square Percentage Error (RMSPE) for model evaluation, focusing on minimizing this value to enhance score accuracy.

## Project Process

### Step 1: Loading Data

Analyze loaded data for initial insights, using `DataFrame.info()` to examine distributions and missing values.

### Step 2: EDA (Exploratory Data Analysis)

Utilize tools like Pandas, Matplotlib, and Seaborn for data visualization and understanding, employing various plot types for in-depth analysis.

### Step 3: Data Pre-processing

Address missing values through removal, filling, or marking strategies to prepare data for modeling.

### Step 4: Feature Engineering

Extract time-related features and convert categorical data into numerical formats for model readiness.

### Step 5: Benchmark Model and Evaluation

Implement a regression tree model as a baseline, using SKLearn's `DecisionTreeRegressor` with K-fold cross-validation and grid search for hyperparameter tuning.

### Step 6: XGBoost Modeling

Fine-tune XGBoost model parameters such as `eta`, `max_depth`, `subsample`, `colsample_bytree`, and `num_trees` for optimal performance.


