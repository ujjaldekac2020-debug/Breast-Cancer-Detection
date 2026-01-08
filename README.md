# Breast Cancer Detection using Machine Learning

This project aims to classify breast tumors as either **Malignant** or **Benign** using diagnostic features extracted from medical images.

---

## ■ Project Title
**Breast-Cancer-Detection: Automated Tumor Classification**

---

## ■ Problem Statement
Early detection of breast cancer is crucial for successful treatment and patient survival. Manual analysis of biopsy data is time-consuming and requires expert pathologists. This project seeks to leverage Machine Learning to provide a fast, reliable, and data-driven approach to assist in the diagnosis process.

---

## ■ Objective
* To build a robust classification model using the Wisconsin Breast Cancer Dataset.
* To identify the most critical features (like texture, area, and smoothness) that distinguish malignant cases.
* To achieve high sensitivity (Recall) to ensure that potential cancer cases are not overlooked.

---

## ■ Dataset Description
The model is trained on the **UCI Breast Cancer Wisconsin (Diagnostic) Dataset**.
- **Features:** 30 numeric features representing characteristics of cell nuclei (e.g., radius, perimeter, concavity).
- **Target:** 2 classes — Malignant (M) and Benign (B).
- **Size:** 569 instances.

---

## ■ Methodology / Approach
1. **Data Cleaning:** Handled missing values and encoded categorical labels.
2. **Feature Scaling:** Applied `StandardScaler` to normalize features for better model performance.
3. **Exploratory Data Analysis (EDA):** Analyzed feature correlations and distributions.
4. **Model Training:** Implemented and compared algorithms including:
   - Logistic Regression
   - Random Forest Classifier
   - Support Vector Machines (SVM)
5. **Evaluation:** Measured performance using Accuracy, Precision, Recall, and F1-Score.

---

## ■ Tools & Technologies Used
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
- **Platform:** Jupyter Notebook / VS Code

---

## ■ Steps to Run the Project
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/Breast-Cancer-Detection.git](https://github.com/your-username/Breast-Cancer-Detection.git)
