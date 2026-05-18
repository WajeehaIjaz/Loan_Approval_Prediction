# 🏦 Loan Approval Prediction

A machine learning project that predicts whether a loan application will be approved based on applicant details. Multiple classification algorithms are compared to find the best-performing model.

---

## 📌 Problem Statement

Banks receive thousands of loan applications daily. This project automates the approval decision by training ML models on historical applicant data, reducing manual effort and improving consistency.

---

## 📂 Dataset

- **File:** `Copy of loan.xlsx`
- **Features used:**
  | Feature | Type |
  |---|---|
  | Gender | Categorical |
  | Married | Categorical |
  | Dependents | Categorical |
  | Education | Categorical |
  | ApplicantIncome | Numerical |
  | CoapplicantIncome | Numerical |
  | LoanAmount (log) | Numerical |
  | TotalIncome (log) | Numerical |
- **Target:** `Loan_Status` (Approved / Not Approved)

---

## ⚙️ Workflow

```
Load Data → EDA & Visualization → Feature Engineering → 
Handle Missing Values → Encode Categoricals → Scale Features → 
Train Models → Compare Accuracy
```

### 1. Exploratory Data Analysis
- Distribution plots for `LoanAmount` and `TotalIncome`
- Count plots by Gender, Married status, Dependents, Self-Employment, Credit History

### 2. Feature Engineering
- `loanAmount_log` — log transform of `LoanAmount` to reduce skewness
- `TotalIncome` — sum of `ApplicantIncome` + `CoapplicantIncome`
- `TotalIncome_log` — log transform of `TotalIncome`

### 3. Missing Value Handling
- Categorical columns → filled with **mode**
- Numerical columns → filled with **mean**

### 4. Preprocessing
- `LabelEncoder` applied to categorical features (Gender, Married, Dependents, Education) and target variable
- `StandardScaler` applied to normalize all features

---

## 🤖 Models Trained

| Model | Reason for Use |
|---|---|
| **Random Forest** | Handles mixed data types, reduces overfitting via ensemble |
| **Gaussian Naive Bayes** | Fast, effective for normally distributed features |
| **Decision Tree** | Interpretable, handles non-linear relationships |
| **K-Nearest Neighbors** | Similarity-based, works well for small/medium datasets |

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/loan-approval-prediction.git
   cd loan-approval-prediction
   ```

2. **Install dependencies**
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn openpyxl
   ```

3. **Add the dataset**
   Place `Copy of loan.xlsx` in `/content/` (if using Google Colab) or update the path in the notebook.

4. **Run the notebook**
   ```bash
   jupyter notebook Loan_Approval_Prediction.ipynb
   ```

---

## 🛠️ Tech Stack

- **Python 3.x**
- **Libraries:** NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn

---

## 📁 Project Structure

```
loan-approval-prediction/
│
├── Loan_Approval_Prediction.ipynb   # Main notebook
├── Copy of loan.xlsx                # Dataset (add manually)
└── README.md
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
