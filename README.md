# **Supply Chain Shipment Pricing Prediction for HIV/AIDS Commodities**

## **Overview**
This project applies machine learning to predict freight costs for global HIV/AIDS commodity shipments. Using real-world logistics data covering multiple countries, shipment modes, and product categories, the analysis identifies key cost drivers and builds predictive models to support cost forecasting and supply chain optimization in global health programs.

**Objective:**  
Predict shipment freight cost and extract actionable insights to support logistics planning, vendor evaluation, and cost optimization.

---

## **Dataset**
- **Source:** Data.gov – Supply Chain Shipment Pricing Data  
- **Records:** ~10,000 shipments  
- **Geographic Coverage:** 43 countries  
- **Manufacturing Sites:** 37  
- **Key Attributes:**  
  - Shipment mode  
  - Product group  
  - Vendor and manufacturing site  
  - Shipment weight and insurance cost  
  - Unit price and total freight cost  

The dataset reflects real-world complexity, including missing values, high-cardinality categorical variables, and non-linear cost behavior.

---

## **Data Preparation & Exploratory Data Analysis (EDA)**
- Removed records with missing **target variable (freight cost)**  
- Imputed missing numerical fields using statistical techniques  
- Encoded categorical variables using **one-hot encoding**  
- Engineered **397 numerical features** from raw shipment attributes  
- Conducted EDA to identify:
  - Cost variation by shipment mode  
  - Product categories with higher logistics expenses  
  - Vendor-level and route-level cost variability  
  - Non-linear relationships between shipment weight, insurance, and freight cost  

EDA results confirmed strong non-linear interactions, motivating the use of ensemble-based models.

---

## **Modeling Approach**

### **Linear Regression (Baseline Model)**
- Implemented as an initial benchmark  
- Failed to capture non-linear cost relationships  
- Performed poorly in high-dimensional feature space  
- Resulted in unstable predictions and negative explanatory power  

### **Random Forest Regressor (Final Model)**
- Captured complex non-linear feature interactions  
- Robust to multicollinearity and high-cardinality encoded features  
- Demonstrated strong generalization on unseen data  
- Selected as the final model based on validation performance  

---

## **Model Performance**

| **Model** | **R² Score** | **RMSE** |
|----------|-------------|----------|
| Linear Regression | < 0 | Extremely High |
| Random Forest Regressor | ~0.70 | ~8,792 |

---

## **Key Findings**
- **Shipment mode** is the strongest cost driver (air freight is significantly more expensive)  
- **Product type and shipment weight** materially influence total freight cost  
- **Vendor and manufacturing site** introduce systematic pricing variability  
- **Ensemble models** substantially outperform linear models for logistics pricing problems  

---

## **Business Impact**
This project demonstrates how predictive analytics can be applied to:
- Forecast logistics costs for large-scale global health supply chains  
- Support vendor comparison and shipment mode selection  
- Improve budgeting and cost optimization decisions  
- Enable data-driven planning for NGOs, governments, and international organizations  

The methodology is transferable to broader supply chain and logistics pricing use cases.

---

## **Technologies Used**
- **Programming:** Python  
- **Data Analysis:** Pandas, NumPy  
- **Machine Learning:** Scikit-learn  
- **Visualization:** Matplotlib  
- **Development Environment:** Jupyter Notebook  

---

## **Repository Structure**
- **notebooks/** – Data exploration, preprocessing, and modeling workflows  
- **reports/** – Analytical summaries and documentation  
- **data/** – Dataset reference (external source)  

---

## **Key Takeaway**
This project highlights the importance of:
- Rigorous data preprocessing and feature engineering  
- Selecting models appropriate for non-linear, high-dimensional data  
- Translating machine learning outputs into actionable supply chain insights  
