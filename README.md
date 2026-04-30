# Design and Implementation of a Data Mining-Based System for Predicting Customer Purchasing Patterns in E-Commerce

**Author:** Rehobot Wolde  
**Subject Area:** Data Mining  

## Abstract
This project aims to design and implement a hybrid data mining system that integrates transaction and clickstream data to accurately predict customer purchasing patterns in e-commerce environments. Most operational e-commerce recommendation engines rely on collaborative filtering or simple rule-based heuristics that only consider past purchases, ignoring rich behavioral signals embedded in clickstream logs. 

By merging transaction records and clickstream logs from the REES46 e-commerce dataset, this research addresses data sparsity and cold-start problems. The system trains and evaluates three classification models: XGBoost, Random Forest, and a two-layer LSTM with attention for sequential clickstream input. Furthermore, it incorporates SHAP-based explainability mechanisms to improve transparency and practical usability for retailers. The ultimate goal is to enable personalized marketing, dynamic inventory management, and reduced cart-abandonment rates.

## Repository Structure
The repository is structured as follows:
```text
ecommerce-purchase-prediction/
+-- README.md
+-- proposal/
|   +-- main.tex
|   +-- references.bib
+-- data/
|   +-- raw/
+-- notebooks/
|   +-- 01_eda.ipynb
|   +-- 02_preprocessing.ipynb
|   +-- 03_modelling.ipynb
+-- src/
|   +-- preprocess.py
|   +-- models.py
|   +-- evaluate.py
+-- requirements.txt
```

## Installation Instructions

The project is built using Python 3.11. To set up the environment and run the code, follow these steps:

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
The system utilizes an industry-standard machine learning ecosystem. The required tools include scikit-learn 1.4, XGBoost 2.0, PyTorch 2.2, and SHAP 0.44. Data wrangling and visualization rely on Pandas, Matplotlib, and Seaborn. 

You can install all required packages via `pip`:
```bash
pip install -r requirements.txt
```

*(Note: If you are configuring PyTorch for GPU acceleration, please refer to the [official PyTorch installation guide](https://pytorch.org/get-started/locally/) to install the correct version for your CUDA environment before running the requirements file.)*

## Usage
1. Place the REES46 raw dataset files (`events.csv` and `purchases.csv`) into the `data/raw/` directory.
2. Execute the Jupyter notebooks in the `notebooks/` directory sequentially to run exploratory data analysis, preprocessing, and modelling.
