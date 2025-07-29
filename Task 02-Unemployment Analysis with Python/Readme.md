# Unemployment in India Analysis

## Overview
This project analyzes the unemployment rate in India using the dataset `Unemployment in India.csv`. The analysis includes data cleaning, exploratory data analysis (EDA), and visualization of trends to understand unemployment patterns across different months.

## Dataset
The dataset (`Unemployment in India.csv`) contains 768 entries with the following columns:
- **Region**: State or region in India (object, 740 non-null)
- **Date**: Date of data collection (object, converted to datetime)
- **Frequency**: Data frequency (e.g., Monthly) (object, 740 non-null)
- **Estimated Unemployment Rate (%)**: Unemployment rate in percentage (float64, 740 non-null)
- **Estimated Employed**: Number of employed individuals (float64, 740 non-null)
- **Estimated Labour Participation Rate (%)**: Labour participation rate in percentage (float64, 740 non-null)
- **Area**: Rural or Urban (object, 740 non-null)

After cleaning, missing values (28 rows) were removed, and new columns (`month` and `year`) were created for temporal analysis.

## Requirements
To run the code, ensure the following Python libraries are installed:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

Install them using:
```bash
pip install pandas numpy matplotlib seaborn
```

## Project Structure
The Jupyter notebook (`Unemployment.ipynb`) is structured as follows:
1. **Import Libraries**: Import `pandas`, `numpy`, `matplotlib`, and `seaborn` for data manipulation and visualization.
2. **Configure Plots**: Set seaborn style to `whitegrid` and figure size to (10, 6).
3. **Load Dataset**: Read the dataset from `Unemployment in India.csv`.
4. **Initial Inspection**:
   - Display the first few rows.
   - Check dataset info (data types, non-null counts).
5. **Data Cleaning**:
   - Strip and lowercase column names, replacing spaces with underscores (e.g., `estimated_unemployment_rate_(%)`).
   - Convert `date` column to datetime format (with a warning about date parsing, suggesting `dayfirst=True` for consistency).
   - Drop rows with missing values in `estimated_unemployment_rate_(%)` (28 rows dropped).
   - Create `month` (as period 'M') and `year` columns from `date`.
6. **Exploratory Data Analysis (EDA)**:
   - Display descriptive statistics (mean, min, max, etc.) for numerical columns:
     - **Estimated Unemployment Rate (%)**: Mean = 11.79, Min = 0.00, Max = 76.74
     - **Estimated Employed**: Mean = 7.20M, Min = 49,420, Max = 45.78M
     - **Estimated Labour Participation Rate (%)**: Mean = 42.63, Min = 13.33, Max = 72.57
   - Visualize the monthly average unemployment rate trend using a line plot with markers.
7. **Save Cleaned Data**: Save the cleaned dataset to `Cleaned_Unemployment_India.csv`.

## How to Run
1. Place `Unemployment in India.csv` in the same directory as the notebook.
2. Open `Unemployment.ipynb` in Jupyter Notebook or Google Colab.
3. Run the cells sequentially to load, clean, analyze, and visualize the data.
4. The line plot will display the monthly average unemployment rate trend.
5. The cleaned dataset will be saved as `Cleaned_Unemployment_India.csv`.

## Results
- **Descriptive Statistics**:
  - Unemployment rates vary significantly, with a maximum of 76.74% and a minimum of 0.00%.
  - Employment numbers range from 49,420 to 45.78 million.
  - Labour participation rates range from 13.33% to 72.57%.
- **Visualization**:
  - The line plot shows the monthly average unemployment rate across India, with data points marked for each month from May 2019 to June 2020.
  - The plot indicates fluctuations in unemployment, likely reflecting economic changes (e.g., pre- and post-COVID periods).

## Notes
- The dataset contains missing values (28 rows), which were dropped to ensure data quality.
- The date parsing warning suggests using `dayfirst=True` in `pd.to_datetime` to handle the `DD-MM-YYYY` format explicitly.
- The `SettingWithCopyWarning` in the notebook indicates potential issues with chained assignments when creating `month` and `year` columns. This can be resolved by using `.loc` or creating a copy of the dataframe explicitly.
- The analysis focuses on monthly trends; further analysis could explore regional or urban/rural differences.
- The high maximum unemployment rate (76.74%) suggests potential outliers or specific regions/periods with extreme unemployment, possibly due to economic disruptions like COVID-19 lockdowns.

## Author
Md Sazzad Hossen

## License
This project is for educational purposes and uses a publicly available dataset. The code and cleaned dataset can be freely modified and used as needed.
