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

# Breast Cancer Detection

This project utilizes Machine Learning to classify breast mass samples as either **Malignant** (cancerous) or **Benign** (non-cancerous) based on digitized images of fine needle aspirates (FNA).

---

## ■ Project Title
**Breast Cancer Prediction and Classification**

---

## ■ Problem Statement
Breast cancer is a leading cause of death among women globally. Early detection significantly increases the chances of successful treatment. This project addresses the need for an automated, high-accuracy diagnostic tool that can assist medical professionals in identifying malignant tumors based on clinical features, reducing human error and diagnostic time.

---

## ■ Objective
* To implement a binary classification model that predicts tumor types with high precision and recall.
* To perform Exploratory Data Analysis (EDA) to understand the relationship between different cellular features (radius, texture, etc.).
* To evaluate the performance of different Machine Learning algorithms to find the most reliable model for clinical application.

---

## ■ Dataset Description
The project uses the **Breast Cancer Wisconsin (Diagnostic) Dataset**.
* **Total Instances:** 569
* **Attributes:** 30 numeric predictive features (e.g., mean radius, mean texture, mean perimeter, smoothness).
* **Target Classes:** * **M (Malignant):** Cancerous
    * **B (Benign):** Non-cancerous

---

## ■ Methodology / Approach
1. **Data Acquisition:** Loading the dataset and checking for missing values.
2. **Exploratory Data Analysis (EDA):** Using heatmaps to find highly correlated features and boxplots to detect outliers.
3. **Data Preprocessing:** - Feature Scaling using `StandardScaler` to ensure all features contribute equally.
   - Label Encoding for the target variable.
4. **Model Selection:** Comparing multiple classifiers (Logistic Regression, Random Forest, and SVM).
5. **Model Evaluation:** Using Confusion Matrices, Precision-Recall curves, and Accuracy scores to validate results.

---

## ■ Tools & Technologies Used
* **Python:** Primary programming language.
* **Pandas & NumPy:** For data cleaning and manipulation.
* **Scikit-Learn:** For implementing ML algorithms and data splitting.
* **Matplotlib & Seaborn:** For generating diagnostic visualizations.
* **Jupyter Notebook:** For interactive development and documentation.

---

## ■ Steps to Run the Project
1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/ujjaldekac2020-debug/Breast-Cancer-Detection.git](https://github.com/ujjaldekac2020-debug/Breast-Cancer-Detection.git)
   cd Breast-Cancer-Detection
