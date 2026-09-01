# 🎓 Online Education Student Performance & Risk Prediction

## 📌 Project Overview

This project focuses on analyzing **online education student data** and using **Machine Learning** techniques to understand and predict student **academic performance, engagement, dropout risk, and final results**.

The project explores different student-related factors such as education level, region, studied credits, online activity, average score, engagement level, performance level, and risk level.

The goal is to use data analysis and machine learning to identify students who may require additional academic support and to understand the factors associated with student success or withdrawal.

---

## 🎯 Objectives

* Analyze student demographic and academic information.
* Study student engagement in online learning.
* Analyze the relationship between online activity and academic performance.
* Identify students with different levels of academic risk.
* Predict student outcomes using Machine Learning.
* Analyze factors related to passing, failing, and withdrawal.
* Provide useful insights that can support early intervention for at-risk students.

---

## 📊 Dataset

The dataset contains **32,593 student records** and **14 features**.

### Dataset Features

| Feature             | Description                                 |
| ------------------- | ------------------------------------------- |
| `id_student`        | Unique student identifier                   |
| `gender`            | Gender of the student                       |
| `region`            | Geographic region of the student            |
| `highest_education` | Highest level of education                  |
| `studied_credits`   | Number of credits studied                   |
| `imd_band`          | Socio-economic/deprivation band             |
| `total_clicks`      | Total online learning platform interactions |
| `avg_score`         | Average academic score                      |
| `engagement_level`  | Student engagement level                    |
| `performance_level` | Student performance category                |
| `risk_level`        | Academic/dropout risk category              |
| `pass_flag`         | Indicates whether the student passed        |
| `dropout_flag`      | Indicates whether the student dropped out   |
| `final_result`      | Final student outcome                       |

### Final Result Categories

The `final_result` column contains four outcomes:

* 🟢 **Pass**
* 🔴 **Fail**
* 🟠 **Withdrawn**
* 🟣 **Distinction**

---

## 🔍 Exploratory Data Analysis

The project performs **Exploratory Data Analysis (EDA)** to understand patterns and relationships within the dataset.

### Analysis Includes

* Dataset structure and information
* Missing value analysis
* Statistical analysis
* Student outcome distribution
* Gender distribution
* Regional distribution
* Education-level distribution
* Studied credits analysis
* Online engagement analysis
* Average score distribution
* Performance-level analysis
* Risk-level analysis
* Correlation analysis
* Data visualization using charts and graphs

---

## 🧹 Data Preprocessing

Before applying Machine Learning algorithms, the dataset is prepared through several preprocessing steps:

* Handling missing values
* Encoding categorical variables
* Selecting relevant features
* Removing unnecessary identifiers
* Preparing input and target variables
* Splitting the dataset into training and testing sets
* Feature transformation and scaling when required

---

## 🤖 Machine Learning

Machine Learning techniques are applied to identify patterns in student data and predict student outcomes.

### 1. 📚 Student Performance Prediction

Predict the academic performance of students based on available academic and engagement-related features.

### 2. 🚨 Dropout Risk Prediction

Identify students who may have a higher probability of dropping out.

### 3. 🎓 Final Result Prediction

Predict the student's final outcome:

```text
Pass | Fail | Withdrawn | Distinction
```

### 4. ⚠️ Student Risk Analysis

Analyze student engagement and academic characteristics to categorize students according to their risk level.

---

## 📈 Model Evaluation

Machine Learning models can be evaluated using appropriate performance metrics such as:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **Confusion Matrix**

These metrics help determine how effectively the model predicts student outcomes.

---

## 🛠️ Technologies Used

* 🐍 **Python**
* ☁️ **Google Colab**
* 📓 **Jupyter Notebook**
* 🐼 **Pandas**
* 🔢 **NumPy**
* 📊 **Matplotlib**
* 📈 **Seaborn**
* 🤖 **Scikit-learn**
* 🧠 **Machine Learning**

---

## 📚 Python Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder, StandardScaler
from sklearn.metrics import (
    accuracy_score,
    classification_report,
    confusion_matrix
)
```

---

## 📁 Project Structure

```text
Online-Education-ML/
│
├── online_education_dataset.csv
├── Online_Education_ML.ipynb
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Online-Education-ML.git
```

### 2. Navigate to the Project

```bash
cd Online-Education-ML
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 4. Run the Notebook

Open:

```text
Online_Education_ML.ipynb
```

You can run the project using:

* ☁️ Google Colab
* 📓 Jupyter Notebook
* 💻 VS Code

---

## ☁️ Google Colab

The complete analysis and Machine Learning implementation is available in Google Colab.

### 🔗 Colab Notebook

[Open Google Colab Notebook](https://colab.research.google.com/drive/16OjUnk5fWE28r3eQyuXoeSM2UF5Rb1Bf)

> **Note:** Make sure the notebook's sharing permission is set to **Anyone with the link – Viewer** if you want other people to access it.

---

## 📌 Key Insights

The dataset provides useful information about student behavior and academic outcomes.

Important areas investigated in this project include:

* 📊 Student engagement and online activity
* 📝 Average academic scores
* 🎓 Academic performance levels
* ⚠️ Student risk levels
* 🚨 Dropout behavior
* 🏆 Final student outcomes
* 📚 Relationship between educational background and performance

These insights can help educational institutions identify students who may need additional academic support.

---

## 💡 Real-World Applications

This type of Machine Learning system can be used in:

* 🎓 Online learning platforms
* 🏫 Colleges and universities
* 👨‍🎓 Student monitoring systems
* 💻 E-learning applications
* 👨‍🏫 Academic counseling systems
* 🚨 Early dropout detection systems

### Example

If a student shows **low engagement, low academic performance, and high risk**, an educational institution could provide additional mentoring or academic support before the student withdraws.

---

## 🔮 Future Improvements

Future versions of this project could include:

* ⚡ Real-time student performance prediction
* 🚨 Early warning system for dropout detection
* 📊 Interactive student analytics dashboard
* 🔔 Automated alerts for high-risk students
* 🧠 Deep Learning models
* ⚙️ Hyperparameter optimization
* 🚀 Model deployment using Flask or FastAPI
* 🌐 Web application for student risk prediction

---

## ⭐ Project Highlights

| Category                 | Details                         |
| ------------------------ | ------------------------------- |
| **Domain**               | Online Education                |
| **Dataset Size**         | 32,593 records                  |
| **Features**             | 14                              |
| **Programming Language** | Python                          |
| **ML Type**              | Classification / Prediction     |
| **Data Analysis**        | Pandas, NumPy                   |
| **Visualization**        | Matplotlib, Seaborn             |
| **ML Framework**         | Scikit-learn                    |
| **Environment**          | Google Colab / Jupyter Notebook |

---

## 👨‍💻 Author

**Karthikeyan R.**

> Machine Learning Project — Online Education Student Performance & Risk Prediction
