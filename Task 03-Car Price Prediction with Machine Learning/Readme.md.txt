

# Car Price Prediction

## Overview
This project uses a linear regression model to predict the selling price of used cars based on the `car_data.csv` dataset. The analysis includes data preprocessing, feature engineering, model training, evaluation, and visualization of results. The project is implemented in a Jupyter notebook (`Car Price.ipynb`) using Python and popular data science libraries.

## Dataset
The dataset (`car_data.csv`) contains 301 entries with the following columns:
- **Car_Name**: Name of the car (e.g., "ritz", "sx4") (object, 301 non-null)
- **Year**: Year of manufacture (int64, 301 non-null)
- **Selling_Price**: Selling price in lakhs (float64, 301 non-null)
- **Present_Price**: Current market price in lakhs (float64, 301 non-null)
- **Driven_kms**: Kilometers driven (int64, 301 non-null)
- **Fuel_Type**: Fuel type (Petrol, Diesel, CNG) (object, 301 non-null)
- **Selling_type**: Dealer or Individual (object, 301 non-null)
- **Transmission**: Manual or Automatic (object, 301 non-null)
- **Owner**: Number of previous owners (int64, 301 non-null)

## Requirements
To run the notebook, ensure the following Python libraries are installed:
- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`
- `joblib`

Install them using:
```bash
pip install pandas numpy matplotlib scikit-learn joblib
```

## Project Structure
The `Car Price.ipynb` notebook is structured as follows:
1. **Import Libraries**: Load necessary libraries (`pandas`, `numpy`, `matplotlib.pyplot`, `sklearn`, `joblib`).
2. **Load Dataset**: Read `car_data.csv` into a pandas DataFrame.
3. **Initial Inspection**: Display the first few rows and dataset info.
4. **Feature Engineering**:
   - Create a `Brand` column by extracting the first word from `Car_Name`.
   - Calculate `Age` by subtracting `Year` from the current year (2025).
   - Select features: `Age`, `Present_Price`, `Driven_kms`, `Fuel_Type`, `Selling_type`, `Transmission`, `Owner`, `Brand`.
   - Encode categorical variables using one-hot encoding.
5. **Data Preprocessing**:
   - Split data into training (80%) and testing (20%) sets.
   - Scale numerical features using `StandardScaler`.
6. **Model Training**: Train a `LinearRegression` model on the scaled training data.
7. **Model Evaluation**: Compute Mean Absolute Error (MAE) and R² Score on the test set.
8. **Visualization**:
   - Scatter plot of actual vs. predicted selling prices.
   - Residual plot to analyze prediction errors.
9. **Save Outputs**:
   - Save the trained model to `car_price_model.pkl` using `joblib`.
   - Save test set predictions to `predictions.csv`.

## How to Run
1. Place `car_data.csv` in the same directory as `Car Price.ipynb`.
2. Open the notebook in Jupyter Notebook or Google Colab.
3. Install the required libraries (see Requirements).
4. Run the cells sequentially to:
   - Load and preprocess the data.
   - Train and evaluate the model.
   - Generate visualizations.
   - Save the model and predictions.
5. Outputs:
   - Visualizations will be displayed (actual vs. predicted prices, residual plot).
   - `car_price_model.pkl`: Saved trained model.
   - `predictions.csv`: Test set predictions with actual and predicted prices.

## Results
- **Model Performance**:
  - The linear regression model predicts car selling prices based on features like age, present price, kilometers driven, fuel type, selling type, transmission, owner count, and brand.
  - Performance metrics (MAE and R² Score) are computed to evaluate the model’s accuracy on the test set.
- **Visualizations**:
  - **Actual vs. Predicted Prices**: A scatter plot shows how well the predicted prices align with actual prices, with a reference line for perfect predictions.
  - **Residual Plot**: A scatter plot of residuals (actual - predicted prices) vs. predicted prices helps identify patterns in prediction errors.
- **Saved Outputs**:
  - The trained model is saved as `car_price_model.pkl` for future use.
  - Test set predictions are saved in `predictions.csv`, including actual and predicted selling prices.

## Notes
- The dataset has no missing values, so no imputation is required.
- The `Brand` feature is derived from `Car_Name`, assuming the first word represents the car brand.
- One-hot encoding significantly increases the number of features due to the high number of unique brands (98). Consider feature selection or dimensionality reduction (e.g., PCA) for improved model performance.
- The model assumes a linear relationship between features and selling price, which may not capture complex patterns. Advanced models (e.g., Random Forest, XGBoost) could be explored for better accuracy.
- The `Age` calculation uses 2025 as the current year, consistent with the notebook’s execution context.

## Author
Md Sazzad Hossen

## License
This project is for educational purposes and uses a publicly available dataset. The code and outputs can be freely modified and used as needed.

