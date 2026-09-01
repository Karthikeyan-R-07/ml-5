# 🧹 Customer Churn Data Preprocessing

## 📌 Project Overview

This project focuses on **data preprocessing for customer churn analysis** using Python and popular data science and machine learning libraries.

The project uses the **Churn Modelling dataset**, which contains customer information such as credit score, geography, age, tenure, balance, number of products, estimated salary, and churn status.

The preprocessing work is divided into two main tasks:

1. 🧹 **Data Cleaning**
2. ⚖️ **Feature Scaling**

---

## 🎯 Project Objectives

* Load and inspect a customer churn dataset.
* Identify missing values.
* Understand the structure and data types of the dataset.
* Handle missing values in the `Age` column.
* Explore basic statistical information.
* Select relevant numerical features.
* Understand feature scaling techniques.
* Prepare customer data for further machine learning tasks.

---

## 📊 Dataset

The dataset used in this project is:

```text
Churn_Modelling1.csv
```

### Dataset Information

| Property              | Details  |
| --------------------- | -------- |
| **Number of Records** | 10,000   |
| **Number of Columns** | 14       |
| **Target Variable**   | `Exited` |
| **Duplicate Rows**    | None     |

### Dataset Features

| Column            | Description                                         |
| ----------------- | --------------------------------------------------- |
| `RowNumber`       | Row number of the customer                          |
| `CustomerId`      | Unique customer ID                                  |
| `Surname`         | Customer surname                                    |
| `CreditScore`     | Customer's credit score                             |
| `Geography`       | Customer's country                                  |
| `Gender`          | Customer gender                                     |
| `Age`             | Customer age                                        |
| `Tenure`          | Number of years the customer has been with the bank |
| `Balance`         | Customer account balance                            |
| `NumOfProducts`   | Number of bank products used                        |
| `HasCrCard`       | Indicates whether the customer has a credit card    |
| `IsActiveMember`  | Indicates whether the customer is an active member  |
| `EstimatedSalary` | Estimated customer salary                           |
| `Exited`          | Indicates whether the customer left the bank        |

---

# 🧹 1. Data Cleaning

The `Data Cleaning.ipynb` notebook performs basic data inspection and missing-value handling.

## 📚 Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

### 📥 Load the Dataset

```python
df = pd.read_csv("Churn_modelling.csv")
```

### 🔍 Inspect the Dataset

```python
df.info()
```

This is used to examine:

* Column names
* Data types
* Number of non-null values
* Dataset structure

### ❓ Check Missing Values

```python
df.isnull().sum()
```

The dataset contains missing values in:

| Column   | Missing Values |
| -------- | -------------: |
| `Gender` |             37 |
| `Age`    |             34 |

### 🗑️ Remove Columns Containing Missing Values

The notebook also demonstrates:

```python
updated_df = df.dropna(axis=1)
```

This removes columns that contain missing values.

> **Note:** Dropping an entire column because of missing values is not always the best approach. In real-world machine learning projects, it is usually better to investigate the missing data and apply an appropriate imputation strategy.

### 📐 Calculate Age Statistics

The mean and median of `Age` are calculated using:

```python
df["Age"].mean()
df["Age"].median()
```

### 🔧 Fill Missing Age Values

Missing values in `Age` are replaced using the mean age:

```python
updated_df = df.copy()

updated_df["Age"] = updated_df["Age"].fillna(
    df["Age"].mean()
)
```

This allows the dataset to retain those customer records instead of removing them.

---

# ⚖️ 2. Feature Scaling

The `Feature_Scaling.ipynb` notebook prepares numerical features for feature scaling using Scikit-learn.

## 📚 Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

Scikit-learn preprocessing classes:

```python
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
```

### 🔍 Dataset Inspection

The notebook uses:

```python
df.info()
df.describe().round(2)
df.head()
```

These functions are used to:

* Inspect the dataset
* Understand data types
* View statistical information
* Display the first few records

### 🎯 Selecting Features

The notebook creates a new DataFrame containing:

