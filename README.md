# E-Commerce Delivery Time Prediction using Machine Learning

# Description
This project predicts **delivery time (in days)** for e-commerce orders using machine learning techniques.  
The prediction is made at the time of order placement using product, location, and logistics-related features.

The project demonstrates a **complete end-to-end ML workflow**, including data preprocessing, exploratory data analysis (EDA), feature engineering, scaling, model training, and evaluation.

---

#  Problem Statement
Accurate delivery time estimation is critical for e-commerce platforms to:
- Improve customer experience
- Set realistic delivery expectations
- Optimize logistics operations

The goal of this project is to predict the number of **delivery days** for each order.

---

# Dataset Overview
- Dataset size: **50,000 rows**
- Dataset type: **Synthetic but realistic**
- Target variable: `delivery_days`

# Features include:
- Product details: category, price, weight  
- Location details: city, GPS coordinates, distance  
- Logistics details: shipping mode, festival season, weather delay  
- Order date information

⚠️ The dataset is synthetic and follows predefined logistics rules. This is acknowledged during evaluation.

---

# Exploratory Data Analysis (EDA)
EDA was performed to understand delivery behavior and identify important factors affecting delivery time.

Key findings:
- Shipping mode strongly influences delivery duration
- Longer distance leads to increased delivery time
- Festival seasons and weather delays cause noticeable delays
- Product price has minimal impact on delivery speed

---

#  Feature Engineering
Feature engineering was applied to improve model learning:
- Extracted date-based features from `order_date`:
  - `order_day`
  - `order_month`
  - `order_weekday`
  - `is_weekend`
- Removed the original date column after extraction
- Applied one-hot encoding for categorical variables

---

# Feature Scaling
Numeric features were scaled using **StandardScaler** for models sensitive to feature magnitude.  
Scaling was applied only on training data to prevent data leakage.

---

# Model Used
# Random Forest Regressor
Random Forest was selected because:
- It handles non-linear relationships effectively
- It performs well on structured tabular data
- It is robust to feature interactions

---

# Model Evaluation
The model was evaluated using:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score
- Actual vs Predicted comparison plots

# Evaluation Note
Very high evaluation scores were observed due to the deterministic nature of the synthetic dataset, where delivery time is strongly defined by logistics rules. This behavior is documented for transparency.

---

# Key Learnings
- Feature engineering is more impactful than model selection
- Extremely high accuracy can indicate deterministic data
- Proper handling of dates and scaling is essential
- Evaluation metrics must always be interpreted in context

---

# Future Improvements
- Add real-world noise to simulate uncertainty
- Convert regression to SLA classification (on-time vs delayed)
- Introduce multi-warehouse routing
- Test on real-world logistics datasets

---

## Author
**Shifa Tk**  


---

## ⚠️ Disclaimer
This project uses **synthetic data for educational purposes**.  
Results may not directly generalize to real-world production systems.
