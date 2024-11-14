Task 1 uploaded, Task 2 on 15.11, Task 3 on Monday 18.11

# NUWE-AI-Data-Science---CAIXABANK-TECH
# 📈 AI Agent - Report Maker 📊

https://nuwe.io/hackathons/the-game-is-hackathon?challenge=python-caixabank-tech 


## 🌐 Project Overview
This project was developed as part of my first hackathon, where I placed 19th out of 51 participants. The challenge's goal was to build several machine learning models and an AI agent to analyze transactional data and generate reports. I am currently working on Tasks 4 and 5 of this challenge as part of my personal learning journey, and so far, I am sharing solutions for the first three tasks.

The project is centered around processing transactional data, including customer information, card data, and transaction records, to support tasks such as:
- Fraud detection
- Expense forecasting
- Customer segmentation

The size of the datasets and high class imbalance added the difficulty (transactions data had 13305915 rows and the fraud transaction accounts for 0.15%).

## 🗂️ Dataset
The project relies on three primary datasets:
1. **Client Data**: demographic and account information
2. **Card Data**: details about clients' credit and debit cards
3. **Transactions**: a detailed record of transactions

We have also received codes dataset to get the transaction categories and transactions labels to train the model.
Due to data confidentiality and file size, the datasets are not included in this repository. 

<img width="327" alt="Screenshot 2024-10-28 at 00 32 37 copy" src="https://github.com/user-attachments/assets/0c38f51d-9918-41a7-97b8-e9a518550aa3">


## 🎯 Completed Tasks
The project is divided into multiple stages. During the time of hakaton, I have completed and received 455 of 1000 points for the first three tasks:

### Task 1: Statistical Queries
Finding answers to specific queries related to clients and transactions, such as identifying the client with the lowest credit limit and latest card expiry date.

### Task 2: Data Processing Functions
Implementation of functions for summarizing earnings, expenses, and cash flow within a specified period, using raw transaction data.

### Task 3: Fraud Detection Model
Creation of a supervised machine learning model to classify transactions as fraudulent or non-fraudulent. This model is trained to identify suspicious transaction patterns based on transaction frequency, amounts, and merchant details. I am working on achieving a higher balanced accuracy.


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
I am actively working on additional tasks, including:
- **Task 4**: Expense Forecasting Model — Building a time series model to forecast monthly expenses based on historical transaction data.
- **Task 5**: AI Agent with LangChain — Implementing an AI agent to generate a summary report based on user input, integrating predictive and analytical functions.

I keep working on crafting solutions for these tasks.

## 📝 Notes
This is my first hackathon project, it was quite challenging but also very close to a real life scenario. This was also my first real world experience with big datasets.

