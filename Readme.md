# FIFA Player Value-for-Money Clustering

This project explores FIFA player data using **K-Means clustering** to identify groups of players based on both performance and financial metrics. The goal is to uncover which players offer the strongest **value for money**, and how clubs might use data-driven insights to optimize transfer and wage decisions.

---

## 📌 Project Overview

Football clubs frequently overspend on players who fail to match their valuation, while undervaluing hidden talent.  
This project uses **unsupervised learning** to examine how players naturally cluster when combining:

- Age  
- Overall rating  
- Market value  
- Wage  

From this, we identify:

- **Undervalued high performers**  
- **Prime, market-priced stars**  
- **High-potential youth**  
- **Affordable veteran depth**  

We also compute a **custom Value-for-Money Index (VMI)** to validate cluster quality.

---

## 📊 Features Used for Clustering

The following four features were used after cleaning and standardization:

- **Age**
- **Overall Rating**
- **Market Value** (converted from strings like "€42.5M" into numeric amounts)
- **Wage** (converted from "€130K" into numeric values)

All data was scaled with `StandardScaler` to prepare for K-Means.

---

## 📁 Dataset

This project uses official FIFA datasets (e.g., FIFA18, FIFA20).  
Preprocessing includes:

- Removing non-essential columns  
- Filtering out rows with `"€0"` values  
- Converting all monetary fields to float  
- Dropping missing or invalid entries  
- Scaling numeric fields  

Final dataset contains only **numeric** columns suitable for clustering.

---

## 🧠 Methods

### **1. Preprocessing**
- Clean monetary fields (`€xxM/K`)  
- Convert to floats  
- Scale features  
- Remove outliers and zeros  

### **2. Selecting K**
Two approaches were used:

- **Elbow Method**  
- **Silhouette Score**

### **3. Clustering**
K-Means was run on:

- Age  
- Overall  
- Value  
- Wage  

Cluster labels were then assigned back to the original dataframe.


## 📈 Visualizations

The notebook includes:

### **3D Cluster Plot**
A 3D scatter of:
- Overall (X)
- Market Value (Y)
- Age (Z)

Color-coded by cluster.

---

## 🛠 Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-Learn  
- Matplotlib  
- Jupyter Notebook  

---

## 🚀 How to Run

1. Clone this repository  
2. Install dependencies:

   ```bash
   pip install pandas numpy scikit-learn matplotlib

