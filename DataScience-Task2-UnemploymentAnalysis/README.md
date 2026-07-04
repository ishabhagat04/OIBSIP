# Task 2: Unemployment Analysis in India

## Objective
Perform exploratory data analysis on unemployment data to uncover regional and temporal trends, with a focus on the impact of the COVID-19 pandemic on unemployment rates in India.

## Dataset
- Source: Kaggle - "Unemployment in India" dataset
- Features: Region, Date, Frequency, Estimated Unemployment Rate (%), Estimated Employed, Estimated Labour Participation Rate (%), Area
- Total records: 768

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook / Google Colab

## Key Observations

### 1. Regional Variation
The unemployment rate shows significant variation across different regions/states. Some states consistently show higher unemployment rates than others:
- **Highest**: Tripura (28.35%), Haryana (26.28%), Jharkhand (20.59%)
- **Lowest**: Meghalaya (4.80%), Odisha (5.66%), Assam (6.43%)

### 2. Seasonal Patterns
Month-wise analysis reveals seasonal patterns in unemployment, with certain months showing higher rates:
- Higher unemployment during certain months
- Lower unemployment during others

### 3. COVID-19 Impact
The Post-COVID period (March 2020 onwards) shows a notable increase in unemployment rate:
- **Pre-COVID average**: 9.51%
- **Post-COVID average**: 17.77%
- **Increase**: 8.26 percentage points

### 4. Rural vs Urban
Rural and urban areas show different unemployment patterns, with one area typically having higher rates.

### 5. Correlation
There is a correlation between unemployment, employment, and labour participation rates, indicating these factors are interconnected.

## How to Run

1. Open the notebook in Google Colab:
   - Go to [Google Colab](https://colab.research.google.com/)
   - Click on **File** → **Upload Notebook**
   - Upload `Task2_Unemployment_Analysis.ipynb`

2. Or open it directly from GitHub:
   - Go to your GitHub repository
   - Click on `Task2_Unemployment_Analysis.ipynb`
   - Click the **"Open in Colab"** button

3. Upload the dataset:
   - The notebook will prompt you to upload `Unemployment_in_India.csv`
   - Download the dataset from [Kaggle - Unemployment in India](https://www.kaggle.com/datasets/gokulrajkmv/unemployment-in-india)

4. Run all cells:
   - Click **Runtime** → **Run all**

## Files Included
- `Task2_Unemployment_Analysis.ipynb` - Main Jupyter Notebook with complete analysis
- `README.md` - Project documentation

## Results Summary
- ✅ Data cleaning and preprocessing completed
- ✅ Regional analysis completed (28 regions analyzed)
- ✅ Seasonal trends identified
- ✅ COVID-19 impact quantified (+8.26 percentage points)
- ✅ Correlation analysis between key variables
- ✅ Visualizations created: time-series, bar charts, box plots, heatmaps