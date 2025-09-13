# 📌 Assignment-1: Bank Marketing Campaign Prediction  

## 📖 Overview  
This project uses the **Portuguese Bank Marketing Dataset** to predict whether a client will subscribe to a term deposit (`y = yes/no`) based on demographic and campaign-related features.  
We applied **Logistic Regression** and **K-Nearest Neighbors (KNN)** classifiers, evaluated their performance, and visualized the confusion matrices with key metrics.  

---

## 📂 Dataset  
- **Source**: Bank Marketing Dataset  
- **Shape**: ~45,000 rows × 17 columns  
- **Target Variable (`y`)**:  
  - `yes` → client subscribed to a term deposit  
  - `no` → client did not subscribe  

### 🔑 Features
- **Demographics**: `age`, `job`, `marital`, `education`, `default`, `balance`  
- **Loan/Finance Info**: `housing`, `loan`  
- **Campaign Info**: `contact`, `day`, `month`, `duration`, `campaign`, `pdays`, `previous`, `poutcome`  

---

## ⚙️ Algorithms Used  

### 1️⃣ Logistic Regression  
- A statistical model to predict binary outcomes (`yes`/`no`).  
- Applied with:  
  ```python
  logreg = LogisticRegression(max_iter=500, solver='liblinear', class_weight='balanced', random_state=42)
  ```
- Handles imbalance using `class_weight='balanced'`

### 2️⃣ K-Nearest Neighbors (KNN)
- A distance-based classification algorithm.
- Uses the 5 nearest neighbors (k=5) to predict the class.
- Applied with:
  ```python
  knn = KNeighborsClassifier(n_neighbors=5)
  ```

---

## 📊 Evaluation Metrics

We evaluated models using:
- **Accuracy** → Overall correctness of the model.
- **Precision** → Fraction of positive predictions that were correct.
- **Recall** → Fraction of actual positives identified correctly.
- **F1-score** → Harmonic mean of precision & recall.

---

## 📊 Model Performance Results

### ✅ Logistic Regression
- **Accuracy**: 0.81
- **Precision**: 0.56
- **Recall**: 0.81
- **F1-Score**: 0.66

**Confusion Matrix**:
- True Negative (Actual: No, Predicted: No): 1230
- False Positive (Actual: No, Predicted: Yes): 284
- False Negative (Actual: Yes, Predicted: No): 364
- True Positive (Actual: Yes, Predicted: Yes): 1240

### ✅ K-Nearest Neighbors (KNN, k=5)
- **Accuracy**: 0.83
- **Precision**: 0.66
- **Recall**: 0.49
- **F1-Score**: 0.56

**Confusion Matrix**:
- True Negative (Actual: No, Predicted: No): 1400
- False Positive (Actual: No, Predicted: Yes): 114
- False Negative (Actual: Yes, Predicted: No): 229
- True Positive (Actual: Yes, Predicted: Yes): 218

---

## 📑 How to Run

1. **Clone the repository**
   ```bash
   git clone [https://github.com/your-username/Assignment-1-BankMarketing.git](https://github.com/IshaJaiswal32/APR_Assignment1)
   cd APR_Assignment_1.ipynb
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the notebook**
   ```bash
   jupyter notebook APR_Assignment_1.ipynb
   ```

---

## 📌 Conclusion

- **Logistic Regression** demonstrated better recall (0.81), meaning it was more effective at identifying actual subscribers to the term deposit.
- **KNN** showed higher accuracy (0.83) and precision (0.66), but lower recall (0.49), indicating it was more conservative in predicting positive cases.
- The dataset is imbalanced, making recall a more important metric than raw accuracy in real banking use-cases where identifying potential subscribers is crucial.
- Logistic Regression's balanced class weighting helped it perform better on the imbalanced dataset compared to KNN.

---

👩‍💻 **Author**: Isha Jaiswal (IIT Patna)
