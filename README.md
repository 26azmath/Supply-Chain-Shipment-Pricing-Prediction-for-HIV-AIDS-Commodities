**Business Problem:**

Global health organizations spend ~$5B annually on HIV/AIDS logistics.
Freight costs vary widely due to shipment mode, weight, insurance, and vendor constraints, making budgeting and procurement inefficient.

**Objective:**
Build a machine learning model to predict freight costs and identify key cost drivers for decision support.

**Dataset Source:** Data.gov (Global Fund & USAID shipments)

Records: ~10,000

Countries: 43

Features: 30 raw → 397 engineered

Target: Freight Cost (USD)

**Technical Approach**

SQL-based data profiling and aggregation

Exploratory Data Analysis (EDA)

Feature engineering (OHE, scaling)

**Model comparison:**

Linear Regression (baseline)

Random Forest Regressor

Evaluation using RMSE and R²

**Key Results**
Model |	RMSE |	R²
Linear Regression	| Extremely high |	Negative
Random Forest |	~8,792 |	~0.70

**Conclusion:**
Random Forest captures non-linear cost drivers and explains ~70% variance.

**Business Insights:**

Air shipments are significantly more expensive.

Weight and insurance cost are dominant predictors.

Product group impacts cost more than vendor or site.

**Tools:** Python, SQL, Pandas, NumPy, Scikit-learn, Tableau, Excel

**Repository Navigation**

/sql: SQL EDA & feature aggregation

/notebooks: End-to-end ML workflow

/reports: Detailed analysis and decisions
