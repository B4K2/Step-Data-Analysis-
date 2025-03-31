# AI & Machine Learning Model for Step Data Analysis

## Overview
This project builds machine learning models to analyze and predict step count data using Fitbit datasets. It includes models for minute-level and hour-level step forecasting, as well as feature engineering using heart rate, calorie consumption, and MET (Metabolic Equivalent of Task) data.

## Features
- **Data Preprocessing**: Merging step count, heart rate, calorie, and MET data.
- **Feature Engineering**: Creating lag features, hourly aggregations, and handling missing values.
- **Deep Learning Model**: Implementing an LSTM model to predict future steps.
- **Visualization**: Plotting step and calorie trends over time.

## Datasets Used
The project utilizes Fitbit datasets containing:
- **Minute-level Data**: Steps, heartbeat, calories, MET.
- **Hourly Data**: Steps, calories.
- **Daily Activity Data**: Total steps, distance, activity minutes, calories.

Dataset source: [Fitbit Dataset on Kaggle](https://www.kaggle.com/datasets/arashnic/fitbit/data)

## Data Preprocessing
1. **Merging Datasets**: Combined minute and hourly data using `pandas.merge()`.
2. **Handling Missing Values**: Used mean imputation for heart rate and other missing values.
3. **Feature Engineering**:
   - Created lag features (previous steps, calories, heart rate)
   - Extracted `Hour` and `DayOfWeek` from timestamps.
   - Converted MET values to hourly aggregation.

## Model Architecture
- **LSTM-based Time Series Model**
- Input Features: Steps, Calories, Heart Rate, MET
- Output: Predicted step count for the next time step

## Visualization
- **Steps & Calories Over Time**
  - `seaborn` line plots to visualize trends.
- **Model Performance Evaluation**
  - Loss curves to analyze model convergence.

## How to Run
### Prerequisites
- Python 3.8+
- Required Libraries: `pandas`, `numpy`, `tensorflow`, `seaborn`, `matplotlib`

### Steps
1. Install dependencies:  
   ```bash
   pip install pandas numpy tensorflow seaborn matplotlib
   ```
2. Load the dataset and preprocess it.
3. Train the LSTM model using the prepared dataset.
4. Evaluate and visualize predictions.

## Future Work
- Optimize LSTM hyperparameters for better accuracy.
- Deploy a lightweight model on mobile devices.
- Improve feature selection for better predictions.

## Author
Akshat Balyan



