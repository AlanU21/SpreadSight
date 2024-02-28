# Things to Consider

## COVID-19 Pandemic

### Excluding Pandemic Data

#### Pros:

* Reduces Noise: The pandemic period includes many anomalies and extreme market movements that are not representative of normal market conditions.
* Improves Model Stability: By excluding outliers, the model might provide more stable and consistent predictions for standard economic scenarios.

#### Cons:

* Loses Information: The pandemic period includes valuable information about how markets react to extreme events.
Reduced Robustness: The model may not perform well in future crises if it hasn't learned from past ones.

#### Dates to Exclude:
* The most intense period of market disruption due to COVID-19 was from around February or March 2020, when the markets began to react strongly to the pandemic, to July 2021 or later, when vaccines became widely available and economies started to reopen.

### Alternatives to Exclusion
* Model the Pandemic as a Special Case: Use dummy variables or segment models to specifically account for the pandemic period. The model can learn the normal relationships but also understand how these relationships change during crises.

* Dynamic Time Warping (DTW): DTW can be useful in aligning time series data that might have shifted during the pandemic.

* Include Pandemic-specific Indicators: Integrate variables that specifically measure pandemic-related economic impacts, like mobility indices, infection rates, or government policy responses.

* Train Multiple Models: Train one model on pre-pandemic data and another on pandemic data. Can help in understanding how relationships between variables might differ in crisis periods.

* Sensitivity Analysis: Test your model with and without the pandemic data to understand how much influence it has on predictions.