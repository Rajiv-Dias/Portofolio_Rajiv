# 🌧️ Rainfall Prediction using Random Forest

## 📌 Project Overview
This project aims to predict whether rainfall will occur based on weather-related features using a **Random Forest Classifier**.  
The project covers the complete machine learning workflow including:

- Data preprocessing
- Exploratory Data Analysis (EDA)
- Handling imbalanced data
- Feature preparation
- Model training
- Hyperparameter tuning
- Cross-validation
- Model evaluation
- Model saving using Pickle
- Prediction on unseen data

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

# ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Pickle

---

# 📊 Exploratory Data Analysis (EDA)

Performed several visualizations including:
- Distribution plots
- Histograms
- Correlation analysis

Example:

```python
sns.histplot(data[column], kde=True)
```

Purpose:
- Understand feature distribution
- Detect skewness and patterns
- Analyze relationships between variables

---

# ⚖️ Handling Imbalanced Data

The dataset was imbalanced, therefore:
- Downsampling technique was applied using:

```python
resample()
```

Purpose:
- Prevent model bias toward majority class
- Improve classification performance

---

# 🔀 Data Shuffling

```python
df_downsampled = df_downsampled.sample(frac=1, random_state=42)
```

Purpose:
- Shuffle dataset rows
- Prevent model from memorizing data order
- Improve generalization

---

# ✂️ Train-Test Split

Dataset was divided into:
- 80% Training Data
- 20% Testing Data

```python
train_test_split(test_size=0.2)
```

---

# 🌲 Random Forest Model

Model used:

```python
RandomForestClassifier()
```

Random Forest works by combining multiple Decision Trees to improve prediction accuracy and reduce overfitting.

---

# 🔧 Hyperparameter Tuning

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

# ✅ Cross Validation

Cross-validation was applied using:

```python
cross_val_score()
```

Purpose:
- Evaluate model stability
- Ensure consistent performance across multiple data splits

## Results

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
- Low standard deviation indicates the model is relatively stable across folds

---

# 📈 Model Evaluation

Evaluation metrics used:
- Accuracy Score
- Confusion Matrix
- Classification Report

Purpose:
- Measure prediction performance
- Analyze false predictions
- Evaluate precision, recall, and F1-score

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

The model can predict:
- Rainfall
- No Rainfall

along with prediction probabilities using:

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
```

---

# 🚀 Future Improvements

Possible improvements for this project:
- Try XGBoost or LightGBM
- Feature Engineering
- Streamlit Web App Deployment
- Improve model performance using additional weather features

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

LinkedIn: *(add your LinkedIn here)*  
GitHub: *(add your GitHub here)*
