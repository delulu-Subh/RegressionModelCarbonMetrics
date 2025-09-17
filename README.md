#RegressionModelCarbonMetrics

📊 Project Overview

RegressionModelCarbonMetrics predicts CO₂ emissions using vehicle fuel consumption and engine data. The project leverages Linear Regression with both numerical and categorical features, providing accurate environmental insights.

Dataset: fuel_consumption_dataset.csv

Features: Engine size, cylinders, fuel consumption, transmission type, fuel type

Target: CO2EMISSIONS (g/km)

🧩 Workflow

Data Preparation

Selected numerical features: ENGINESIZE, CYLINDERS, FUELCONSUMPTION_COMB

Selected categorical features: TRANSMISSION, FUELTYPE

One-hot encoded categorical features

Standardized numerical features for better scaling

Train-Test Split

80% training, 20% testing

Model Training

Applied Linear Regression on combined numerical + encoded categorical features

Model coefficients reveal feature contributions to CO₂ emissions

Evaluation

Metrics calculated on the test set:

MAE: 3.27 g/km

MSE: 24.81 g²/km²

RMSE: 4.98 g/km

R² Score: 0.994 — extremely accurate prediction

Visualization

Scatter plot comparing actual vs predicted CO₂ emissions:

plt.figure(figsize=(8,6))
plt.scatter(y_test, y_pred, color='darkcyan', alpha=0.7)
plt.plot([y.min(), y.max()], [y.min(), y.max()], 'r--', linewidth=2)
plt.xlabel("Actual CO2 Emissions (g/km)")
plt.ylabel("Predicted CO2 Emissions (g/km)")
plt.title("Actual vs Predicted CO2 Emissions")
plt.grid(True)
plt.show()

📈 Results
Metric	Value
Mean Absolute Error (MAE)	3.27
Mean Squared Error (MSE)	24.81
Root Mean Squared Error (RMSE)	4.98
R² Score	0.994

The scatter plot demonstrates an almost perfect fit along the y=x line.

🚀 Insights

Fuel consumption is the strongest predictor of CO₂ emissions.

Transmission and fuel type also contribute, but numerical features dominate.

This model can help automotive engineers and policymakers monitor and reduce carbon footprints efficiently.

🔗 Files

CarbonIQ.ipynb — full notebook with preprocessing, regression, metrics, and plots

fuel_consumption_dataset.csv — input dataset
