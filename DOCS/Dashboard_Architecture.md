🏗️ Dashboard Architecture
1. Purpose
The dashboard architecture defines how data flows from source systems into Power BI, how relationships are modeled, and how KPIs are calculated and visualized. It ensures scalability, accuracy, and usability for stakeholders.

2. Data Sources
Property Listings Dataset: Location, property type, square footage, price, amenities

Transaction Records: Historical sales and rental data

External Data (Optional): Market indices, demographic data, geospatial layers

3. ETL Process
Data Extraction: Import datasets from CSV/Excel/SQL sources

Transformation: Cleaning, encoding, normalization

Loading: Data imported into Power BI model

4. Data Model
Fact Table: Transactions (price, date, property ID)

Dimension Tables:

Property details (type, size, amenities)

Location (city, neighborhood, coordinates)

Time (year, month, quarter)

Relationships:

One-to-many between dimensions and fact tables

Star schema for optimized querying

5. Calculated Columns
Defined in calculated_columns.md:

Price Category

Year, Month Name

Location Group

Profit Category

6. Measures (KPIs)
Defined in measures.md:

Average Price

Price per Sqft

Growth %

Market Share by Property Type

Net Revenue

7. Dashboard Components
KPI Cards: Display core metrics (Average Price, Growth %, Market Share)

Clustered Bar Charts: Compare property types across locations

Line Charts: Show price trends over time

Heatmaps: Highlight demand hotspots

Interactive Filters: Drill-down by location, property type, and amenities

8. Security & Access
Role-based access for stakeholders (Investor, Developer, Analyst)

Row-level security applied for location-specific data

9. Maintenance
Weekly data refresh

Quarterly review of DAX measures

Version control maintained in GitHub repository