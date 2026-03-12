# -CODING-SAMURAI-INTERNSHIP-TAS
Here is a **much stronger GitHub README (Portfolio Level)** for your EDA project. This version looks **more professional, recruiter-friendly, and portfolio ready**.

You can copy this directly into **README.md**.

---

# 🏡 Airbnb Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on an Airbnb dataset to identify patterns, trends, and key factors affecting listing prices.

The objective of this project is to practice **data cleaning, feature understanding, and data visualization** using Python while extracting meaningful insights from real-world data.

This project is part of my **Data Science Portfolio for internship opportunities**.

---

# 🎯 Project Objectives

* Understand the structure of the Airbnb dataset
* Clean and preprocess real-world messy data
* Perform **exploratory data analysis (EDA)**
* Identify **factors influencing Airbnb prices**
* Visualize relationships between important features

---

# 📊 Dataset Information

The dataset contains information about **Airbnb listings**, including:

| Feature            | Description                                   |
| ------------------ | --------------------------------------------- |
| price              | Listing price                                 |
| room_type          | Type of room (Entire home, Private room etc.) |
| property_type      | Type of property                              |
| bedrooms           | Number of bedrooms                            |
| bathrooms          | Number of bathrooms                           |
| beds               | Number of beds                                |
| host_response_rate | Host response percentage                      |
| city               | Listing location                              |

---

# 🛠️ Tech Stack

| Tool             | Purpose                   |
| ---------------- | ------------------------- |
| Python           | Programming language      |
| Jupyter Notebook | Data analysis environment |
| Pandas           | Data manipulation         |
| NumPy            | Numerical operations      |
| Matplotlib       | Data visualization        |
| Seaborn          | Statistical visualization |

---

# 📂 Project Workflow

## 1️⃣ Data Collection

The dataset was loaded using **Pandas**.

```python
import pandas as pd

df = pd.read_csv("airbnb.csv")
```

---

# 2️⃣ Data Understanding

Initial dataset exploration included:

* Dataset shape
* Column names
* Data types
* Summary statistics

```python
df.shape
df.info()
df.describe()
```

---

# 3️⃣ Data Cleaning

Real-world datasets often contain missing values and inconsistent formats.

### Handling Missing Values

```python
df.fillna({
    'bedrooms': df['bedrooms'].median(),
    'bathrooms': df['bathrooms'].median(),
    'beds': df['beds'].median()
}, inplace=True)
```

---

### Converting Host Response Rate to Numeric

```python
df['host_response_rate'] = df['host_response_rate'].astype(str)
df['host_response_rate'] = df['host_response_rate'].str.replace('%','')
df['host_response_rate'] = pd.to_numeric(df['host_response_rate'])
```

---

### Removing Duplicate Records

```python
df.drop_duplicates(inplace=True)
```

---

# 📈 Exploratory Data Analysis

Several visualizations were created to understand the dataset.

### Price Distribution

Analyzes how listing prices are distributed.

### Room Type Distribution

Shows the most common room types.

### Property Type Analysis

Identifies the most frequently listed property types.

### Price vs Room Type

Compares pricing differences between different room categories.

### Bedrooms vs Price

Explores how the number of bedrooms affects listing price.

### Correlation Heatmap

Identifies relationships between numerical variables.

---

# 🔍 Key Insights

Key findings from the analysis:

✅ **Entire homes/apartments generally have higher prices** compared to private rooms.

✅ **Listings with more bedrooms tend to have higher prices.**

✅ **Certain property types dominate Airbnb listings.**

✅ Some numerical variables show **strong correlations with price.**

---

# 📁 Project Structure

```
Airbnb-EDA-Project
│
├── airbnb.csv
├── airbnb_eda.ipynb
└── README.md
```

---

# 🚀 How to Run This Project

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/airbnb-eda-project.git
```

### 2️⃣ Navigate to the project folder

```bash
cd airbnb-eda-project
```

### 3️⃣ Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4️⃣ Open the notebook

```
airbnb_eda.ipynb
```

---

# 📊 Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis
* Data Visualization
* Feature Understanding
* Data Interpretation

---

# 👨‍💻 Author

**Anshul Srivastava**

MBA Student | Data Scientist Intern

💡 Skills:

* Python
* SQL
* Data Analysis
* Machine Learning
* Data Visualization