```python
new_df = pd.DataFrame(
    df,
    columns=["Age", "Tenure"]
)
```

Therefore, the following numerical features are selected for the scaling exercise:

* `Age`
* `Tenure`

### 📌 Scaling Techniques

Two common scaling techniques are introduced:

#### Standardization

```python
scaler = StandardScaler()
```

StandardScaler transforms features so that they generally have:

* Mean ≈ `0`
* Standard deviation ≈ `1`

#### Min-Max Scaling

```python
scaler = MinMaxScaler()
```

MinMaxScaler generally transforms values into a range between:

```text
0 and 1
```

> **Note:** The current notebook imports `StandardScaler` and `MinMaxScaler` and selects `Age` and `Tenure`, but the actual scaling transformation has not yet been applied in the provided notebook.

---

# 🔄 Data Preprocessing Workflow

```text
             Churn Modelling Dataset
                       │
                       ▼
                Load Dataset
                       │
                       ▼
                 Inspect Data
                       │
                       ▼
             Check Missing Values
                       │
                       ▼
                Data Cleaning
                       │
                       ▼
              Handle Missing Data
                       │
                       ▼
              Select Age & Tenure
                       │
                       ▼
               Feature Scaling
                       │
                       ▼
                Preprocessed Data
```

---

# 📊 Dataset Quality

The provided dataset contains:

* **10,000 customer records**
* **14 columns**
* **No duplicate rows**
* **34 missing values in `Age`**
* **37 missing values in `Gender`**

The cleaning notebook specifically handles missing `Age` values using the **mean of the `Age` column**.

---

# 🛠️ Technologies Used

| Technology              | Purpose                           |
| ----------------------- | --------------------------------- |
| 🐍 **Python**           | Programming language              |
| 🐼 **Pandas**           | Data loading and manipulation     |
| 🔢 **NumPy**            | Numerical operations              |
| 📊 **Matplotlib**       | Data visualization                |
| 📈 **Seaborn**          | Statistical visualization         |
| 🤖 **Scikit-learn**     | Feature preprocessing and scaling |
| 📓 **Jupyter Notebook** | Development environment           |

---

# 📁 Project Structure

```text
Customer-Churn-Preprocessing/
│
├── Churn_Modelling1.csv
│
├── Data Cleaning.ipynb
│
├── Feature_Scaling.ipynb
│
└── README.md
```

---

# 🚀 How to Run the Project

## 1. Clone the Repository

```bash
git clone https://github.com/Jenos07/cleaning-and-prediction.git
```

## 2. Navigate to the Project

```bash
cd cleaning-and-prediction
```

## 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## 4. Start Jupyter Notebook

```bash
jupyter notebook
```

## 5. Open the Notebooks

Run:

```text
Data Cleaning.ipynb
```

or:

```text
Feature_Scaling.ipynb
```

---

# 🔮 Future Improvements

The project can be extended by:

1. Handling missing `Gender` values.
2. Applying `StandardScaler` to numerical features.
3. Applying `MinMaxScaler` and comparing the results.
4. Encoding categorical variables such as `Geography` and `Gender`.
5. Removing unnecessary identifiers such as `RowNumber` and `CustomerId`.
6. Splitting the dataset into training and testing sets.
7. Training a machine learning model to predict customer churn.
8. Evaluating the model using:

   * Accuracy
   * Precision
   * Recall
   * F1-Score
   * Confusion Matrix
9. Building a complete customer churn prediction pipeline.
10. Deploying the trained model as a web application or API.

---

# 💡 Key Learning Outcomes

Through this project, I learned how to:

* Work with a real-world customer dataset.
* Load and inspect datasets using Pandas.
* Identify missing values.
* Handle missing numerical values.
* Perform basic statistical analysis.
* Select relevant numerical features.
* Understand data preprocessing.
* Understand Standardization and Min-Max Scaling.
* Prepare data for machine learning.

---

# 👩‍💻 Author

**karthikeyan R**

This project was created as a **Python and Machine Learning data preprocessing practice project**.
