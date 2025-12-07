# Dynamic-Pricing-Engine-For-Flight-Booking-and-Revenue-Optimization
An end-to-end machine learning and simulation framework that predicts fares, models price elasticity, simulates inventory-based pricing, and delivers dynamic pricing recommendations through interactive Power BI dashboards

This project demonstrates how airlines can increase revenue by 10–14% and reduce spoilage by 30–40% by integrating:

1. Machine Learning (LightGBM Regression)

2. Price Elasticity Modeling

3. Inventory-Aware Pricing Simulation

4. Dynamic Pricing Dashboards (Power BI)

5. Competitor Benchmarking

6. Seasonal & Route-Level Insights

1. Project Overview

Airlines today rely on dynamic pricing to balance revenue, demand, competition, and inventory.
This project builds a full pricing engine capable of:

✔️ Predicting fares
✔️ Modeling the relationship between price and demand
✔️ Finding optimal price points
✔️ Adjusting pricing by seats remaining
✔️ Visualizing performance in Power BI

The result is a production-ready dynamic pricing decision-support system.

2. Business Problem

Airlines struggle with:

1. Pricing seats too high → seats go unsold (spoilage).

2. Pricing too low → revenue loss.

3. Not adjusting prices based on booking window or remaining seats.

4. Slow response to competitor fare changes.

This project solves these problems by merging ML forecasting + economic modeling + inventory simulation.

3. Features & Capabilities
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
