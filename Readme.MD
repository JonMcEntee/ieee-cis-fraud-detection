# IEEE-CIS Fraud Detection

<img src="https://github.com/JonMcEntee/ieee-cis-fraud-detection/blob/main/credit-card-fraud.png?raw=true" width="50%" height="50%">

## Overview

This repository contains my solution to Kaggle's [IEEE-CIS Fraud Detection](https://www.kaggle.com/c/ieee-fraud-detection) competition, aiming to predict fraudulent online transactions. The project demonstrates a complete machine learning workflow from exploratory data analysis to model deployment.

## Competition Background IEEE-CIS

Institute of Electrical and Electronics Engineers - Computational Intelligence Society partnered with industry experts to create this challenge, using real-world transaction data from Vesta Corporation, a leading payment service company. 

## Methodology

The notebook implements a comprehensive approach: 

### Data Exploration
- Feature distribution visualization
- Statistical relevance examination using T-tests and Chi-squared

### Modeling Approaches
- Logistic Regression
- Multi-layer Perceptron
- XGBoost
- Random Forest

### Evaluation Metrics
- Primary: AUC-ROC (Area Under the Receiver Operating Characteristic Curve)
- Secondary: Precision-Recall curves
- Additional: Top 5 and top 10 precision scores

## Getting Started
### Prerequisites
- Python 3.7+
- Jupyter Notebook/Lab

### Installation 

```bash
git clone https://github.com/JonMcEntee/ieee-cis-fraud-detection.git
cd ieee-cis-fraud-detection
pip install -r requirements.txt
```

### Data Setup
1. Download competition data from [Kaggle](https://www.kaggle.com/c/ieee-fraud-detection/data)
2. Create a `data/` directory in the project root
3. Place all CSV files in this directory

### Running the Notebook

```bash
jupyter notebook IEEE_CIS_Fraud_Detection.ipynb
```

## Project Structure 

``` 
ieee-cis-fraud-detection/ 
├── data/ # Data directory (not included in repo) 
├── IEEE_CIS_Fraud_Detection.ipynb # Main notebook 
├── README.md # This file
└── requirements.txt # Python dependencies
```

## Key Insights

1. **Class Imbalance Challenge**:
- Only 3.5% of transactions were fraudulent
- Implemented class weighting
2. **Feature Importance**:
- Transaction amount and frequency were top predictors
- Certain card types showed higher fraud rates
3. **Performance**:
- Best single model: XGBoost (AUC = 0.917)

## Results

| Model | Train AUC | Test AUC | Train PR AUC | Test PR AUC | Precision K5 | Precision K10 |
 ------ | --------- | -------- | ------------ | ----------- | ------------ | ------------- |
| Logistic Regression | 0.543805 | 0.504985 | 0.039877 | 0.034906 | 0.0 | 0.0 |
| Multi-Layer Perceptron | 0.500011 | 0.499930 | 0.035136 | 0.034409 | 0.0 | 0.0 |
| Random Forest | 0.879251 | 0.857202 | 0.516721 | 0.426802 | 1.0 | 1.0 | 
| XGBoost | 0.980381 | 0.917417 | 0.878228 | 0.558776 | 1.0 | 1.0 |


## Acknowledgments
 - Kaggle and IEEE-CIS for hosting the competition
 - Vesta Corporation for providing the dataset
 - Kaggle community for shared insights and techniques
