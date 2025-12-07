# Dynamic-Pricing-Engine-For-Flight-Booking-and-Revenue-Optimization
An end-to-end machine learning and simulation framework that predicts fares, models price elasticity, simulates inventory-based pricing, and delivers dynamic pricing recommendations through interactive Power BI dashboards

📌 This project demonstrates how airlines can increase revenue by 10–14% and reduce spoilage by 30–40% by integrating:

  1. Machine Learning (LightGBM Regression)
  
  2. Price Elasticity Modeling
  
  3. Inventory-Aware Pricing Simulation
  
  4. Dynamic Pricing Dashboards (Power BI)
  
  5. Competitor Benchmarking
  
  6. Seasonal & Route-Level Insights

📌 1. Project Overview

Airlines today rely on dynamic pricing to balance revenue, demand, competition, and inventory.
This project builds a full pricing engine capable of:

✔️ Predicting fares.
✔️ Modeling the relationship between price and demand.
✔️ Finding optimal price points.
✔️ Adjusting pricing by seats remaining.
✔️ Visualizing performance in Power BI.

The result is a production-ready dynamic pricing decision-support system.

📌 2. Business Problem

Airlines struggle with:

  1. Pricing seats too high → seats go unsold (spoilage).
  
  2. Pricing too low → revenue loss.
  
  3. Not adjusting prices based on booking window or remaining seats.
  
  4. Slow response to competitor fare changes.

This project solves these problems by merging ML forecasting + economic modeling + inventory simulation.

📌3. Features & Capabilities
🔹 ML Fare Prediction Model
    Algorithm: LightGBM Regressor
    Inputs: route, distance, airline, month, seasonality indicators
    Performance: MAE ≈ $13.2
    Predicts average fare for any route under any scenario.
  
🔹 Price Elasticity Engine
Models how demand changes with price:
  Price multipliers tested: 0.8 → 1.2
  Demand response curve
  Revenue optimization curve
  Identifies optimal price (≈ 0.9–1.0 multiplier)
  
🔹 Inventory-Aware Pricing Simulation
  Simulates pricing & demand over booking windows:
  
  ⬆️ Prices increase as seats remaining ↓
  ⬇️ Prices decrease when seats are plentiful
  
  Outputs:
  
  Optimal revenue day
  Revenue heatmaps
  Demand heatmaps
  Booking-window sensitivity insights

🔹 Power BI Dashboards

Three interconnected dashboards:

1️⃣ Historical & Predicted Fare Insights.
2️⃣ Elasticity-Based Pricing Simulator.
3️⃣ Inventory-Based Pricing Simulator.

All dashboards are filterable by:

  Origin
  Destination
  Route
  Airline

📌 4. Data Sources

Dataset includes:
  
  Airline route information.
  Historical fares.
  Distances.
  Airlines.
  Time-series monthly trends.
  Competitor fare benchmarks.

📌 5. Machine Learning Model
📘 Model: LightGBM Regressor

Handles non-linear relationships & seasonal patterns effectively.

Input Features:
  
  Month.
  Distance.
  Airline.
  Origin State.
  Destination State.
  Competitor Average Fare.
  Seasonal Features (e.g., “Summer peak” indicator).

Output:

Predicted average fare in USD.

Performance:
Metric	        Value
MAE	            $13.2
RMSE	          Strong generalization
R²	            Good explanatory power

📌 6. Price Elasticity Modeling

Elasticity curve modeled as linear demand decay with price multipliers:

Price Multiplier	Demand
      0.8          0.50
      0.9          0.35
      1.0          0.30
      1.1          0.20
      1.2          0.10

Results:

Demand decreases smoothly as prices rise.
Revenue peaks near 0.9–1.0 multiplier.
High prices collapse demand → revenue loss.
Low prices increase bookings but reduce per-seat revenue.
Optimal zone: 90%–100% price multiplier.

📌 7. Inventory Simulation

Simulates pricing across:
  
  Booking windows (0–10, 11–20, …, 81–90 days)
  Seat levels (10, 50, 100, 150 seats)

Key findings:
  
  Prices decrease over longer booking windows.
  Remaining seats strongly influence final fare.
  Revenue peaks around mid-window.
  Demand grows toward late windows.

This reduces spoilage significantly.

📌 8. Power BI Dashboards
Dashboard 1: Historical & Predicted Fare Analysis

Includes:
  
  Monthly fare trend.
  Predicted vs actual fares.
  Top routes by fare.
  Airline-level benchmarking.
  Fuel consumption, miles flown, number of airlines.

Dashboard 2: Price Elasticity Simulation

Includes:
  1. Elasticity curve
  2. Revenue optimization curve
  3. Competitor positioning bubble chart
  4. Key KPIs:
     -> Baseline Revenue
     -> Optimal Revenue
     -> Revenue Uplift %

Dashboard 3: Inventory Simulation

Includes:

  Price vs Days (by seats remaining)
  Revenue vs Days (by inventory)
  Revenue heatmap
  Demand heatmap
  Optimal booking day

📌 9. Key Insights
⭐ Revenue can increase by 10–14% with optimized pricing

Supported by:
  
  Elasticity curves.
  Baseline vs optimal revenue KPIs.
  Simulation results.

⭐ Spoilage can drop by 30–40%

Inventory simulation shows:
  
  Earlier bookings stimulated
  Fewer seats remain unsold late-window
  Better price control across cycles

⭐ Seasonality explains predictable price peaks
  
  Apr–Sep: High demand months
  Oct–Dec: Fare troughs

⭐ Competitor fares anchor predicted fare

  Model closely tracks competitor pricing ranges.
