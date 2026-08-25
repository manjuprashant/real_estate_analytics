Code

---

## 📗 **calculated_columns.md**
```markdown
# Real Estate Analytics – Calculated Columns

## [Price Category](ca://s?q=Price_Category_Calculated_Column)
**Definition:** Classifies properties into price bands  
**DAX:**
```DAX
Price Category = SWITCH(TRUE(),
    Properties[Price] < 500000, "Low",
    Properties[Price] >= 500000 && Properties[Price] < 1500000, "Mid",
    Properties[Price] >= 1500000, "High"
)
Year
Definition: Extracts year from transaction date
DAX:

DAX
Year = YEAR(Properties[Date])
Month Name
Definition: Extracts month name from transaction date
DAX:

DAX
Month Name = FORMAT(Properties[Date], "MMM")
Location Group
Definition: Groups properties by urban vs suburban
DAX:

DAX
Location Group = SWITCH(TRUE(),
    Properties[City] = "Bengaluru", "Urban",
    Properties[City] = "Mysuru", "Suburban",
    "Other"
)
Profit Category
Definition: Classifies properties based on profitability
DAX:

DAX
Profit Category = IF(Properties[Revenue] > Properties[Cost], "Profitable", "Not Profi