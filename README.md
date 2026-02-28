# Flight Price Prediction - EDA & Analysis 🛫💰

**Author**: Megha Kallapur  
**Location**: Karnataka, India  
**[GitHub](https://github.com/Megha-B-K)** 
---

## Project Overview

Comprehensive **Exploratory Data Analysis (EDA)** of **10,683 flight records** to understand Indian aviation pricing patterns. Perfect foundation for ML price prediction models.

**Dataset**: Real flight booking data (2019) with airlines, routes, timings, stops, and prices.

**Key Questions**:
- Which airlines offer best value?
- How do stops/duration affect pricing?
- Peak travel seasons & routes?
- Time-of-day pricing patterns?

---

## Dataset Overview (10,683 Records)

| Feature | Description | Sample |
|---------|-------------|--------|
| **Airline** | IndiGo, Jet Airways, Air India, etc. | IndiGo (most frequent) |
| **Source** | Departure cities | Banglore, Kolkata, Delhi |
| **Destination** | Arrival cities | New Delhi, Banglore, Cochin |
| **Total_Stops** | 0, 1, 2+ stops | non-stop = lowest price |
| **Duration** | Flight time (minutes) | Avg: ~9087₹, Max: 79,512₹ [file:36] |
| **Price** | Ticket cost (₹) | Mean: ₹9,087 |

**Price Stats**: ₹1,759 (min) → **₹9,087 (avg)** → ₹79,512 (max)

---

## EDA Analysis Performed

### Data Cleaning Pipeline
```python
# Feature Engineering (from your notebook)
df['Date'] = pd.to_datetime(df['Date_of_Journey'], format='%d/%m/%Y')
df['Month'], df['Year'] = df['Date'].dt.month, df['Date'].dt.year
df['Departure_Hour'] = pd.to_datetime(df['Dep_Time']).dt.hour
df['Duration_min'] = pd.to_timedelta(df['Duration']).dt.total_seconds() / 60
df['Total_Stops'] = df['Total_Stops'].map({'non-stop': 0, '1 stop
': 1, '2 stops': 2, '3 stops': 3, '4 stops': 4})

## Key Visualizations Created

- **Airline vs Price** (boxplots)
- **Stops vs Price** correlation  
- **Source-Destination** heatmaps
- **Duration-Price** scatter plots
- **Monthly/Seasonal** trends
- **Departure time** patterns




