# 🚗 Used Cars Price Prediction

This project is all about predicting the selling price of used cars using machine learning. We worked with a real-world dataset that includes details like car name, manufacturing year, kilometers driven, fuel type, transmission, mileage, ownership type, and more.

---

## 📊 Objective

To build a regression model that accurately predicts the **Selling Price** of a used car based on various input features, and to compare different ML models to see which one performs best.

---

## 🧹 Data Preprocessing

- Dropped non-informative or redundant columns: `Name`, `Location`, `New_Price`, etc.
- Cleaned and converted textual mileage values (e.g., `"21.4 kmpl"`, `"20.5 km/kg"`) into numeric float values.
- Encoded categorical columns like `Owner_Type` and `Fuel_Type`.
- Removed rows with `NaN` values for a cleaner training process.
- Split data into `X_train`, `X_test`, `y_train`, `y_test`.

---

## 🤖 Models Used

### 1. **Linear Regression**
- Basic baseline model.
- Simple, interpretable, but didn’t perform too well.
- **R² Score**: ~0.65
- **Conclusion**: Not great, but helps us compare other models.

---

### 2. **Lasso Regression**
- Linear model with L1 regularization.
- Helps in feature selection by zeroing out less important features.
- Played with hyperparameter `alpha` to balance underfitting vs. overfitting.
- **R² Score**: Slightly better than basic Linear Regression.
- **Conclusion**: Good for feature reduction, but still not the best performer.

---

### 3. **Random Forest Regressor**
- Ensemble model based on decision trees.
- Captures non-linearity and interactions really well.
- **R² Score**: **0.86** 🔥
- **Conclusion**: Massive performance boost. Robust and reliable.

---

### 4. **XGBoost Regressor**
- Extreme Gradient Boosting — high-performance boosting algorithm.
- Tuned with parameters like `n_estimators`, `learning_rate`, and `max_depth`.
- Needed to make sure all features were properly encoded (especially categorical ones).
- **R² Score**: Close to Random Forest or sometimes better depending on tuning.
- **Conclusion**: Very powerful, great for production-level models.

---

## 🧠 Evaluation Metrics

- **R² Score** (coefficient of determination)
- **MSE** (Mean Squared Error)
- **Baseline R²**: ~-0.002 — literally worse than guessing the average 😂
- Final models improved performance dramatically over baseline.

---

## 🧪 Future Work

- Hyperparameter tuning using GridSearchCV.
- Try stacking/blending multiple models.
- Deploy using Flask or Streamlit.
- Add more advanced feature engineering.

---

## 📁 Files

- `USED_CARS_PRICE.ipynb`: Main notebook with all preprocessing, model training, and evaluation.
- `README.md`: You’re looking at it 😉

---

## 💬 Final Thoughts

This project was a full ML pipeline from raw dataset to performance comparison across multiple models. Random Forest and XGBoost dominated the leaderboard, but every model helped in understanding the data better.

Let's keep learning and building. 🚀

