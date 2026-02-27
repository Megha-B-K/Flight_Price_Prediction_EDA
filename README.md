# Flight Price Prediction - Exploratory Data Analysis (EDA)

**Author: Megha Kallapur**
  Bengaluru, India  
  meghakallapur22@gmail.com | GitHub : https://github.com/Megha-B-K

## Overview
Performed comprehensive EDA on a dataset of **10,683 Indian domestic flights** to uncover patterns in ticket prices influenced by airlines, stops, timings, and routes. Average price: **₹9,087** (std: ₹4,611); prices range from **₹1,759 to ₹79,512**. Prepared data for potential ML modeling like price prediction.

** Key Insights**:
- Jet Airways flights often premium-priced
- Multi-stop routes (2+ stops) correlate with higher costs  
- Non-stop Bangalore-Delhi flights are budget-friendly

## Dataset
- **Source**: `flight_price.xlsx` (11 columns: Airline, Date_of_Journey, Source, Destination, Route, Dep_Time, Arrival_Time, Duration, Total_Stops, Additional_Info, Price)
- **Size**: 10,683 rows
- **Missing Values**: Minimal (Route/Total_Stops: 1 each ~0.01%)
- **Features Engineered**: Date/Month/Year, Dep/Arrival Hour/Min, Duration (minutes)

## Tech Stack
- **Languages/Tools**: Python, Pandas, NumPy, Matplotlib, Seaborn
- **Environment**: Jupyter Notebook

## EDA Process
1. **Data Loading & Inspection**: Loaded Excel; checked shape, info, head/tail, nulls via `df.isnull().sum()`
2. **Cleaning**: Handled minimal nulls; dropped redundant columns (e.g., original times)
3. **Feature Engineering**:
   - Split Date_of_Journey → Date/Month/Year (int)
   - Parsed Dep/Arrival_Time → Hour/Min (int)
   - Duration → Hours/Mins → Total minutes
4. **Analysis**:
   - Descriptive stats: `df.describe()` for Price distribution
   - Visualizations: Distributions, correlations (implied via code)
5. **Insights**: Higher stops/duration → higher price; airline-specific trends

## Repository Structure
Flight-Price-Prediction/
├── Flight-Price-Prediction.ipynb # Main EDA notebook
├── price.xlsx # Dataset
├── requirements.txt # Dependencies
├── README.md # This file

## Skills Demonstrated
- Exploratory Data Analysis (EDA)
- Data Cleaning & Preprocessing
- Feature Engineering (temporal features)
- Statistical Analysis
- Data Visualization Setup

