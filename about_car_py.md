
# 📄 About `car.py`

The `car.py` script is a complete end-to-end machine learning pipeline built to **predict car resale prices** using structured vehicle data. It performs data preprocessing, exploratory data analysis, feature engineering, and model training using both linear and ensemble techniques.

## 🔍 Purpose:
To clean, explore, and model car listing data to accurately predict resale prices using machine learning techniques.

## 🔧 Key Functionalities:

### 📂 Data Loading:
- Loads training and test datasets from Google Colab environment.
- Reads CSVs using Pandas.

### 🧹 Data Preprocessing:
- Drops rows with missing values in key columns (`Mileage`, `Engine`, `Power`, `Seats`).
- Extracts features from composite fields like `Name`, `Mileage`, `Engine`, `Power`, `New_Price`.
- Converts extracted values to numeric types.
- Encodes categorical variables using `pd.get_dummies()`.
- Combines dummy variables with original dataset for training.

### 📊 Data Analysis:
- Visualizations using Seaborn:
  - Distribution plots
  - Box plots
  - Swarm/strip plots
  - Correlation heatmaps
- Feature importance analysis using `ExtraTreesRegressor`.

### 🤖 Model Training:
- **Linear Regression**
- **Random Forest Regressor**
- Train-test split (80/20)
- Prints R² accuracy for training and test sets.

### 📈 Evaluation Metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

### 📊 Accuracy Summary:
- Random Forest:
  - Train Accuracy: ~98.33%
  - Test Accuracy: ~86.84%
- Linear Regression:
  - Train Accuracy: ~71.21%
  - Test Accuracy: ~67.79%

### 🧠 Libraries Used:
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn (metrics, models)

## 📌 Notes:
- Best suited for Colab or Jupyter Notebook environment.
- Replace file paths (`/content/...`) with local paths if running outside Colab.
- Clean feature engineering and robust evaluation built-in.
