# 🌧️ Rainfall Prediction using Random Forest

## 📌 Project Overview
This project aims to predict whether rainfall will occur based on weather-related features using a **Random Forest Classifier**.  
The project covers the complete machine learning workflow from data preprocessing, exploratory analysis, model training, hyperparameter tuning, evaluation, and prediction on unseen data.

---

# 🎯 Project Objectives
- Analyze weather-related factors affecting rainfall
- Build a machine learning classification model
- Evaluate model performance using multiple metrics
- Predict rainfall on unseen weather data

---

# 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pickle

---

# 📂 Dataset Features

The dataset contains several weather-related variables such as:

- Pressure
- Dew Point
- Humidity
- Cloud
- Sunshine
- Wind Direction
- Wind Speed

Target Variable:
- `rainfall` (Yes / No)

---

# A. Data Collection and Preprocessing

## Data Collection
The dataset contains historical weather information used to predict rainfall occurrence.

## Initial Preprocessing
Several preprocessing steps were performed:
- Handling missing values
- Checking duplicate data
- Data type verification
- Feature selection

Example:

```python
data.info()
data.isnull().sum()
```

---

# B. Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to understand:
- Feature distributions
- Outliers
- Data spread
- Weather pattern behavior

## Distribution Plot

The following visualization was used to analyze feature distribution:

```python
sns.histplot(data[column], kde=True)
```

### 📷 Distribution Plot

![imagealt](https://github.com/Rajiv-Dias/Portofolio_Rajiv/blob/f9993f6d4adce675cd3bf7ca627f298d6890270e/Python_Project/2.%20Rainfall_Prediction%20(Random%20Forest)/Pictures/Distribution%20for%20each%20columns.png)

Purpose:
- Understand feature distribution
- Detect skewness
- Identify potential anomalies

---

## Boxplot Analysis

Boxplots were used to detect outliers and compare data spread.

```python
sns.boxplot(x=data[column])
```

### 📷 Boxplot Visualization
<img width="800" alt="boxplot" src="YOUR_IMAGE_LINK_HERE">

Purpose:
- Detect outliers
- Understand feature variability

---

# C. Correlation Matrix

Correlation analysis was performed to identify relationships between features.

```python
sns.heatmap(data.corr(), annot=True, cmap='coolwarm')
```

### 📷 Correlation Heatmap
<img width="800" alt="heatmap" src="YOUR_IMAGE_LINK_HERE">

Purpose:
- Identify highly correlated variables
- Understand relationships between weather features
- Support feature selection

---

# D. Data Preprocessing

## Handling Imbalanced Data

The dataset was imbalanced, therefore:
- Downsampling technique was applied using:

```python
resample()
```

Purpose:
- Prevent model bias toward majority class
- Improve classification performance

---

## Data Shuffling

```python
df_downsampled = df_downsampled.sample(frac=1, random_state=42)
```

Purpose:
- Shuffle dataset rows
- Prevent the model from memorizing data order
- Improve model generalization

---

## Train-Test Split

Dataset was divided into:
- 80% Training Data
- 20% Testing Data

```python
train_test_split(test_size=0.2)
```

Purpose:
- Separate training and testing process
- Evaluate unseen data performance

---

# E. Model Preparation and Training

## Random Forest Model

The model used in this project:

```python
RandomForestClassifier()
```

Random Forest combines multiple Decision Trees to improve prediction performance and reduce overfitting.

---

## Hyperparameter Tuning

Hyperparameter tuning was performed using:

```python
GridSearchCV()
```

Parameters tuned:
- n_estimators
- max_depth
- max_features
- min_samples_split
- min_samples_leaf

Purpose:
- Find the best parameter combination
- Improve model performance
- Reduce overfitting

---

## Cross Validation

Cross-validation was applied using:

```python
cross_val_score()
```

Purpose:
- Evaluate model consistency
- Ensure stable performance across different data splits

### Cross-validation Scores

```python
[0.81578947 0.76315789 0.89189189 0.86486486 0.75675676]
```

### Mean Cross-validation Score

:contentReference[oaicite:0]{index=0}

### Standard Deviation

:contentReference[oaicite:1]{index=1}

Interpretation:
- The model achieved good average performance
- Low standard deviation indicates relatively stable model performance

---

# F. Check Model Accuracy

Several evaluation metrics were used to evaluate model performance:

## Accuracy Score

```python
accuracy_score(y_test, y_pred)
```

Purpose:
- Measure overall prediction accuracy

---

## Confusion Matrix

```python
confusion_matrix(y_test, y_pred)
```

Purpose:
- Analyze correct and incorrect predictions
- Detect false positives and false negatives

---

## Classification Report

```python
classification_report(y_test, y_pred)
```

Metrics included:
- Precision
- Recall
- F1-score

Purpose:
- Provide detailed classification evaluation

---

# 💾 Model Saving

The trained model was saved using Pickle:

```python
pickle.dump()
```

Purpose:
- Reuse the trained model without retraining
- Prepare model for deployment

---

# 🔮 Prediction on Unseen Data

Example prediction:

```python
prediction = model.predict(input_df)
```

The model predicts:
- Rainfall
- No Rainfall

along with prediction probability using:

```python
predict_proba()
```

---

# 📁 Project Structure

```bash
├── rainfall_prediction.ipynb
├── rainfall_prediction_model.pkl
├── README.md
├── dataset.csv
├── images/
```

---

# 🚀 Future Improvements
Possible future improvements:
- Try XGBoost or LightGBM
- Perform feature engineering
- Deploy using Streamlit
- Add more weather features

---

# 📌 Key Learning Outcomes
Through this project, I learned:
- End-to-end machine learning workflow
- Random Forest implementation
- Hyperparameter tuning
- Cross-validation techniques
- Model evaluation
- Model persistence using Pickle

---

# 👨‍💻 Author
Rajiv Noor Said

LinkedIn: *(Add your LinkedIn here)*  
GitHub: *(Add your GitHub here)*
