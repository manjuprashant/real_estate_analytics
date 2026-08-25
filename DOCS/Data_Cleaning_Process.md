Data Cleaning Process
1. Purpose
To ensure consistency, accuracy, and reliability of the real estate dataset before applying analytics and building dashboards.

2. Initial Assessment
Checked for missing values in key columns (Profession, Work_Experience, Var_1, Location, Price).

Identified duplicate records and inconsistencies in categorical fields.

Reviewed numerical ranges for outliers (extreme property sizes or prices).

3. Cleaning Steps
Missing Values

Imputed categorical nulls with mode (most frequent value).

Imputed numerical nulls with median values.

Dropped records with excessive missingness (>40%).

Duplicates

Removed exact duplicates based on PropertyID.

Standardized categorical entries (e.g., “Apartment” vs “Apt”).

Outlier Treatment

Applied IQR method for price and square footage.

Winsorized extreme values to reduce skewness.

Encoding

Label encoding for binary categories (e.g., Parking: Yes/No).

One-hot encoding for multi-category fields (Property Type, Location).

Scaling

Standardized numerical features (Price, Sqft) using z-score normalization.

Ensured consistency across Train and Test datasets.

4. Validation
Verified consistency between Train and Test datasets.

Checked distributions post-cleaning to confirm no bias introduced.

Ensured categorical encoding matched across datasets.

5. Documentation
Cleaning rules applied consistently across Train and Test datasets.

Steps logged for reproducibility in Python scripts (data_cleaning.py).

Summary report generated for transparency.