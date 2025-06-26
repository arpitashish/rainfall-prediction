# Rainfall-prediction



## 📌 Overview

This project applies **Machine Learning (ML)** techniques to predict **rainfall occurrence** (yes/no) using historical meteorological data. The model is trained using a **Random Forest Classifier**, optimized through **GridSearchCV**, and deployed via a **Flask web application** for real-time predictions.

---

##  Objective

- Build a predictive system for rainfall using historical weather data.
- Preprocess and clean meteorological data.
- Perform exploratory data analysis (EDA) to extract patterns.
- Train and optimize a machine learning model.
- Deploy the model in a user-friendly web app interface.

---

##  Dataset Description


- **Features (12 total):**
  - `pressure`, `maxtemp`, `mintemp`, `temperature`, `dewpoint`
  - `humidity`, `cloud`, `rainfall`, `sunshine`
  - `winddirection`, `windspeed`, `day`
- **Target variable:** `rainfall` (yes = 1, no = 0)

---

##  Methodology

### 🔧 Data Preprocessing
- Filled missing values (mode/median)
- Removed redundant temperature-related features
- Encoded `rainfall` to binary
- Addressed class imbalance via downsampling

###  Exploratory Data Analysis (EDA)
- Histograms, boxplots, count plots
- Feature correlation analysis

###  Model Training
- Model: `RandomForestClassifier`
- Optimized using `GridSearchCV`
- Evaluated with accuracy, precision, recall, F1-score

###  Evaluation
- **Cross-validation Accuracy:** 81.15%
- **Test Accuracy:** 79.7%
- **Recall (Rain):** 90%
- **Top Features:** `cloud`, `sunshine`, `humidity`

###  Deployment
- Model saved using `pickle`
- Flask web app for user input and prediction
- Outputs predicted label and confidence scores

---

##  Running the App

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run Flask app:
   ```bash
   python app.py
   ```
3. Visit:
   ```
   http://localhost:5000/
   ```

---

##  Sample Prediction

| Feature        | Value |
|----------------|-------|
| Pressure       | 1015  |
| Dew Point      | 20.2  |
| Humidity       | 85    |
| Cloud          | 80    |
| Sunshine       | 2.4   |
| Wind Direction | 70.0  |
| Wind Speed     | 16.9  |

 **Prediction:** Yes  
 **Confidence:** 86%

---

## ✅ Conclusion

This project demonstrates how machine learning can effectively support weather prediction, achieving high recall for rainfall detection and offering practical deployment through a web app. It’s a step forward in integrating data science with real-world environmental forecasting.
