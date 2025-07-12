# 🌦️ Rain Prediction using Gaussian Naive Bayes (weatherAUS Dataset)

## 📌 Project Overview

This project uses the **Gaussian Naive Bayes** algorithm to predict whether it will rain tomorrow based on historical weather data. The dataset comes from Australian weather stations and includes daily observations for various weather conditions.

---

## 📁 Dataset Information

- **📄 File Name**: `weatherAUS.csv`  
- **🎯 Target Variable**: `RainTomorrow` (1 = Yes, 0 = No)  
- **🔢 Features** include:
  - `MinTemp`, `MaxTemp`, `Rainfall`, `Humidity3pm`, `Pressure9am`, etc.  
  - Categorical features like `Location`, `WindGustDir`, `RainToday`

---

## 🧹 Data Preprocessing

1. ✅ Loaded data using `pandas.read_csv()`  
2. 🔍 Checked for missing values using `.isnull().sum()`  
3. 🧼 Filled missing values:
   - For numeric columns → filled with **median**  
   - For object (categorical) columns → filled with **mode**  
4. 🔁 Converted categorical data to numeric using `LabelEncoder`  
5. 🧾 Dropped `Date` and selected `RainTomorrow` as the target variable

---

## 🛠️ Model Training

- 🧠 Model: **Gaussian Naive Bayes** from `sklearn.naive_bayes`  
- 🧪 Data Split: 80% training, 20% testing using `train_test_split()`  
- ✅ Model training:
  ```python
  model.fit(x_train, y_train)
  ```

---

## 📈 Evaluation

- 📍 Predictions made with `model.predict(x_test)`  
- ✔️ Accuracy calculated using:
  ```python
  accuracy_score(y_test, y_pred)
  ```

---

## 📌 Key Observations

- Naive Bayes assumes independence between features, which makes it fast and scalable  
- Suitable for high-dimensional data and probabilistic outputs  
- Label encoding handled categorical features well  
- Filling missing data is crucial for model performance

---

## 🧰 Libraries Used

- `pandas` 🐼  
- `numpy` 🔢  
- `sklearn.model_selection` 🤖  
- `sklearn.naive_bayes` 🧠  
- `sklearn.metrics` 📊

---

## 🚀 Future Enhancements

- 📊 Compare with other models like Decision Trees or Random Forest  
- 📉 Analyze model with confusion matrix, precision, and recall  
- 🔁 Use feature scaling to improve model input consistency  
- 🌍 Visualize predictions per location or time using maps/charts

---

## 🙏 Acknowledgments

- Dataset provided by Australian Bureau of Meteorology  
- Inspired by weather prediction systems and climate analytics

---

## 📜 License

This project is licensed under the **MIT License** ✅
