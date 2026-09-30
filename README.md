# 🔧 FeatureForge — Data Preparation & Feature Engineering

A practical machine learning assignment focused on transforming raw user data into meaningful, model-ready features using **Python, Pandas, NumPy, and Scikit-learn**.

The project uses a **SoundWave Music Platform** case study to explore how user behavior and profile information can be prepared and transformed for predicting **churn risk**.

## 📌 Project Overview

This assignment demonstrates an end-to-end data preparation workflow, starting from dataset inspection and continuing through feature engineering, categorical encoding, data splitting, feature scaling, and model preprocessing.

### 🎯 Key Areas Covered

* 📂 Dataset loading and inspection
* 📅 Datetime feature engineering
* 🎵 Domain-specific feature creation
* 🔤 Categorical feature encoding
* 📊 Feature discretization and binning
* ✂️ Stratified train-test splitting
* ⚖️ Leakage-free feature scaling
* 🔄 Scikit-learn preprocessing pipeline
* 🤖 Logistic Regression classification

## 🧠 Feature Engineering

Several new features are created from the original SoundWave user data:

| Feature           | Purpose                                          |
| ----------------- | ------------------------------------------------ |
| `signup_month`    | Extracts the signup month                        |
| `signup_day_name` | Identifies the signup day                        |
| `tenure_days`     | Calculates user tenure                           |
| `skip_rate`       | Estimates the user's song skipping behavior      |
| `is_curator`      | Identifies users who create multiple playlists   |
| `tier_code`       | Converts subscription levels into ordinal values |
| `age_group`       | Groups users into age categories                 |

## 🔤 Data Encoding

The notebook demonstrates two different approaches to handling categorical data:

* **Ordinal Encoding** for subscription tiers
* **One-Hot Encoding** for device types and other categorical variables

## ✂️ Train-Test Split

The dataset is divided using an **80/20 stratified split**.

Stratification is used to maintain a similar distribution of the `churn_risk` target variable in both training and testing sets.

## ⚖️ Feature Scaling

`StandardScaler` is used to standardize numerical features.

To prevent **data leakage**, the scaler is:

1. Fitted only on the training data
2. Used to transform the training data
3. Reused to transform the test data

## 🔄 Machine Learning Pipeline

The final section combines preprocessing and classification into a Scikit-learn pipeline.

```text
Raw Data
   ↓
Feature Selection
   ↓
Numerical Scaling + Categorical Encoding
   ↓
Preprocessing Pipeline
   ↓
Logistic Regression
   ↓
Churn Risk Prediction
```

## 🛠️ Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## 📁 Project Structure

```text
FeatureForge-Data-Preparation/
│
├── Assignment_05_Feature Engineering & Data Preparation.ipynb
└── README.md
```

## 📚 Learning Outcomes

Through this assignment, the following practical concepts are explored:

* Preparing raw data for machine learning
* Creating meaningful features from existing variables
* Handling categorical data
* Converting datetime information into useful features
* Maintaining class distribution during data splitting
* Preventing data leakage during preprocessing
* Building reusable Scikit-learn pipelines
* Preparing data for classification models

## 👩‍💻 Author

**Sabrin Alam**

Computer Science & Engineering
Aspiring AI Engineer & AI Research Enthusiast

---

⭐ *A hands-on exploration of turning raw user data into meaningful, machine-learning-ready features.*
