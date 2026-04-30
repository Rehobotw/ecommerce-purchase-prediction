# [cite_start]Design and Implementation of a Data Mining-Based System for Predicting Customer Purchasing Patterns in E-Commerce [cite: 9, 10]

[cite_start]**Author:** Rehobot Wolde [cite: 11]  
[cite_start]**Subject Area:** Data Mining [cite: 13]  

## Abstract
[cite_start]This project aims to design and implement a hybrid data mining system that integrates transaction and clickstream data to accurately predict customer purchasing patterns in e-commerce environments[cite: 33]. [cite_start]Most operational e-commerce recommendation engines rely on collaborative filtering or simple rule-based heuristics that only consider past purchases, ignoring rich behavioral signals embedded in clickstream logs[cite: 27]. 

[cite_start]By merging transaction records and clickstream logs from the REES46 e-commerce dataset, this research addresses data sparsity and cold-start problems[cite: 29, 35]. [cite_start]The system trains and evaluates three classification models: XGBoost, Random Forest, and a two-layer LSTM with attention for sequential clickstream input[cite: 67]. [cite_start]Furthermore, it incorporates SHAP-based explainability mechanisms to improve transparency and practical usability for retailers[cite: 59]. [cite_start]The ultimate goal is to enable personalized marketing, dynamic inventory management, and reduced cart-abandonment rates[cite: 25].

## Repository Structure
[cite_start]The repository is structured as follows[cite: 152]:
```text
[cite_start]ecommerce-purchase-prediction/ [cite: 153]
[cite_start]+-- README.md [cite: 154]
[cite_start]+-- proposal/ [cite: 155]
|   [cite_start]+-- main.tex [cite: 156]
|   [cite_start]+-- references.bib [cite: 158]
[cite_start]+-- data/ [cite: 160]
|   [cite_start]+-- raw/ [cite: 161]
[cite_start]+-- notebooks/ [cite: 162]
|   [cite_start]+-- 01_eda.ipynb [cite: 163]
|   [cite_start]+-- 02_preprocessing.ipynb [cite: 165]
|   [cite_start]+-- 03_modelling.ipynb [cite: 166]
[cite_start]+-- src/ [cite: 167]
|   [cite_start]+-- preprocess.py [cite: 168]
|   [cite_start]+-- models.py [cite: 169]
|   [cite_start]+-- evaluate.py [cite: 172]
[cite_start]+-- requirements.txt [cite: 173]
```

## Installation Instructions

[cite_start]The project is built using Python 3.11[cite: 71]. To set up the environment and run the code, follow these steps:

### 1. Clone the Repository
```bash
git clone [https://github.com/Rehobotw/ecommerce-purchase-prediction.git](https://github.com/Rehobotw/ecommerce-purchase-prediction.git)
cd ecommerce-purchase-prediction
```

### 2. Create a Virtual Environment (Recommended)
It is recommended to use a virtual environment to manage dependencies.
```bash
python3.11 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### 3. Install Dependencies
[cite_start]The system utilizes an industry-standard machine learning ecosystem[cite: 72]. [cite_start]The required tools include scikit-learn 1.4, XGBoost 2.0, PyTorch 2.2, and SHAP 0.44[cite: 71, 74, 81, 84]. [cite_start]Data wrangling and visualization rely on Pandas, Matplotlib, and Seaborn[cite: 86]. 

You can install all required packages via `pip`:
```bash
pip install -r requirements.txt
```

*(Note: If you are configuring PyTorch for GPU acceleration, please refer to the [official PyTorch installation guide](https://pytorch.org/get-started/locally/) to install the correct version for your CUDA environment before running the requirements file.)*

## Usage
1. [cite_start]Place the REES46 raw dataset files (`events.csv` and `purchases.csv`) into the `data/raw/` directory[cite: 160, 161].
2. [cite_start]Execute the Jupyter notebooks in the `notebooks/` directory sequentially to run exploratory data analysis, preprocessing, and modelling[cite: 162, 163, 165, 166].
```
