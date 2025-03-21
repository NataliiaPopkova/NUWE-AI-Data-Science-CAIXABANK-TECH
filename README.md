# NUWE-AI-Data-Science---CAIXABANK-TECH 💳

> **Challenge**: [The Game is Hackathon – CaixaBank Tech @ NUWE](https://nuwe.io/hackathons/the-game-is-hackathon?challenge=python-caixabank-tech)

## 🌐 Project Overview

This project was developed as part of my **first hackathon**, where I placed **19th out of 51 participants**. The challenge aimed to build machine learning models and an AI agent to analyze transactional data and generate reports.

Since the hackathon, I continued working on the tasks to improve and deepen my understanding of ML for fraud detection and expense prediction.

The tasks included:
- Fraud detection  
- Expense forecasting  
- Customer segmentation  

The dataset was large-scale (13M+ transactions) and **highly imbalanced**, with only **0.15%** of transactions labeled as fraud.

---

## 🗂️ Dataset

The challenge provided three main datasets:

1. **Client Data** – demographic and account info  
2. **Card Data** – client credit/debit card details  
3. **Transactions** – all transaction records  

Additional auxiliary datasets included merchant category codes (`mcc`) and fraud labels.

> ⚠️ **Note**: Due to size and confidentiality, datasets are not included in this repo.

---

<img width="327" alt="Screenshot 2024-10-28 at 00 32 37 copy" src="https://github.com/user-attachments/assets/0c38f51d-9918-41a7-97b8-e9a518550aa3">


## 🎯 Completed Tasks

### 📌 Task 1: Statistical Queries

Queries about customer and transaction data, such as finding clients with the lowest credit limits, latest card expirations, etc.

### 🔧 Task 2: Data Processing Functions

Functions that compute:
- Total earnings  
- Total expenses  
- Net cash flow over a selected time period

These were validated via unit tests provided by organizers.

### 🛡️ Task 3: Fraud Detection Model

Developed a supervised ML model to classify transactions as **fraudulent** or **legitimate**.

#### ⚠️ Challenge:
- Dataset with ~13M rows  
- Only 0.15% labeled as fraud  
- Highly imbalanced

#### ✅ Approach:
- Model used: `XGBoostClassifier`  
- Applied **SMOTE** to upsample minority class (fraud)  
- Encoded categorical variables using `OrdinalEncoder`  
- Used `StratifiedTrainTestSplit`

#### 📊 Final Model Performance:
> Model trained **after** hackathon using improved pipeline and full training set

- **Balanced Accuracy**: 0.94
- **Recall (Fraud)**: 0.87  
- **Precision (Fraud)**: 0.54  
- **F1-score (Fraud)**: 0.67  

The model shows strong ability to detect rare fraud transactions.

#### 🔍 Feature Importance:

Top features:
- `mcc` (merchant category code)  
- `merchant_state`, `merchant_id`, `merchant_city`  
- `amount`, `hour` of transaction  
- Note: `id` remained in the dataset and ranked high in importance

---


## 📂 Repository Structure
The repository structure follows the hackathon's requirements and contains code that was completed and implemented
```plaintext
├── notebooks/                 # Jupyter notebooks I used to write the solutions
│   ├── data_preprocessing_Task_1.ipynb
│   ├── Task_2_Functions.ipynb
│   ├── task_3_classification_model.ipynb
│
├── predictions/               # Predictions files used for checking the solutions
│   ├── predictions_1.json     # Queries results for Task 1
│   ├── predictions_3.json     # Transactions IDs with corresponding labels
│   
│
├── reports/                   
│   ├── figures/               #An example of an expenses_summary image resulting from expenses_summary function
│      
│
├── src/                       
│   ├── data/                  # Data processing scripts
│   │   ├── data_functions.py  # Descriptions of functions to be implemented (completed)
│   │  
│
├── tests/                     # Unit tests were provided by the organizers 
│   ├── statistics_test.py     # Unit tests for data functions.py script
│   └── conftest.py            # Pytest configuration                    
│
├── README.md                  
└── requirements.txt          

```
![expenses_summary](https://github.com/user-attachments/assets/ce374bfb-f7f9-4d61-b9a2-24e8e6e1e64a)


## 🚀 Future Development

I am actively working on:

- **Task 4**: Expense forecasting (time series model)  
- **Task 5**: AI agent with LangChain to generate natural language reports based on user input

---

## 📝 Notes

This was my **first real-world experience** with big data and real-life classification challenges. It helped me discover a strong interest in **ML for FinTech** and the **ethical value** of fraud detection.

> 📌 **Purpose-driven data science**: I believe that solving real problems like fraud detection brings both technical growth and social impact.

