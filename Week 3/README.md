# 🌍 Country Clustering Analysis for HELP International

## 📌 Project Overview
This project was completed as part of the **CEI Internship Program 2026 – Week 3 Assignment**.

The objective is to help **HELP International**, a humanitarian NGO, identify countries that require the most aid by clustering countries based on their socioeconomic and health indicators.

Using **Unsupervised Machine Learning**, countries are grouped into meaningful categories that can support data-driven humanitarian decision-making.

---

## 🎯 Business Objective

HELP International wants to allocate resources efficiently to countries that need aid the most.

By analyzing indicators such as:

- Child Mortality
- Income
- GDP per Capita
- Health Expenditure
- Life Expectancy
- Total Fertility
- Inflation
- Exports & Imports

we can identify groups of countries with similar development levels.

---

## 📊 Dataset

The dataset contains country-level socioeconomic and health-related attributes.

**Target:** No predefined target variable (Unsupervised Learning)

**Rows:** 167 Countries

**Features:** Multiple economic, demographic, and health indicators

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---

## 🔍 Project Workflow

### 1. Data Exploration
- Loaded and inspected the dataset
- Checked data types and descriptive statistics
- Verified missing values

### 2. Exploratory Data Analysis (EDA)
- Correlation Heatmap
- Feature Distribution Analysis
- Outlier Detection using Boxplots

### 3. Data Preprocessing
- Removed non-numeric country names
- Standardized features using **StandardScaler**

### 4. K-Means Clustering
- Applied the **Elbow Method**
- Evaluated candidate values of K
- Compared clustering performance using:
  - Silhouette Score
  - PCA Visualization

### 5. Cluster Validation
- Compared:
  - **K = 3**
  - **K = 4**

Although K=4 produced a slightly better silhouette score, PCA visualization revealed that one cluster contained only a single country.

Therefore:

✅ **K = 3 was selected**

### 6. Alternative Model: DBSCAN
DBSCAN was evaluated using multiple `eps` values.

Observations:
- Excessive noise points
- Unstable cluster formation
- Poor suitability for classifying all countries

❌ DBSCAN was rejected.

---

## 📈 Final Clusters

| Cluster | Label | Characteristics |
|----------|--------|----------------|
| 0 | Developing | Moderate income and development indicators |
| 1 | Developed | High income, high life expectancy, low child mortality |
| 2 | Underdeveloped | Low income, high child mortality, low healthcare access |

---

## 🌍 Key Insights

### 🔴 Underdeveloped Countries
- Highest child mortality rates
- Lowest GDP per capita
- Lowest income levels
- Lowest healthcare expenditure
- Require immediate humanitarian support

### 🟡 Developing Countries
- Moderate economic growth
- Improving healthcare indicators
- Potential candidates for targeted development programs

### 🟢 Developed Countries
- Strong economies
- High life expectancy
- Low child mortality
- Minimal need for humanitarian aid

---

## 📉 Model Comparison

| Method | Result |
|----------|---------|
| K-Means (K=3) | ✅ Selected |
| K-Means (K=4) | ❌ Over-segmented data |
| DBSCAN | ❌ High noise and poor separation |

---

## 🏆 Final Conclusion

The analysis successfully categorized countries into:

- **Developed**
- **Developing**
- **Underdeveloped**

Among the evaluated approaches, **K-Means Clustering with K=3** provided the most meaningful and interpretable segmentation.

These clusters can help **HELP International** prioritize aid distribution and focus resources on countries facing the greatest socioeconomic challenges.

---

## 👨‍💻 Author

**Sankalp Tamboli**  
CEI Internship Program 2026 – Week 3 Assignment

---

⭐ If you found this project useful, consider giving the repository a star!
