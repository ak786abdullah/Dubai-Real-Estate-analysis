# Dubai Real Estate Market Analysis 

##  Project Overview
An exploratory data analysis (EDA) of the Dubai real estate market aimed at identifying profitable investment opportunities. This project involves cleaning a dataset of **39k+ property listings**, engineering features like **Rental Yield**, and validating data integrity using statistical correlation checks.

##   (Data Cleaning)
During initial inspection, I discovered a **negative correlation (-0.25)** between `beds` (number of bedrooms) and `area_sqft`.
* **The Problem:** Mathematically, as bedroom count increases, area should increase. The data defied logic.
* **The Cause:** I found that **37.8%** of the dataset had `0` values for `area_sqft`.
* **The Fix:** I performed rigorous data cleaning to handle these missing values, resulting in a corrected **positive correlation (0.61)**, restoring data integrity.

##  Key Features Engineered
* **Price Per SqFt:** Standardized metric to compare value across different neighborhoods.
* **Rental Yield (ROI):** Calculated as `(Average Rent / Price) * 100`.
    * *Constraint Applied:* Filtered out unrealistic yields (>20%) to remove bad data points.

##  Tech Stack
* **Python:** Pandas, NumPy
* **Statistics:** Correlation matrices, Outlier detection

##  How to Run
1. Clone the repo
2. Install requirements: `pip install -r requirements.txt`
3. Run the notebook in `notebooks/Real_Estate_Analysis.ipynb`
