# Domino's Sale Performance
This repository showcases an **Interactive Power BI Report** visualizig a comprehensive sales analysis for **Domino's Pizza**.

![image](https://github.com/user-attachments/assets/b0f5eb21-e401-4d82-b247-4028d144d84a)

## Business Questions:

1️⃣ What is the total revenue generated from all pizza orders?  
2️⃣ What are the monthly sales trends for Domino’s pizzas?  
3️⃣ What is the distribution of orders across different hours of the day?  
4️⃣ Which days of the week have the highest and lowest sales?  
5️⃣ What is the average order value per customer?  
6️⃣ What is the peak order time during the day?  
7️⃣ Which pizza category (e.g., Classic, Veggie, Supreme) generates the most revenue?  
8️⃣ What are the best-selling pizzas based on quantity sold?  
9️⃣ Are there any seasonal trends in pizza sales (e.g., higher sales on weekends or certain months)?  
🔟 Which size of pizza is ordered the most?

## Dataset

[Download Dataset](https://github.com/user-attachments/files/18668857/Dataset.csv)

## DAX Queries Used

> **New Measures:**

```dax
Revenue = SUMX('Dataset','Dataset'[price]*'Dataset'[quantity])
```
```dax
Avg Order Value = ([Revenue]/DISTINCTCOUNT('Dataset'[order_id]))
```

> **New Columns:**

```dax
Month = MONTH('Dataset'[order_date])
```
```dax
Day of Week = WEEKDAY('Dataset'[order_date])
```
## Dashboard

![powerbi_report](https://github.com/user-attachments/assets/a89a3cfd-2549-4c69-bde4-58b566ea59d8)

To See the Live Report [click here](https://app.powerbi.com/view?r=eyJrIjoiOWRmNTdmY2ItY2YwZC00ZWRmLTg0NDctYzAwYmU2MWJjNzVkIiwidCI6IjY0NWY1NDA5LWJkNjAtNDNhMS04ZmVmLTFhODNiNjU3YzIyMCJ9).
