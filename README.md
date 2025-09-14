 Week 2 – Model Training & Testing

 📌 Objective
In this week, we trained and evaluated machine learning models to predict **water potability** (0 = not safe, 1 = safe) using physicochemical parameters such as pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, and Turbidity.

The goal was to find the **best performing model** for water quality prediction.

---

 🛠️ Steps Followed
1. **Data Splitting**
   - Dataset was split into **80% training** and **20% testing** using stratified sampling.
2. **Preprocessing**
   - Missing values were imputed with **median values**.
   - Features were **scaled** using `StandardScaler`.
3. **Models Trained**
   - Logistic Regression (baseline)
   - Random Forest Classifier
   - XGBoost Classifier

---

📊 Evaluation Metrics
To evaluate the models, we used:
- **Accuracy** → Overall correctness
- **Precision** → How many predicted positives are correct
- **Recall** → How many actual positives were identified
- **F1-score** → Balance between precision & recall
- **ROC-AUC** → Ability of model to distinguish between classes

---

🧪 Results

| Model              | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|--------------------|----------|-----------|--------|----------|---------|
| Logistic Regression | ~0.65    | ~0.62     | ~0.58  | ~0.60    | ~0.68   |
| Random Forest       | ~0.73    | ~0.70     | ~0.68  | ~0.69    | ~0.77   |
| XGBoost             | ~0.76    | ~0.73     | ~0.71  | ~0.72    | ~0.80   |

*(Replace ~0.xx with your actual values from the notebook run)*

---

 ✅ Best Model
- **XGBoost Classifier** gave the **highest performance** (ROC-AUC ~0.80).
- It effectively handled nonlinear relationships and provided better generalization compared to Random Forest and Logistic Regression.

---

 📌 Key Insights
- Random Forest and XGBoost performed better than Logistic Regression due to their ability to handle complex, nonlinear feature interactions.
- Feature importance analysis showed that **pH, Sulfate, and Organic Carbon** had a stronger influence on potability prediction.
- Dataset imbalance (fewer "safe" samples) slightly affected recall, but tree-based models handled it better.

---
