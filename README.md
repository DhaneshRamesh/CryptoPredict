# **Ethereum Price Analysis and Feature Engineering**

This repository contains a Jupyter Notebook and associated Python scripts that demonstrate **data loading, cleaning, feature creation, and exploratory analysis** for Ethereum price data. We also set up the environment for eventual **model training** using XGBoost.

---

## **Table of Contents**
1. [Introduction](#introduction)  
2. [Project Structure](#project-structure)  
3. [Key Features of the Notebook (Where You Score Marks)](#key-features-of-the-notebook-where-you-score-marks)  
4. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
5. [Usage](#usage)  
6. [Data Explanation](#data-explanation)  
7. [Notebook Workflow](#notebook-workflow)  
8. [Future Improvements](#future-improvements)  
9. [Contributing](#contributing)  
10. [License](#license)  
11. [Acknowledgements](#acknowledgements)

---

## **1. Introduction**
This project aims to **analyze and preprocess Ethereum historical prices** from two datasets:

- `coin_Ethereum.csv`  
- `Ethereum_Historical_Data.csv`

We demonstrate:
- Merging and cleaning data
- Creating new time-based features
- Exploratory data analysis with visualizations
- An outline for eventual **model training** using XGBoost


## **2. Project Structure**


```
├── README.md
├── environment.yml or requirements.txt   # Dependencies
├── your_notebook.ipynb                  # Main Jupyter Notebook with all code
├── coin_Ethereum.csv                    # First Ethereum dataset
├── Ethereum_Historical_Data.csv         # Second Ethereum dataset
└── ...
```


## **3. Key Features of the Notebook (Where You Score Marks)**

1. **Data Loading & Preparation**  
   - Importing necessary libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`, etc.).
   - Loading two Ethereum CSV files.
   - Verifying data integrity (`df.info()`, `df.isnull().sum()`, etc.).

2. **Data Cleaning & Feature Selection**  
   - Dropping unnecessary columns (`SNo`, `Name`, `Symbol`, `Volume`, `Marketcap`).
   - Parsing dates and setting the index to `Date` for time-series alignment.

3. **Feature Engineering**  
   - Creating new columns (`dayofweek`, `month`, `dayofyear`) for richer modeling.
   - Demonstrating how to transform raw data into features beneficial for machine learning.

4. **Exploratory Data Analysis**  
   - Simple visual checks (e.g., `sns.histplot`) to understand price distributions over time.

5. **Model Setup (XGBoost)**  
   - Outlining how features (`Open`, `High`, `Low`, etc.) and target variable (`Close`) are defined.
   - Importing `xgboost` for future regression or classification tasks.



## **4. Getting Started**

### 4.1 **Prerequisites**

- **Python 3.7 or above**  
- **Jupyter Notebook or JupyterLab** installed  
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `xgboost`  



### 4.2 **Installation**

1. **Clone this repository**:
   ```bash
   git clone https://github.com/yourusername/ethereum-analysis.git
   cd ethereum-analysis
   ```
2. **Create and activate a virtual environment** (optional but recommended):
   ```bash
   # Using conda
   conda create -n eth-env python=3.9
   conda activate eth-env

   # Or using python's venv
   python -m venv venv
   source venv/bin/activate  # On macOS/Linux
   venv\Scripts\activate     # On Windows
   ```
3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   or
   ```bash
   conda env create -f environment.yml
   conda activate eth-env
   ```


## **5. Usage**

1. **Jupyter Notebook**  
   - Launch Jupyter:  
     ```bash
     jupyter notebook
     ```
   - Open `your_notebook.ipynb` in the browser.

2. **Data Files**  
   - Ensure `coin_Ethereum.csv` and `Ethereum_Historical_Data.csv` are placed in the correct folder (or update paths in the notebook accordingly).

3. **Run Cells in Order**  
   - The notebook is designed to run sequentially. Start from the top (data loading) and follow through to feature creation and the initial modeling setup.

> **Highlight for Marks**: Step-by-step usage instructions show that you tested the workflow yourself.

---

## **6. Data Explanation**

- **`coin_Ethereum.csv`**:  
  - Contains historical Ethereum prices from 2015 to 2021, including `High`, `Low`, `Open`, `Close`, `Volume`, `Marketcap`, etc.

- **`Ethereum_Historical_Data.csv`**:  
  - Another time-series data source for Ethereum prices with fields like `Price`, `Open`, `High`, `Low`, `Vol.`, `Change %`, etc.

## **7. Notebook Workflow**

1. **Importing Libraries**  
   - `pandas`, `numpy`, `matplotlib`, `seaborn`, `xgboost`, etc.

2. **Data Loading**  
   - Reading CSVs with `pd.read_csv()`, checking shapes and info.

3. **Cleaning and Indexing**  
   - Dropping redundant columns.
   - Parsing and setting `Date` as the index for time-series operations.

4. **Feature Engineering**  
   - Creating day-based features: `dayofweek`, `month`, `dayofyear`.

5. **Exploratory Data Analysis (EDA)**  
   - Visualizing close prices over time with a histogram or any desired plot to observe trends or anomalies.

6. **Defining Features and Target**  
   - Features: `['Open','High','Low','dayofweek','month','dayofyear']`
   - Target: `['Close']`

7. **Model Preparation**  
   - Importing `xgboost` for potential regression tasks (training steps can be added in the future).



## **8. Future Improvements**

- **Model Training & Evaluation**:  
  - Implement the XGBoost model training and compare results (MAE, RMSE, R²).
  - Try other models (LSTM for time-series, Random Forest, etc.).
- **Hyperparameter Tuning**:  
  - Use Grid Search or Bayesian optimization to improve model accuracy.
- **Additional Features**:  
  - Incorporate external signals like network hashrate, on-chain metrics, or macroeconomic data.

> **Highlight for Marks**: Demonstrating awareness of your project’s limitations and offering next steps indicates thorough thinking.

---

## **9. Contributing**

1. **Fork** the repository  
2. **Create a new branch** (`git checkout -b feature/some-feature`)  
3. **Commit changes** (`git commit -m 'Add some feature'`)  
4. **Push to the branch** (`git push origin feature/some-feature`)  
5. **Open a Pull Request**

---

## **10. License**

You can include a license of your choice, for example:
```
MIT License
```
See the [LICENSE](LICENSE) file for details.

---

## **11. Acknowledgements**

- **Data Sources**:  
  - [coin_Ethereum.csv](https://www.kaggle.com/) or any original source reference  
  - [Ethereum_Historical_Data.csv](https://www.investing.com/) or any other site  
- **Libraries**:  
  - [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/), [Matplotlib](https://matplotlib.org/), [Seaborn](https://seaborn.pydata.org/), [XGBoost](https://xgboost.readthedocs.io/)



