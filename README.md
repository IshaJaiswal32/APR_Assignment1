# APR_Assignment1
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
- Handles imbalance using class_weight='balanced'

  2️⃣ K-Nearest Neighbors (KNN)

A distance-based classification algorithm.

Uses the 5 nearest neighbors (k=5) to predict the class.

Applied with:

knn = KNeighborsClassifier(n_neighbors=5)

📊 Evaluation Metrics

We evaluated models using:

Accuracy → Overall correctness of the model.

Precision → Fraction of positive predictions that were correct.

Recall → Fraction of actual positives identified correctly.

F1-score → Harmonic mean of precision & recall.

📸 Outputs
✅ Logistic Regression

Classification Report

Precision: 0.xx | Recall: 0.xx | F1-Score: 0.xx | Accuracy: 0.xx


Confusion Matrix with Metrics


✅ K-Nearest Neighbors (KNN, k=5)

Classification Report

Precision: 0.xx | Recall: 0.xx | F1-Score: 0.xx | Accuracy: 0.xx


Confusion Matrix with Metrics


📑 How to Run

Clone the repository

git clone https://github.com/your-username/Assignment-1-BankMarketing.git
cd Assignment-1-BankMarketing


Install dependencies

pip install -r requirements.txt


Run the notebook

jupyter notebook Assignment-1.ipynb

📌 Conclusion

Logistic Regression performed better in terms of handling class imbalance.

KNN struggled with high-dimensional categorical data without feature scaling.

The dataset is imbalanced, so recall is more important than raw accuracy in real banking use-cases.

👩‍💻 Author: Isha Jaiswal (IIT Patna)
