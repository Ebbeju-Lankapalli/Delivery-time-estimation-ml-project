# 🚀 Food Delivery Time Prediction (ML Project)

## 📌 Overview
This project predicts **food delivery time (in seconds)** using a DoorDash-like dataset. The goal is to estimate delivery duration based on order details, restaurant information, and marketplace conditions using machine learning models.

---

## 🎯 Objective
To build a regression model that accurately predicts food delivery time using real-world features such as order size, demand conditions, and estimated delivery distance.

---

## 🗂️ Dataset Features

### Order Details
- total_items  
- subtotal  
- num_distinct_items  
- min_item_price  
- max_item_price  
- average_item_price  

### Marketplace Conditions
- total_onshift_dashers  
- total_busy_dashers  
- total_outstanding_orders  
- busy_dasher_ratio  
- outstanding_order_ratio  

### Store Information
- store_primary_category  
- store_id (frequency encoded)  
- order_protocol  
- market_id  

### Time Features
- order_hour  
- order_day  
- order_month  
- day_of_week  
- is_weekend  
- meal_period  

### Target Variable
- delivery_duration (in seconds)

---

## 🔧 Workflow

### 1. Data Preprocessing
- Handled missing values  
- Converted timestamps into useful features  
- Encoded categorical variables  
- Removed duplicates and cleaned data  

---

### 2. Feature Engineering
- Busy dasher ratio  
- Outstanding order ratio  
- Average item price  
- Store frequency encoding  
- Time-based features (rush hour, meal period, weekday/weekend)

---

### 3. Outlier Treatment
- Applied percentile-based clipping (1st–99th percentile)  
- Reduced extreme variations while preserving data distribution  

---

### 4. Encoding
- One-hot encoding for categorical variables  
- Frequency encoding for high-cardinality features  

---

## 🤖 Models Used

- Linear Regression  
- Ridge Regression  
- Lasso Regression (Best Model)  
- ElasticNet Regression  
- Support Vector Regression (SVR)  
- K-Nearest Neighbors (KNN)  
- Decision Tree Regressor  

---

## 📈 Final Model Performance

| Metric | Value |
|------|------|
| **MAE** | 152.17 sec |
| **MSE** | 46,718.24 |
| **RMSE** | 216.14 sec |
| **R² Score** | 0.9499 |

---

## 🧠 Key Insights

- Delivery time is strongly influenced by demand-supply imbalance  
- Estimated driving duration and order complexity are key drivers  
- Time-based patterns significantly affect delivery delays  
- Linear models performed best due to strong linear relationships in data  

---

## 🏁 Conclusion

This project demonstrates an end-to-end machine learning pipeline for predicting food delivery time with high accuracy. The final model achieved an **R² score of ~0.95**, indicating strong predictive capability on the processed dataset.

---

## 🚀 Future Improvements

- Deploy as a web app using Streamlit/Flask  
- Experiment with ensemble models (Random Forest, XGBoost)  
- Build real-time ETA prediction API  
