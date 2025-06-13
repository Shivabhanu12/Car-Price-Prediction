
# 🚗 Car Resale Price Prediction

This project focuses on building a machine learning model to predict the resale price of used cars based on various features such as location, fuel type, transmission, engine size, mileage, and more.

## 📁 Dataset

The datasets used include:
- `Project_train-data.csv` – Contains historical listings of used cars with price and feature details.
- `Project_test-data.csv` – Contains similar listings without price, used for predictions.

These are loaded via Google Colab:
```python
from google.colab import drive
drive.mount('/content/drive')
```

## 🧼 Data Preprocessing

Key preprocessing steps:
- Removed null values from critical fields (Mileage, Power, Engine, Seats)
- Extracted and converted units from `Mileage`, `Power`, `Engine`
- Converted `Owner_Type`, `Fuel_Type`, and other categoricals using one-hot encoding
- Dropped unnecessary columns like `Name`, `New_Price`, `Company` after transformation

## 📊 Exploratory Data Analysis

Visualization and analysis include:
- Price distribution by `Fuel_Type`, `Owner_Type`, `Location`, `Company`, `Year`
- Feature importance using `ExtraTreesRegressor`
- Correlation heatmaps for numerical insight

## 🧠 Model Building

Trained two machine learning models:
- **Linear Regression**
- **Random Forest Regressor**

Split training data using `train_test_split()` and evaluated on:
- Training Accuracy
- Testing Accuracy
- R² Score
- MAE, MSE, RMSE

## 📈 Performance Summary

| Model                | Train Accuracy | Test Accuracy |
|---------------------|----------------|---------------|
| Random Forest        | ~98.33%        | ~86.84%       |
| Linear Regression    | ~71.21%        | ~67.79%       |

## 📊 Evaluation Metrics

```text
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score
```

## 🛠️ Requirements

```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```

## 📬 Author

**Konde Shiva Bhanu**  
B.Tech CSE (Data Science), SR University  
Project developed at NIT Warangal (Internship)

