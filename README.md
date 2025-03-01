
# 📦 Predicting Delivery Delays 🚛
## 📌 Problem Statement:
Timely delivery is crucial for customer satisfaction and business efficiency. Delays in outbound deliveries can lead to missed sales, increased operational costs, and reduced consumer trust.
Currently, delivery performance is influenced by factors such as:

* Invoice processing time
* Outbound logistics constraints
* Warehouse & supply chain inefficiencies

## Objective:
 The goal is to create a prediction model that can
 assess the possibility of delivery delays using past sales,
 delivery (IOD)data. By detecting key patterns and risk
 factors, the model enables firms to take preventative
 measures to increase delivery efficiency.

 ## 📊 Dataset Description  

The dataset consists of multiple features that influence delivery performance:  

| 🔢 **Feature Name**          | 📌 **Description** |
|----------------------------|------------------|
| 📦 **Product**             | Type of product being delivered  |
| 📆 **Month**               | Month of the transaction |
| 🏭 **Supplying_Plant_Code** | Unique identifier for the supplying plant |
| 🚚 **Channel**             | Distribution channel (`E-com`, `MT`, `Normal Trade`) |
| 🏢 **Sales_Office_ID**     | ID of the sales office handling the order |
| 🧾 **Invoice_No**         | Unique invoice number for the transaction |
| 📅 **Invoice_Date**       | Date when the invoice was generated |
| 🏙️ **Ship_to_Code_City**  | City where the order is being delivered |
| 🔄 **OBD_No**            | Outbound delivery number |
| 🔢 **QTY**                | Quantity of items in the order |
| 💰 **Sales_Value**        | Total value of the sale |
| 🏬 **Supplying_Plant_City** | Location of the supplying plant |
| 🏙️ **Sales_Office_City** | City of the sales office |
| 🧾 **Billing_Amount**     | Total amount billed to the customer |
| ⏳ **Delivery_Days**      | Time taken for delivery (target variable) |
| ⚠️ **Delivery_Delayed**  | Whether the delivery was delayed (`1: Yes`, `0: No`) |

## ⚙️ Methodology
1️⃣ Data Preprocessing
* Handling missing values with forward & backward filling.
* Converting date columns to datetime format for better analysis.
* Feature engineering: Delivery lead time, invoice processing time.

2️⃣ Exploratory Data Analysis (EDA)
* 📊 Visualized delivery trends across different months & locations.
* 🔍 Correlation analysis to find key factors affecting delays.
* 📈 Identified patterns in sales & logistics bottlenecks.

3️⃣ Model Training & Evaluation

🤖 Trained multiple ML models:
* Decision Tree
* Random Forest

📉 Evaluation Metrics Used:
Accuracy, Precision, Recall, F1-score.

## 🏆 Model Comparison  

| **Model**             | **Training Accuracy** | **Testing Accuracy** | **Observations** |
|----------------------|------------------|------------------|------------------------|
|  Decision Tree | 98.21%            | 94.56%            | Balanced performance |
| Random Forest       | 98.21%            | 95.82%            | Tends to overfit |

## 📌 Key Takeaways
✅ Invoice processing time and Outbound logistics time are major contributors to delays.

✅ Random Forest achieved the highest accuracy but was prone to overfitting.

✅ AdaBoost provided the best trade-off between accuracy and generalization.

✅ Feature engineering played a key role in improving model performance.

## 🚀 Future Improvements
*  Hyperparameter tuning for better model optimization.
* Including real-time tracking data from IoT sensors.
* Deploying the model using Flask or Streamlit for real-time predictions.
* Expanding dataset to consider external factors like weather, traffic, and demand fluctuations.
