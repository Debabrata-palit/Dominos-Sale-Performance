# Domino's Sale Performance
This repository showcases an **Interactive Power BI Dashboard** visualizig a comprehensive sales analysis for **Domino's Pizza**.

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

Download Dataset [click here](https://github.com/Ayushi0214/Masterclass-Datasets/blob/main/domino's/Dataset.csv)

## DAX Queries Used

> **New Measures:**

```dax
Revenue = SUMX('Dataset','Dataset'[price]*'Dataset'[quality])
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

![image](https://github.com/user-attachments/assets/4df76866-82bd-4759-a517-9b0a1610ec3a)

To See the Live Report [click here](https://app.powerbi.com/view?r=eyJrIjoiOWRmNTdmY2ItY2YwZC00ZWRmLTg0NDctYzAwYmU2MWJjNzVkIiwidCI6IjY0NWY1NDA5LWJkNjAtNDNhMS04ZmVmLTFhODNiNjU3YzIyMCJ9).
