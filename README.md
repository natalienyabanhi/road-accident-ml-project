#South Africa Road Accident Analysis & Intelligent Decision System (2017)

Project Overview

This project is a complete data science and machine learning system that analyzes road accident data in South Africa (2017). It includes data preprocessing, exploratory data analysis (EDA), ensemble machine learning models and a reinforcement learning (RL) system for accident prevention recommendations.

The goal is to predict accident severity and recommend traffic interventions using AI techniques.


##  Dataset Source
The dataset used in this project is publicly available and contains road accident records from South Africa (2017).

Source: https://www.kaggle.com/


## Dataset Description
The dataset contains 120 records and 16 features, including:

- Accident severity  
- Location type  
- Province and city  
- Vehicle type  
- Speed and speed zone  
- Number of vehicles and casualties  
- Date and time of accident  
- Road conditions (Occasions)



## Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- XGBoost  
- CatBoost  


##  Data Preprocessing
The dataset was cleaned and prepared using the following steps:

- Artificial missing values (8%) introduced for simulation  
- Missing values handled using:
- Mode imputation (categorical variables)  
- Median imputation (numerical variables)  
- Date and Time converted into usable formats  
- Outliers detected using IQR method and capped (Winsorisation)  
- Feature engineering:
- Hour extracted from Time  
- Month extracted from Date  
- Label encoding applied to categorical variables  
- Target variable encoded:
  - 0 = Bumper Accident  
  - 1 = Headon Accident  
  - 2 = Fatal Accident  

---

## Exploratory Data Analysis (EDA)
EDA was performed to understand:

- Accident severity distribution  
- High-risk provinces  
- Vehicle types involved  
- Casualty distribution patterns  
- Time and seasonal trends  


## Machine Learning Models
Three ensemble models were used:

- Random Forest Classifier  
- XGBoost Classifier  
- CatBoost Classifier  

### Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion Matrix  

CatBoost performed best due to strong handling of categorical features.


## Reinforcement Learning System

A Markov Decision Process (MDP) was used to model accident prevention.

### Components:
- **States:** Location × Speed Zone × Occasion  
- **Actions:** No Action, Safety Campaign, Speed Enforcement, Road Maintenance  
- **Reward:** Reduction in accident severity  
- **Algorithm:** Q-Learning  

The agent learns optimal traffic intervention strategies over time.


## System Architecture

The system has two stages:

1. **Prediction Stage (Machine Learning):**  
   Predicts accident severity using ensemble models.

2. **Decision Stage (Reinforcement Learning):**  
   Recommends interventions based on predicted severity.

---

##  Ethical Considerations
- Dataset contains geographic bias across provinces  
- Model must be explainable (SHAP recommended)  
- System should support decision-making, not full automation  
- Must comply with POPIA data privacy rules  
- Personal data (e.g., street names) should be anonymised in real deployment 

## How to Run the Project

### 1. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost catboost

2. Run Jupyter Notebookj

 jupyter notebook

3. Run steps in order:
Data loading
Preprocessing
EDA
Model training
Evaluation
RL simulation

PROJECT STRUCTURE

├── data/
│   └── South_Africa_Road_Accidents_2017.xlsx
├── notebooks/
│   └── analysis.ipynb
├── images/
│   └── eda_overview.png
├── README.md

References
James, G., Witten, D., Hastie, T. & Tibshirani, R. (2021). An Introduction to Statistical Learning. Springer
Scikit-learn documentation
XGBoost documentation
CatBoost documentation

Author : Natalie Nyabanhi

Data Science Student Richfield Institute if Technology
Focus: Machine Learning, Data Analysis and Intelligent Systems

Project Outcome

This project demonstrates an end to end AI system including:

Data preprocessing
Feature engineering
Machine learning
Reinforcement learning
Ethical AI considerations


