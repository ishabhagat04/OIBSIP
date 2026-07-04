# Task 3: Car Price Prediction with Machine Learning

## Objective
Build a regression model that predicts the selling price of a used car based on features such as brand, age, mileage, fuel type, and transmission.

## Dataset
- Source: Kaggle - "Vehicle dataset from cardekho"
- Features: Name, Year, Selling_Price, KM_Driven, Fuel, Seller_Type, Transmission, Owner
- Total records: 4,340

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (Linear Regression, Random Forest Regressor)
- Google Colab

## Key Observations

### 1. Data Preprocessing
- **Null values**: None found in the dataset
- **Feature engineering**: 
  - Created `car_age` feature (2026 - year)
  - Extracted `brand` from car name

### 2. Exploratory Data Analysis
- **Selling Price Distribution**: Right-skewed (most cars priced lower)
- **Price vs Fuel Type**: Diesel cars have higher average prices
- **Price vs Car Age**: Older cars have lower selling prices
- **Price vs Transmission**: Automatic cars have higher prices

### 3. Feature Importance (Random Forest)
Top 5 most important features:
1. **Transmission_Manual** (29.4%)
2. **KM_Driven** (13.6%)
3. **Fuel_Diesel** (10.1%)
4. **Car_Age** (9.8%)
5. **Year** (9.5%)

### 4. Model Performance Comparison

| Model | MAE | RMSE | R² Score |
|:---|:---|:---|:---|
| Linear Regression | 185,499.61 | 379,425.16 | 0.5283 |
| Random Forest | 117,147.84 | 272,649.98 | 0.7564 |

**Best Model**: Random Forest Regressor (R² = 0.7564)

### 5. Business Insights
- **Car age** has the highest impact on selling price
- **Year of manufacture** is a crucial factor
- **KM driven** significantly affects the price
- **Fuel type** (Diesel > Petrol) impacts the price
- **Transmission type** (Automatic > Manual) matters
- **Brand reputation** affects resale value

## How to Run

1. Open the notebook in Google Colab:
   - Go to [Google Colab](https://colab.research.google.com/)
   - Click on **File** → **Upload Notebook**
   - Upload `Task3_Car_Price_Prediction.ipynb`

2. Or open it directly from GitHub:
   - Go to your GitHub repository
   - Click on `Task3_Car_Price_Prediction.ipynb`
   - Click the **"Open in Colab"** button

3. Upload the dataset:
   - The notebook will prompt you to upload the car dataset
   - Download the dataset from [Kaggle - Car Price Prediction Dataset](https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho)

4. Run all cells:
   - Click **Runtime** → **Run all**

## Files Included
- `Task3_Car_Price_Prediction.ipynb` - Main Jupyter Notebook with complete analysis
- `README.md` - Project documentation

## Results Summary
- ✅ Data cleaning and preprocessing completed
- ✅ Feature engineering completed (car_age, brand)
- ✅ EDA visualizations created
- ✅ Two models trained (Linear Regression, Random Forest)
- ✅ Random Forest achieved R² = 0.7564
- ✅ Feature importance analysis completed
- ✅ Residual analysis completed