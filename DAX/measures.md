# Real Estate Analytics – Measures

## [Average Price](ca://s?q=Average_Price_DAX_Measure)
**Definition:** Mean property price across all listings  
**DAX:**
```DAX
Average Price = AVERAGE(Properties[Price])
Price per Sqft
Definition: Price normalized by square footage
DAX:

DAX
Price per Sqft = DIVIDE(SUM(Properties[Price]), SUM(Properties[Sqft]))
Growth %
Definition: Percentage change in property prices over time
DAX:

DAX
Growth % = DIVIDE([Current Period Price] - [Previous Period Price], [Previous Period Price]) * 100
Market Share by Property Type
Definition: Share of each property type in total listings
DAX:

DAX
Market Share = DIVIDE(COUNT(Properties[PropertyID]), CALCULATE(COUNT(Properties[PropertyID]), ALL(Properties[PropertyType])))
Net Revenue
Definition: Revenue minus costs (if available)
DAX:

DAX
Net Revenue = SUM(Properties[Revenue]) - SUM(Properties[Cost])
