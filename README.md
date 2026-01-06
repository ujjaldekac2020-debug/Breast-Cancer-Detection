# Breast Cancer Detection using Machine Learning

## Project Title
**Breast Cancer Diagnostic Classification System**

## Problem Statement
Breast cancer is one of the most common cancers globally, making early and accurate diagnosis essential for patient survival. The challenge lies in efficiently distinguishing between **Malignant** (cancerous) and **Benign** (non-cancerous) tumors. Manual classification by medical professionals can be time-consuming and subject to human error, creating a need for automated diagnostic assistance.

## Objective
The primary goals of this project are:
* To develop a machine learning model that accurately classifies breast mass tumors.
* To identify key cellular features that serve as strong indicators of malignancy.
* To provide a reliable, data-driven decision-support tool for clinical settings.

## Dataset Description
This project utilizes the **Breast Cancer Wisconsin (Diagnostic) Dataset**:
* **Total Instances**: 569 samples.
* **Features**: 30 numeric attributes including radius, texture, perimeter, and area of cell nuclei.
* **Target Classes**: Binary classification—Malignant (M) and Benign (B).

## Methodology / Approach
The project follows a structured data science pipeline:
1. **Exploratory Data Analysis (EDA)**: Visualizing correlations and feature distributions.
2. **Data Preprocessing**: Handling feature scaling and normalization for consistent model performance.
3. **Model Selection**: Implementing algorithms such as Logistic Regression, Random Forest, or Support Vector Machines (SVM).
4. **Evaluation**: Assessing the model using Accuracy, Precision, Recall, and Confusion Matrices.

## Tools & Technologies Used
* **Programming Language**: Python
* **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Environment**: Jupyter Notebook / Google Colab

## Steps to Run the Project
1. **Clone the repository**: Download the project files to your local environment.
2. **Install dependencies**: Run `pip install -r requirements.txt` to set up the necessary libraries.
3. **Execute the notebook**: Open the `.ipynb` file and run all cells sequentially to train and evaluate the model.

## Results / Output
* **Model Accuracy**: The final model achieved a classification accuracy of approximately **97-98%**.
* **Key Findings**: Features related to "worst area" and "worst concave points" were found to be the most significant predictors of malignancy.
