# 📉 Bankruptcy Prediction Using Machine Learning

This project focuses on predicting **company bankruptcy** using financial indicators and machine learning models.  
The objective is to build a predictive system that can identify whether a company is likely to become **bankrupt or remain financially stable** based on financial ratios and performance metrics.

Bankruptcy prediction is an important problem in **financial analytics**, helping investors, financial institutions, and regulators assess financial risk.

---

# 🎯 Objective

The goal of this project is to develop a machine learning model that can accurately classify companies as:

- **0 → Non-Bankrupt**
- **1 → Bankrupt**

The dataset contains **financial performance indicators**, and the project involves:

- Data preprocessing
- Handling class imbalance
- Feature selection
- Training multiple machine learning models
- Evaluating performance using multiple metrics

---

# 📊 Dataset

The dataset contains **financial indicators of companies**, including profitability ratios, debt ratios, operational efficiency, and other financial metrics.

### Dataset Characteristics

- **Total rows (after cleaning):** 6,819  
- **Total features:** 95 financial indicators  
- **Target variable:** `Bankrupt?`  
- **Target type:** Binary classification

### Example Financial Features

Some important financial indicators used in the dataset include:

- Return on Assets (ROA)
- Operating Profit Rate
- Net Value Per Share
- Debt Ratio
- Cash Flow Metrics
- Working Capital Ratios
- Asset Turnover Ratios
- Financial Leverage Indicators

The dataset is originally sourced from financial records such as the **Taiwan Economic Journal database**.

---

# 🔍 Exploratory Data Analysis (EDA)

Exploratory Data Analysis was performed to understand the structure and characteristics of the dataset.

Key steps included:

- Checking dataset shape and data types
- Identifying duplicate rows
- Removing duplicate records
- Visualizing class distribution
- Performing correlation analysis between financial indicators

### Class Distribution

The dataset was highly **imbalanced**, which is common in bankruptcy prediction.

| Class | Description | Proportion |
|------|-------------|------------|
| 0 | Non-Bankrupt | 96.77% |
| 1 | Bankrupt | 3.23% |

This imbalance required special handling during modeling.

---

# 🧹 Data Preprocessing

Several preprocessing steps were applied before training machine learning models.

### Data Cleaning

- Removed **duplicate rows**
- Verified **missing values** (none present)
- Checked statistical distribution of features

### Feature Scaling

Financial features were standardized using **StandardScaler** to ensure all features contribute equally to the models.

### Train-Test Split

The dataset was split into:

- **80% Training Data**
- **20% Testing Data**

Stratified sampling was used to preserve class distribution.

---

# ⚖️ Handling Class Imbalance

Since bankruptcy cases are rare, the dataset was imbalanced.

To address this issue, **SMOTE (Synthetic Minority Over-sampling Technique)** was used.

SMOTE generates synthetic examples of the minority class, resulting in a **balanced dataset**.

After applying SMOTE:

- Class 0 → 50%
- Class 1 → 50%

This improves model learning and reduces bias toward the majority class.

---

# 🧠 Feature Selection

To reduce dimensionality and improve model performance:

- Feature importance was computed using **Random Forest**
- The **top 20 most important features** were selected for model training

This helped reduce noise and improve predictive performance.

---

# 🤖 Machine Learning Models Used

Multiple machine learning models were implemented and compared.

### Models Implemented

1. Logistic Regression
2. Decision Tree
3. Naive Bayes
4. K-Nearest Neighbors (KNN)
5. Support Vector Machine (SVM)

Hyperparameter tuning was performed using **GridSearchCV** where applicable.

---

# 📈 Model Evaluation Metrics

The models were evaluated using several performance metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Cross Validation
- Confusion Matrix

These metrics help assess how well the models detect bankruptcy cases.

---

# 📊 Model Performance Comparison

| Model | Accuracy | Precision | Recall | F1 Score |
|------|---------|---------|-------|-------|
| Logistic Regression | 0.8788 | 0.8794 | 0.8780 | 0.8787 |
| Decision Tree | **0.9515** | 0.9435 | 0.9606 | **0.9520** |
| Naive Bayes | 0.7841 | 0.7090 | 0.9636 | 0.8170 |
| KNN | 0.9375 | 0.9030 | **0.9803** | 0.9401 |
| SVM | 0.9261 | 0.8958 | 0.9644 | 0.9289 |

---

# 🏆 Best Performing Model

The **Decision Tree classifier** achieved the best overall performance with:

- **Accuracy:** 95.15%
- **Precision:** 94.35%
- **Recall:** 96.06%
- **F1 Score:** 95.20%

This model effectively balanced precision and recall, making it the most reliable predictor for bankruptcy detection.

---

# 📊 Confusion Matrix Analysis

Confusion matrices were generated for each model to evaluate prediction errors.

These matrices help analyze:

- True Positives (Correct Bankruptcy Predictions)
- True Negatives (Correct Non-Bankruptcy Predictions)
- False Positives
- False Negatives

Such analysis is crucial in financial risk prediction.

---

# ⚙️ Tech Stack

### Programming Language

- Python

### Libraries & Frameworks

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Imbalanced-Learn (SMOTE)

---

# 📈 Machine Learning Workflow

The project follows a structured ML pipeline:

1. Data Loading
2. Data Cleaning
3. Exploratory Data Analysis
4. Feature Scaling
5. Handling Class Imbalance (SMOTE)
6. Feature Selection
7. Model Training
8. Hyperparameter Tuning
9. Model Evaluation
10. Performance Comparison

---

# 🧪 Potential Applications

Bankruptcy prediction models can be used in:

- Credit risk assessment
- Financial market analysis
- Investment risk management
- Corporate financial monitoring
- Banking and lending systems

---

# 🚀 Future Improvements

Potential improvements include:

- Using **ensemble models** (XGBoost, LightGBM)
- Applying **deep learning models**
- Implementing **feature engineering**
- Building a **real-time financial risk prediction system**
- Deploying the model as a **web application or API**

---

# 🎯 Learning Outcomes

Through this project, the following concepts were explored:

- Financial data analysis
- Handling imbalanced datasets
- Feature selection techniques
- Model evaluation strategies
- Comparing multiple machine learning algorithms

---

# 👨‍💻 Author

**Prem**  
BCA Student – Artificial Intelligence & Machine Learning

Interests:

- Machine Learning
- Data Science
- Financial Analytics
- AI Applications

---

⭐ If you found this project useful, consider giving it a **star on GitHub**.
