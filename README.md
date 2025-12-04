# Gold Price Prediction

## Project Overview
This project aims to build a machine learning model to predict the daily closing price of Gold (GLD) based on various financial indicators. The goal is to assist traders and investors in making informed decisions by providing accurate price forecasts.

## Dataset
The project uses the `gold price dataset.csv`, which contains the following columns:
- **Date**: The date of the record.
- **SPX**: S&P 500 Index.
- **GLD**: Gold Price (Target Variable).
- **USO**: United States Oil Fund.
- **SLV**: Silver Trust.
- **EUR/USD**: Euro to US Dollar exchange rate.

## Libraries Used
The following Python libraries are used in this project:
- `numpy`: For numerical operations.
- `pandas`: For data manipulation and analysis.
- `matplotlib`: For data visualization.
- `seaborn`: For statistical data visualization.
- `sklearn`: For machine learning models and evaluation metrics.
- `xgboost`: For gradient boosting models.

## Methodology

### 1. Data Preprocessing
- Loaded the dataset and inspected its structure.
- Converted the `Date` column to datetime objects.
- Sorted the data by date to ensure chronological order.
- Checked for missing values and duplicates (none were found).

### 2. Exploratory Data Analysis (EDA)
- Generated descriptive statistics to understand the data distribution.
- Analyzed correlations between GLD and other features (SPX, USO, SLV, EUR/USD).
- Visualized data distributions using plots.

### 3. Model Building
- **Model**: Random Forest Regressor.
- **Feature Engineering**: Created lag features for GLD and EUR/USD to capture temporal dependencies.
- **Data Splitting**: Split the data into training and testing sets.
- **Scaling**: Used `StandardScaler` to normalize the features for linear regression.

### 4. Model Evaluation
The model was evaluated using the following metrics:
- **R-squared (R2) Score**: Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables.
- **Mean Absolute Error (MAE)**: The average of the absolute errors.
- **Mean Squared Error (MSE)**: The average of the squared errors.
- **Root Mean Squared Error (RMSE)**: The square root of the mean squared errors.

## Results
The Random Forest Regressor achieved high accuracy on the test set:
- **R2 Score**: ~0.9986
- **MAE**: ~0.4388
- **MSE**: ~0.8087
- **RMSE**: ~0.8993


## How to Run
1. Install the required libraries using `pip install -r requirements.txt`.
2. Place the `gold price dataset.csv` in the project directory.
3. Open and run the `gold_price.ipynb` notebook in a Jupyter environment.
