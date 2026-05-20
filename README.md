# Telecom Customer Churn Prediction with LLM-Powered Retention Insights

Predicting customer churn for a telecom provider using machine learning, and using a large language model to generate retention strategy suggestions for high-risk customers.

## Why this project

Telecom companies lose significant revenue when customers churn. Identifying customers who are likely to leave before they actually leave gives the business a chance to intervene with targeted retention offers. This project does two things:

1. Trains a classification model that predicts whether a customer will churn, based on their account, services, and demographics.
2. Uses an LLM to generate plain-language retention strategy suggestions for the customers the model flags as high-risk, bridging the gap between a prediction and an actionable next step.

## Dataset

IBM Telco Customer Churn dataset, 7043 customers, 21 features.

Source: https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv

Target variable: `Churn` (Yes / No).

## Repository structure

```
.
├── README.md
├── requirements.txt
├── data/                 # downloaded dataset goes here
└── notebooks/
    ├── 01_eda.ipynb              # exploratory data analysis
    ├── 02_modeling.ipynb         # baseline + tuned models (Session 2-3)
    └── 03_llm_enrichment.ipynb   # LLM retention suggestions (Session 4)
```

## Setup

```bash
# Clone or download this repo, then:
cd churn_project
python -m venv venv
source venv/bin/activate          # on Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Open `notebooks/01_eda.ipynb` and run the cells from top to bottom.

## Tools

- Python 3.10+
- pandas, numpy for data handling
- matplotlib, seaborn, plotly for visualization
- scikit-learn for modeling (Session 2 onwards)
- Anthropic Claude API for LLM enrichment (Session 4 onwards)

## Author

Seif Mostafa — Software Engineering graduate, currently working as a freelance AI automation engineer. Building this project as part of an application to the Vodafone Egypt AI Academy.
