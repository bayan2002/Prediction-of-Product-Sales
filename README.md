# Food Sales Prediction Project

## Project Overview
This project analyzes and predicts sales for products across different outlets.  
The goal is to provide actionable insights and accurate sales predictions to help management optimize inventory and marketing strategies.

---

## Part 1 – Load and Inspect Data
- Load the dataset into a pandas DataFrame.  
- Inspect the dataset using `.info()`, `.head()`, `.shape`, and `.dtypes`.  
- Understand the structure, types, and completeness of the data.  

---

## Part 2 – Clean Data
- Remove duplicate rows to ensure data integrity.  
- Handle missing values:
  - Fill missing numeric values (e.g., `Item_Weight`) with 0.  
  - Fill missing categorical values (e.g., `Outlet_Size`) with 'Unknown'.  
- Standardize text and correct inconsistent categories (e.g., `Item_Fat_Content`).  
- Drop high-cardinality identifiers that do not provide predictive value (e.g., `Item_Identifier`).  
- Verify cleaning with summary statistics and counts.

---

## Part 3 – Exploratory Data Analysis (EDA)
Focuses on **understanding patterns, distributions, and trends** in the data using visualizations.

## Key Insights
### 1. Distribution of Item Outlet Sales
![Sales Distribution](hist_sales_distribution.png)
Interpretation: The distribution of sales is heavily right-skewed, indicating that while most products have moderate sales, a few high-performing items significantly drive revenue.

### 2. Feature Correlation Heatmap
![Correlation Heatmap](heatmap_correlations.png)
Interpretation: There is a moderate positive correlation between Item_MRP and Sales, suggesting that price is a key driver of total income.

---


## Part 4 – Predictive Modeling

### Linear Regression Coefficients
![Linear Regression Coefficients]<img width="1189" height="590" alt="c1" src="https://github.com/user-attachments/assets/caf98857-23df-4ef6-8a79-acba448fcfc6" />


**Top 3 Features:**
1. **Item_MRP (+979.46):** Higher product prices result in higher sales.  
2. **Outlet_Type_Supermarket Type3 (+709.60):** Type 3 supermarkets consistently perform better.  
3. **Outlet_Identifier_OUT027 (+709.60):** This specific outlet has strong sales, likely due to location or size.  

**Negative Impact Features:**  
- Grocery Stores and underperforming outlets decrease predicted sales.  
- Being in a small or low-performing outlet reduces sales potential.

*Summary:* Positive coefficients increase predicted sales, while negative coefficients decrease it. Linear Regression shows that **product price and store type** are strong drivers of sales.

---

### Random Forest Feature Importances
![Random Forest Feature Importances]<img width="1189" height="590" alt="c2" src="https://github.com/user-attachments/assets/f49e8949-4c3f-43a9-b05f-be4e0f558f8e" />


**Top 5 Features:**
1. **Item_MRP (0.5100):** Higher-priced products sell more.  
2. **Outlet_Type_Grocery Store (0.2653):** Outlet type heavily influences sales.  
3. **Item_Visibility (0.0455):** Better shelf visibility improves product sales.  
4. **Outlet_Type_Supermarket Type3 (0.0454):** These outlets consistently perform well.  
5. **Outlet_Identifier_OUT027 (0.0444):** This top-performing outlet sells more than most others.

*Summary:* Random Forest confirms that **price and store characteristics** are the main drivers, while visibility and specific outlet performance also matter. The model captures non-linear patterns missed by Linear Regression.

---

## Final Recommendations for Stakeholders
1. **Focus on high MRP products:** Premium items consistently drive higher sales.  
2. **Optimize outlet strategy:** Promote and invest in high-performing outlets (Type 3 supermarkets and top outlets like OUT027).  
3. **Use shelf placement effectively:** Ensure key products have good visibility to increase sales.  
4. **Strategically manage grocery stores:** Understand why grocery stores underperform and adjust pricing, inventory, or marketing.  
5. **Leverage data-driven decisions:** Continue monitoring sales patterns using these models to guide promotions, inventory, and outlet planning.

---

## Limitations & Next Steps
- Some features have missing values that could affect predictions if not handled carefully.  
- External factors such as regional events or seasonal trends are not included in the model.  
- Next steps: Implement more advanced models, incorporate additional external data, and refine marketing strategies based on predictions.

---

## Contact
For further information, please contact: **bayanabdelbaryq@gmail.com**

---
