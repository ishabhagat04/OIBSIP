# Task 5: Sales Prediction Using Python

## Objective
Build a regression model that predicts product sales based on advertising spend across different media channels (TV, Radio, Newspaper).

## Dataset
- Source: Advertising Dataset (`advertising.csv`)
- Features: TV, Radio, Newspaper (advertising spend in thousands of dollars)
- Target: Sales (product sales in thousands of units)
- Total records: 200

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (Linear Regression, Random Forest Regressor, Polynomial Regression)
- Google Colab

## Key Observations

### 1. Data Overview
- **No null values** in the dataset
- **TV** has the strongest positive correlation with Sales (0.78)
- **Radio** has moderate positive correlation with Sales (0.58)
- **Newspaper** has the weakest correlation with Sales (0.23)

### 2. Exploratory Data Analysis
- **Sales vs TV**: Strong positive linear relationship
- **Sales vs Radio**: Moderate positive relationship
- **Sales vs Newspaper**: Weak/No clear relationship
- **Pairplot**: Shows distribution and relationships between all variables

### 3. Correlation Matrix

| Feature | Correlation with Sales |
|:---|:---|
| TV | 0.78 |
| Radio | 0.58 |
| Newspaper | 0.23 |

### 4. Model Performance Comparison

| Model | MAE | RMSE | R² Score |
|:---|:---|:---|:---|
| Linear Regression | 1.5116 | 1.8500 | 0.9059 |
| Random Forest | 0.8691 | 1.2214 | 0.9590 |
| Polynomial Regression (degree 2) | 1.4686 | 1.8386 | 0.9071 |

**Best Model**: Random Forest Regressor with R² = 0.9590

### 5. Which Advertising Channel Has the Highest Impact on Sales?

**TV** has the highest impact on sales based on both:
- **Linear Regression coefficients**: TV has the highest coefficient (3.56)
- **Random Forest feature importance**: TV is the most important feature (0.63)

### 6. Business Insights
1. **TV advertising** has the strongest relationship with sales
2. **Radio** also contributes positively to sales
3. **Newspaper** has the least impact on sales
4. Companies should allocate more budget to **TV advertising**
5. Newspaper advertising may not provide good ROI

### 7. Residual Analysis
- **Mean of residuals**: Near zero (good model fit)
- **Residuals appear randomly distributed**: No systematic bias
- **Model is well-fitted** for prediction

## How to Run

1. Open the notebook in Google Colab:
   - Go to [Google Colab](https://colab.research.google.com/)
   - Click on **File** → **Upload Notebook**
   - Upload `Task5_Sales_Prediction.ipynb`

2. Or open it directly from GitHub:
   - Go to your GitHub repository
   - Click on `Task5_Sales_Prediction.ipynb`
   - Click the **"Open in Colab"** button

3. Upload the dataset:
   - The notebook will prompt you to upload `advertising.csv`
   - Download from [Kaggle - Advertising Dataset](https://www.kaggle.com/datasets/ashydv/advertising-dataset)

4. Run all cells:
   - Click **Runtime** → **Run all**

## Files Included
- `Task5_Sales_Prediction.ipynb` - Main Jupyter Notebook with complete analysis
- `README.md` - Project documentation

## Results Summary
- ✅ Data loading and EDA completed (null check, descriptive statistics, pairplot)
- ✅ Individual scatter plots for Sales vs each channel
- ✅ Correlation matrix heatmap
- ✅ Train/test split completed
- ✅ 3 models trained (Linear Regression, Random Forest, Polynomial Regression)
- ✅ Models evaluated using MAE, RMSE, R² score
- ✅ Best model: Random Forest (R² = 0.9590)
- ✅ Residual plot for best model
- ✅ Interpretation: TV has highest impact on sales
- ✅ Clean, well-commented Jupyter Notebook