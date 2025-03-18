### **Project: Predicting Customer Booking Completion for British Airways** ✈️  

#### **Overview**  
This project aims to predict whether a customer will complete a flight booking based on historical booking data from British Airways. Using machine learning models, we analyze customer behavior, booking trends, and key factors that influence booking completion.  

The insights from this model can help optimize marketing strategies, improve customer targeting, and increase booking conversions.  
---

## **🔬 Problem Statement**  
British Airways wants to identify potential customers who are most likely to complete their flight bookings. By predicting customer behavior, the airline can:  
Personalize marketing offers 🎯  
Optimize pricing & promotions 💰  
Improve customer engagement & retention 📈  
---

## **📊 Dataset Description**  
The dataset contains customer booking information, including:  

| Feature | Description |
|----------------------|-----------------------------------------------------------|
| `num_passengers` | Number of passengers in the booking. |
| `sales_channel` | Online, travel agent, or offline booking channel. |
| `trip_type` | One-way or round-trip flight. |
| `purchase_lead` | Days before departure the ticket was booked. |
| `length_of_stay` | Duration of stay at the destination. |
| `flight_hour` | Flight departure time. |
| `flight_day` | Day of the week the flight is scheduled. |
| `route` | Flight route (Origin to Destination). |
| `booking_origin` | Country or city where the booking was made. |
| `wants_extra_baggage` | If the customer requested extra baggage (1 = Yes, 0 = No). |
| `wants_preferred_seat` | If the customer chose a preferred seat. |
| `wants_in_flight_meals` | If the customer ordered an in-flight meal. |
| `flight_duration` | Flight duration in hours. |
| `booking_complete` | **Target variable (1 = Booking Completed, 0 = Not Completed).** |
---

## **🛠️ Methodology**  
**Exploratory Data Analysis (EDA)** – Understanding the dataset, visualizing trends, and identifying imbalances.  
**Data Preprocessing** – Handling missing values, encoding categorical features, and normalizing numerical data.  
**Feature Engineering** – Creating meaningful features like booking time patterns and customer preferences.  
**Handling Class Imbalance** – Since many customers don’t complete bookings (0s > 1s), we used class weighting and SMOTE to balance the dataset.  
**Model Training & Tuning** – Tested multiple models, including:  
   - **Logistic Regression**  
   - **Random Forest** *Best Performing Model*  
**Model Evaluation** – Used Accuracy, Precision, Recall, F1-score, and AUC-PR to find the best-performing model.  
---

## **Key Findings & Results**  
**Class Imbalance Observed** – The dataset had **85% non-bookings (0s) and 15% bookings (1s)**, requiring special handling.  
**Random Forest Performed Best** – Achieved **Accuracy: ~78%**, with a balance between **precision & recall**.  
**SMOTE Did Not Improve Results** – Oversampling led to overfitting in some cases.  
**Class Weighting Helped** – Adjusting class weights improved recall for identifying customers likely to book.  

---

## **Future Improvements**  
🔹 **Improve Feature Engineering** – Extract insights from **booking trends, flight times, and customer history**.  
🔹 **Try Deep Learning Models** – LSTMs or Transformers for better sequential pattern detection.  
🔹 **Optimize Hyperparameters Further** – Fine-tune the model to improve precision-recall trade-off.  
