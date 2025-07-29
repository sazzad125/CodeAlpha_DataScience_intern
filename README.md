
# CodeAlpha Data Science Internship

This repository contains **three practical data science projects** that demonstrate end-to-end workflows using Python. Each project covers different domains such as classification, regression, and exploratory data analysis (EDA).

---

## 📁 Projects Overview

### 1. 🌸 Iris Flower Classification
- **Goal**: Predict the species of Iris flowers using logistic regression.
- **Dataset**: Built-in Iris dataset (3 species, 150 samples).
- **Techniques**:
  - Data cleaning
  - Label encoding
  - Train-test split
  - Feature scaling
  - Confusion matrix & classification report
- **Model Used**: Logistic Regression
- **Libraries**: `pandas`, `scikit-learn`, `seaborn`, `matplotlib`

### 2. 📉 Unemployment Analysis in India
- **Goal**: Explore and visualize unemployment trends and the impact of COVID-19.
- **Dataset**: [Unemployment in India.csv](https://www.kaggle.com/datasets/rajanand/unemployment-in-india)
- **Techniques**:
  - Data preprocessing & EDA
  - Trend and seasonal analysis
  - Regional unemployment visualization
- **Key Insights**:
  - COVID-19 caused a spike in unemployment
  - States show differing trends
- **Libraries**: `pandas`, `matplotlib`, `seaborn`, `plotly`

### 3. 🚗 Car Price Prediction
- **Goal**: Predict used car selling prices using regression.
- **Dataset**: [Vehicle Dataset from Cardekho](https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho)
- **Techniques**:
  - Feature engineering
  - Label encoding for categorical variables
  - Standardization
  - Train/test split
  - Feature importance
- **Model Used**: Random Forest Regressor
- **Libraries**: `pandas`, `scikit-learn`, `matplotlib`, `seaborn`

---

## 📦 Requirements

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly
```

---

## 🚀 How to Run

Each project is available as a **Jupyter Notebook**:

```bash
jupyter notebook
```

Then open:
- `Iris.ipynb`
- `Unemployment.ipynb`
- `Car Price.ipynb`

---

## 📊 Output Snapshots

### Iris Project:
- Confusion Matrix Heatmap
- Classification Report

### Unemployment Project:
- Month-wise Unemployment Line Chart
- State-wise Choropleth Maps

### Car Price Prediction:
- Feature Importance Plot
- Predicted Car Price output

---

## 🎯 Learning Outcomes

- Practical implementation of machine learning algorithms
- Hands-on experience with data preprocessing and visualization
- Real-world problem solving in domains like finance, labor economics, and retail

---

## 📁 Dataset Sources

| Project | Dataset | Source |
|--------|---------|--------|
| Iris | Built-in Dataset | `sklearn.datasets.load_iris()` |
| Unemployment | [Unemployment in India.csv](https://www.kaggle.com/datasets/rajanand/unemployment-in-india) | Kaggle |
| Car Price | [Vehicle Dataset](https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho) | Kaggle |

---

## 📂 Project Structure

```
.
├── Iris.ipynb
├── Unemployment.ipynb
├── Car Price.ipynb
├── data/
│   ├── Unemployment in India.csv
│   └── car_data.csv
└── README.md
```
## 📄 License
This project is licensed under the MIT License — feel free to use, share, and modify with attribution.
