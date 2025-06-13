🚗 Car Resale Price Prediction
This project focuses on building a machine learning model to predict the resale price of used cars based on various features such as location, fuel type, transmission, engine size, mileage, and more.

📁 Dataset
The datasets used include:

Project_train-data.csv – Historical listings of used cars with price and feature details.

Project_test-data.csv – Similar listings without price, used for prediction.

These are loaded from Google Drive in a Colab notebook:

python
Copy
Edit
from google.colab import drive
drive.mount('/content/drive')
🧼 Data Preprocessing
Removed null values from key fields (Mileage, Power, Engine, Seats)

Extracted numeric values from:

Mileage (kmpl/kmpkg)

Power (bhp)

Engine (CC)

Converted Fuel_Type, Owner_Type, Transmission, etc. using one-hot encoding

Dropped redundant fields (Name, New_Price, Company)

📊 Exploratory Data Analysis
Distribution plots: Prices by fuel type, year, location, and ownership

Box plots: Visual comparisons of categories

Correlation heatmap: Identify relationships between variables

Feature importance: Using ExtraTreesRegressor

🧠 Model Building
Two machine learning models were trained:

Linear Regression

Random Forest Regressor

Data was split using train_test_split() and evaluated on:

R² Score

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

📈 Performance Summary
Model	Train Accuracy	Test Accuracy
Random Forest	~98.33%	~86.84%
Linear Regression	~71.21%	~67.79%

📊 Evaluation Metrics
Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

R² Score

🛠️ Requirements
bash
Copy
Edit
pip install pandas numpy seaborn matplotlib scikit-learn
📬 Author
Konde Shiva Bhanu
B.Tech CSE (Data Science), SR University
Project developed during Internship at NIT Warangal

