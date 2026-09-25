# STAT 011 Final Project — Bike Sharing Demand Analysis

Statistical analysis of hourly bike rental demand using the UCI Bike
Sharing dataset, examining how time, weather, and calendar effects
relate to rental counts.

**Authors:** Zihui Zhang, Dennis Wu, Jannelly Hwaynate, Sungha Woo

## Data
Hourly bike rental records (`bikes.csv`) with rental counts split into
casual and registered riders, alongside weather (temperature, humidity,
windspeed, weather condition) and calendar features (season, holiday,
working day, weekday, hour).

## Exploratory Analysis
- Distribution of total, casual, and registered rentals
- Rental patterns by hour, weekday, working day, and holiday
- Rental count vs. temperature, humidity, and windspeed
- Correlation matrix across weather variables and rental count

## Statistical Analysis
1. **Simple Linear Regression** — `cnt ~ temp`. Temperature has a
   significant positive effect on rentals (p < 0.05); each 1-unit
   increase in temperature is associated with ~381 more rentals
   (95% CI: 368.49–394.10).
2. **Multiple Linear Regression** — `cnt ~ temp + season + workingday`.
   Temperature and season are significant predictors; working day is
   not. Residual diagnostics support the linear model assumptions.
3. **Logistic Regression** — predicting high- vs. low-demand days from
   `temp + workingday`. Both predictors are significant; each 1-unit
   increase in temperature multiplies the odds of a high-demand day
   substantially, and working days show higher odds of high demand.

## Tools
R, base R plotting, linear/logistic regression (`lm`, `glm`), `step()`
for backward variable selection

## Files
- `Stats_final_Project_bikes.Rmd` — full analysis
- `bikes.csv` — dataset (UCI Bike Sharing)
