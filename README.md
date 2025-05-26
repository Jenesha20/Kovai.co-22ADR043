# Public Transport Passenger Journeys Analysis and Forecasting

## Overview
This project analyzes daily public transport passenger journeys by service type using historical data. It provides key insights into usage patterns, external impacts such as the COVID-19 pandemic, seasonal variations, and service-specific dynamics. Additionally, it leverages the **Prophet forecasting model** to predict short-term passenger demand, helping guide operational planning and resource allocation.

---

## Dataset
The dataset contains daily passenger journey counts for multiple service types:
- **Local Route**
- **Light Rail**
- **Peak Service**
- **Rapid Route**
- **School Service**

Data spans several years including **pre-pandemic**, **pandemic**, and **post-pandemic** periods.

---

## Key Insights

### 📈 Seasonal Trends in Public Transport Usage
Passenger numbers vary significantly by season, with higher usage during school terms and notable drops during holiday periods like December and January.

**Evidence:**  
- On **28/12/2021**, "School" journeys were **0**.  
- On **01/03/2023**, they surged to **5,544**.

---

### 🦠 Impact of COVID-19 on Transport Demand
A sharp decline in passenger numbers occurred during 2020 and early 2021 due to pandemic restrictions, particularly affecting "Light Rail" and "Peak Service."

**Evidence:**  
- On **20/04/2020**, "Local Route" dropped to **379** passengers.  
- "Peak Service" was **0** compared to pre-pandemic averages over **10,000**.

---

### 🕑 Peak vs. Off-Peak Service Disparity
"Peak Service" usage is highly volatile, often dropping to zero on weekends or non-school days, while "Rapid Route" and "Local Route" maintain more stable daily counts.

**Evidence:**  
- On **11/09/2021** (weekend), "Peak Service" was **0**.  
- "Local Route" still recorded **820** journeys.

---

### 🚈 Growth in Light Rail Popularity
Post-2021, "Light Rail" usage shows strong recovery and growth, indicating increased adoption or service expansion.

**Evidence:**  
- Passenger counts rose from **2,352** on **28/12/2021** to **12,226** on **07/03/2024** — a **fivefold increase**.

---

### ❗ Anomalies and Special Events
Certain dates show near-zero usage across all services, likely due to public holidays or disruptions. Some dates show spikes possibly linked to special events or promotions.

**Evidence:**  
- On **29/09/2024**, "Local Route" dropped to **1** passenger.  
- On **24/07/2019**, it peaked at **19,380**.

---

### 🎒 School Service Dependency
The "School" service shows highly predictable dependency on school term dates, with consistent zero counts during breaks and spikes during terms.

**Evidence:**  
- Zero counts consistently in **December/January**.  
- Spikes like **5,544** passengers on **01/03/2023**.

---

## Forecasting Approach

### 🔮 Forecasting with Prophet

The project uses **Facebook Prophet**, a powerful open-source time series forecasting tool developed by Meta, to predict future passenger journeys.

**Key Features Used**:
- **Trend modeling**: Captures non-linear growth.
- **Yearly seasonality**: Accounts for predictable calendar-based trends.
- **Weekly seasonality**: Captures daily usage patterns.
- **Holiday effects**: Can optionally include school holidays or public holidays (custom calendar support).
- **Uncertainty intervals**: Displays confidence bands on forecast plots.


---

## Visualizations Included

* **📊 Pie Chart**: Overall passenger journey distribution by service type.
* **📉 Bar Chart**: Average daily passengers per service type.
* **📈 Line & Confidence Interval Plot**: Actual vs forecasted passenger counts over time.
* **🔮 Forecast Bar Chart**: Predicted passenger counts for the next 7 days per service.

---

## How to Run

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Jenesha20/Kovai.co-22ADR043.git
   cd public-transport-forecasting
   ```

2. **Install dependencies**:

   ```bash
   pip install pandas matplotlib seaborn prophet
   ```

3. **Place the dataset**
   `Daily_Public_Transport_Passenger_Journeys_by_Service_Type_20250526.csv`
   in the project directory.


---

## Conclusion

The analysis reveals strong **seasonal patterns**, **pandemic impact**, **service-specific usage volatility**, and **growth trends in light rail usage**. Combined with forecasting, these insights support **data-driven decision-making** for resource allocation, scheduling, and promotional planning in public transport systems.



