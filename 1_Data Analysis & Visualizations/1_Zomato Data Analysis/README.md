# 🍽️ Zomato Data Analysis Using Python

## 📌 Project Overview

This project analyzes the Zomato restaurant dataset using Python to uncover customer preferences and restaurant trends. The goal is to generate business insights that can help restaurant owners and stakeholders make data-driven decisions.

### Key Questions Answered

* Do more restaurants provide online delivery compared to offline services?
* Which restaurant types are most popular among customers?
* What price range do couples prefer for dining out?
* How do restaurant ratings differ between online and offline ordering options?
* Which restaurant received the highest number of votes?

---

## 📊 Dataset Information

The dataset contains information about restaurants, including:

| Column Name                 | Description                           |
| --------------------------- | ------------------------------------- |
| name                        | Restaurant name                       |
| online_order                | Online ordering availability (Yes/No) |
| book_table                  | Table booking availability            |
| rate                        | Restaurant rating                     |
| votes                       | Number of customer votes              |
| approx_cost(for two people) | Estimated cost for two people         |
| listed_in(type)             | Restaurant category/type              |

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 📂 Project Workflow

### 1. Import Required Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### 2. Load Dataset

```python
df = pd.read_csv("Zomato_data.csv")
```

### 3. Data Cleaning

The `rate` column contains values such as `4.1/5`. These values were converted into float format.

```python
def handleRate(value):
    value = str(value).split('/')
    value = value[0]
    return float(value)

df['rate'] = df['rate'].apply(handleRate)
```

### 4. Data Exploration

* Checked dataset structure using `df.info()`
* Verified missing values using `df.isna().sum()`

---

## 📈 Analysis & Findings

### 1. Restaurant Type Distribution

A count plot was used to identify the most common restaurant categories.

**Finding:**
Dining restaurants represent the largest category in the dataset.

---

### 2. Votes by Restaurant Type

Customer votes were aggregated by restaurant type.

**Finding:**
Dining restaurants received the highest number of votes, indicating greater customer preference.

---

### 3. Most Voted Restaurant

```python
max_votes = df['votes'].max()
```

**Finding:**
🏆 **Empire Restaurant** received the highest number of customer votes.

---

### 4. Online Order Availability

The distribution of restaurants offering online ordering was analyzed.

**Finding:**
Most restaurants do not provide online ordering services.

---

### 5. Ratings Distribution

A histogram was used to visualize restaurant ratings.

**Finding:**
Most restaurants have ratings between **3.5 and 4.0**.

---

### 6. Cost Preference for Couples

The approximate cost for two people was analyzed.

**Finding:**
Most couples prefer restaurants with an average cost of **₹300**.

---

### 7. Online vs Offline Ratings

A boxplot compared ratings of restaurants with and without online ordering.

**Finding:**
Restaurants offering online ordering generally received higher ratings than those that did not.

---

### 8. Restaurant Type vs Online Ordering

A heatmap was created to analyze the relationship between restaurant type and online ordering availability.

**Finding:**

* Dining restaurants are more likely to receive offline orders.
* Cafes tend to receive more online orders.
* Customers generally prefer in-person dining at restaurants but online ordering from cafes.

---

## 📊 Visualizations Included

* Count Plot of Restaurant Types
* Votes by Restaurant Type
* Online Order Availability Count Plot
* Ratings Distribution Histogram
* Cost Distribution for Couples
* Online vs Offline Rating Boxplot
* Restaurant Type vs Online Order Heatmap

---

## 🎯 Key Insights

✅ Dining restaurants dominate the market.

✅ Empire Restaurant is the most popular based on customer votes.

✅ Most customers prefer restaurants with moderate pricing.

✅ Online ordering is associated with better restaurant ratings.

✅ Customer behavior differs between restaurant categories and ordering methods.

---

## 🚀 Future Improvements

* Perform sentiment analysis on customer reviews.
* Build interactive dashboards using Power BI or Tableau.
* Create machine learning models to predict restaurant ratings.
* Analyze location-wise restaurant performance.
* Develop recommendation systems for restaurant suggestions.

---

## 📧 Author

**Alamgir Hossen**

Aspiring Data Analyst | Data Science & Machine Learning Enthusiast

GitHub:(https://github.com/alamgirDroid)

