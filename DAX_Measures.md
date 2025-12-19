# DAX Measures – Retail Sales Dashboard

## Total Revenue
```DAX
Total Revenue = SUMX(Sales, Sales[Quantity] * Sales[Price])
Total Orders = COUNT(Sales[Order_ID])
Average Order Value = DIVIDE([Total Revenue], [Total Orders])
Average Order Value = DIVIDE([Total Revenue], [Total Orders])
Revenue Growth % =
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], PREVIOUSMONTH(Sales[Date])),
    CALCULATE([Total Revenue], PREVIOUSMONTH(Sales[Date])))

