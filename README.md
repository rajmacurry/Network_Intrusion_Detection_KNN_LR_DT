#  Network Intrusion Detection using Machine Learning

This project focuses on detecting network intrusions (normal vs anomaly) using classical machine learning algorithms.  
We compare multiple models — **K-Nearest Neighbors (KNN)**, **Logistic Regression**, and **Decision Tree** —  
to evaluate their performance on detecting malicious network traffic.

---

##  Project Overview

###  Objective
The goal of this project is to build and compare different machine learning models for intrusion detection,  
analyzing how well each algorithm identifies anomalies within network traffic data.

###  Models Used
- **Logistic Regression**
- **K-Nearest Neighbors (KNN)**
- **Decision Tree**

Each model was:
- Trained on the same dataset
- Optimized using **Optuna** (for hyperparameter tuning)
- Evaluated using key classification metrics

---

## ⚙️ Workflow

### 1️ Data Preparation
- The dataset was split into **training** and **testing** sets.  
- Features were **one-hot encoded** for categorical variables.  
- Labels were kept as-is (binary: normal / anomaly).

### 2️ Model Training
Each model was trained separately:
- **Logistic Regression** for baseline linear classification  
- **KNN** for distance-based detection  
- **Decision Tree** for rule-based detection

### 3️ Hyperparameter Optimization
Used **Optuna** for parameter tuning:
- KNN: optimized `n_neighbors`
- Decision Tree: optimized `max_depth` and `criterion`

### 4 Evaluation Metrics
Each model was evaluated using:
- **Accuracy (Train & Test)**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**

All metrics were visualized for easy comparison.

---

##  Results Summary

| Model               | Train Accuracy | Test Accuracy |
|----------------------|----------------|----------------|
| KNN                 | 0.998          | 0.994          |
| Logistic Regression | 0.974          | 0.975          |
| Decision Tree       | 1.000          | 0.997          |

### Confusion Matrix & Classification Report Insights
- **Decision Tree** achieved the highest accuracy with perfect precision and recall — indicating near-flawless classification.  
- **KNN** closely followed, showing strong robustness with minimal false positives.  
- **Logistic Regression** performed slightly lower but still maintained high recall and precision, proving effective for linear decision boundaries.

### Precision & Recall Comparison
- All models achieved high precision and recall (>97%), demonstrating strong generalization and minimal misclassification.  
- **Precision** represents how many detected anomalies were truly anomalies.  
- **Recall** shows how many actual anomalies were correctly detected.

### F1-Score Comparison
The F1-Score balances Precision and Recall.  
All models scored >0.97, confirming reliable anomaly detection across algorithms.

---

##  Visualizations
The project includes:
- **Bar plots** comparing Precision and Recall for all models  
- **F1-score comparison** plot  
- **Confusion matrices** for each model  
- **Optuna optimization history and parameter importance plots**

---

##  Technologies Used
- Python   
- Scikit-learn  
- Optuna  
- Matplotlib / Plotly  
- Pandas, NumPy  
- Tabulate (for clean terminal outputs)

---

##  How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/network-intrusion-detection.git

2. Navigate to the folder:
   cd network-intrusion-detection

3. Install Dependencies:
   pip install -r requirements.txt

4. Run the main notebook or script:
   python final_code.ipynb
