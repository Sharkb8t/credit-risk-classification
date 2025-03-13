# 💳 Credit Risk Classification

## 🌐Overview:

This project involves building a **logistic regression model** to predict **credit risk** based on historical loan data. The goal is to classify loans as either **healthy (0)** or **high-risk (1)** using **scikit-learn's Logistic Regression model**.  

## 🖥️ Technologies Used:

🐍 Python

📊 Pandas

🤖 Scikit-Learn

📒 Jupyter Notebook  

## ℹ️ Dataset:

The dataset (`lending_data.csv`) contains **loan records** with various financial attributes.  

- **Label Variable (`loan_status`)**:

  - `0`: Healthy Loan

  - `1`: High-Risk Loan

- **Features (`X`)**: Various financial indicators (e.g., income, loan amount, credit history).  

## 🔧 Installation and Usage:

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Sharkb8t/credit-risk-classification.git
cd credit-risk-classification
```

### 2️⃣ Install Required Libraries

```bash
pip install pandas scikit-learn
```

### 3️⃣ Run the Jupyter Notebook

```bash
jupyter notebook
```

Open `credit_risk-classification.ipynb` and run cells in sequencial order.
> Update file path in cell *5*

## 🗺️ Steps in the Analysis

#### 1.) Data Preprocessing

✅ Load and inspect the dataset:

- Read lending_data.csv into a Pandas DataFrame.

- Check for missing values and data types.

✅ Define features and target variables:

- Separate loan_status as the target variable (y).

- Drop loan_status from the dataset to create features (X).

✅ Split the dataset:

- Use train_test_split() to divide the data into 80% training and 20% testing.

#### 2.) Model Training

🚀 Train a Logistic Regression Model:

- Import `LogisticRegression` from scikit-learn.

- Instantiate the model with `random_state=1`.

- Train the model using `X_train` and `y_train`.

#### 3.) Predictions and Evaluation

📈 Generate Predictions:

> Use `predict()` on `X_test` to generate loan risk predictions (`y_pred`).

📊 Evaluate Model Performance:

- Compute the Confusion Matrix to analyze misclassifications.

- Generate a Classification Report to measure:

> Precision (Positive Predictive Value)

> Recall (Sensitivity)

> F1-Score (Balance between Precision & Recall)

- Overall Accuracy

## 🧑‍🔬 Results Summary

| Metric        | Class 0 (Healthy Loan) | Class 1 (High-Risk Loan) |
|--------------|------------------------|--------------------------|
| **Precision**  | 100%                   | 86%                      |
| **Recall**     | 100%                   | 91%                      |
| **F1-Score**   | 100%                   | 88%                      |
| **Accuracy**   | **99%**                 | -                        |

### 🔍 Key Observations

- ✅ The model performs exceptionally well overall with 99% accuracy.

- 🔵 Perfect precision and recall for healthy loans (0).

- 🟡 Good recall (91%) for high-risk loans (1), but slightly lower precision (86%), meaning some false positives exist.

### 📑 Recommendation

The model is highly effective for predicting healthy loans, but to improve high-risk loan precision, we could:

- ⚖️ Adjust class weights (since high-risk loans are underrepresented).

- 🔄 Experiment with higher `max_iter` values for better convergence.

- 🌲 Use alternative models like Random Forest or SMOTE (Synthetic Minority Oversampling Technique) for balancing.
