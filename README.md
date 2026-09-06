# Diabetes Classification using Naive Bayes

A machine learning project that predicts diabetes based on glucose levels and blood pressure measurements using the **Gaussian Naive Bayes** classifier.

---

## 📌 Overview

This project builds a binary classification model to predict whether a patient has diabetes. The dataset contains 995 samples evaluated against key physiological parameters, achieving an overall cross-validation accuracy of **~93.27%**.

---

## 📊 Dataset Details

* **Total Samples:** 995 entries


* **Missing Values:** None


* **Features (`X`):**
* `glucose`: Glucose level


* `bloodpressure`: Blood pressure reading




* **Target Variable (`y`):**
* `diabetes`: Target binary variable (`0` = No Diabetes, `1` = Diabetes)





---

## 🛠️ Project Workflow

1. **Data Loading & Preprocessing:**
* Loaded data using `pandas`.


* Verified missing values (`isna().sum()`) and checked dataset info.


* Features scaled using `StandardScaler`.




2. **Train-Test Split:**
* Data split into 80% training set (796 samples) and 20% testing set (199 samples) using `random_state=42`.




3. **Model Training:**
* Trained a `GaussianNB` classifier on scaled training data.




4. **Validation & Evaluation:**
* Evaluated model using accuracy score, classification report, confusion matrix, and 5-fold cross-validation.





---

## 📈 Model Performance & Results

* **Test Accuracy:** **92.96%**

* **5-Fold Cross-Validation Accuracy:** **93.27%**


### Classification Report

```text
               precision    recall  f1-score   support

           0       0.92      0.92      0.92        93
           1       0.93      0.93      0.93       106

    accuracy                           0.93       199
   macro avg       0.93      0.93      0.93       199
weighted avg       0.93      0.93      0.93       199

```

### Confusion Matrix

| | Predicción: No (0) | Predicción: Sí (1) |
| :--- | :---: | :---: |
| **Actual: No (0)** | 86 | 7 |
| **Actual: Sí (1)** | 7 | 99 |

* **True Negatives (Class 0):** 86
* **True Positives (Class 1):** 99
* **False Positives:** 7
* **False Negatives:** 7


---

## 🚀 Installation & Usage

### Prerequisites

Make sure you have Python installed along with the required dependencies:

```bash
pip install pandas scikit-learn

```

### Running the Notebook

1. Clone this repository:
```bash
git clone https://github.com/mohitbatheja/your-repository-name.git
cd your-repository-name

```


2. Place `Naive-Bayes-Classification-Data.csv` in the root directory.


3. Run the Jupyter Notebook or convert it to a script to train and evaluate the model.
