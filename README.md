# **🍕 DOMINOS-PREDICTIVE-PURCHASE-ORDER-SYSTEM**  

## **📋 Introduction**  
This project focuses on optimizing Dominos' ingredient ordering process by utilizing historical sales data and ingredient details. The objective is to accurately predict future pizza sales and develop an efficient purchase order system based on these forecasts. This solution will help Dominos maintain adequate ingredient stock to meet customer demand, reduce waste from overstocking, and avoid stockouts that can disrupt operations. By combining predictive modeling with operational planning, the project aims to improve inventory management and streamline the purchasing process.

## **🛠️ SKILLS TAKEAWAY FROM THIS PROJECT:**  
Here’s the updated content with emojis for each component:

- **🧹 Data Cleaning and Preprocessing:** Managing missing data, creating new features, and transforming data for analysis.  
- **📊 Exploratory Data Analysis (EDA):** Visualizing and analyzing sales trends, category distributions, and correlations to gain insights.  
- **🤖 Predictive Modeling:** Building and training machine learning models to forecast future sales.  
- **🍳 Ingredient Analysis:** Estimating ingredient needs based on sales predictions and recipe data.  
- **🛒 Purchase Order Automation:** Automating the generation of purchase orders based on forecasted demand.  
- **📈 Data Visualization:** Designing detailed and interactive visualizations using Matplotlib, Seaborn, and Plotly.  
- **💡 Decision-Making Insights:** Using analytical results to optimize inventory management and enhance supply chain efficiency.  
- **🐍 Python Programming:** Utilizing advanced Python techniques for data analysis, visualization, and modeling tasks.  
- **📓 Jupyter Notebook:** Efficiently documenting and executing tasks within the Jupyter Notebook environment.

# **📊 EDA-REPORT:**  
**Exploratory Data Analysis (EDA) discovers patterns, relationships, and anomalies in the data.**  

- **🍕 Top-Selling Pizzas**  
  - This visualization showcases the 10 best-selling pizzas based on total sales.  
  - It reveals which pizzas are most popular among customers.  
  - The y-axis displays the pizza names, and the x-axis indicates the quantities sold.  

![image](https://github.com/user-attachments/assets/e23d7ef9-8279-47c8-be9e-77645d002b00)




- **🍕 Distribution of Pizza Categories**  
  - This visualization shows how pizza orders are distributed across different categories (e.g., vegetarian, meat-lovers).  
  - It offers insights into customer preferences and trends for each category.  
  - The y-axis lists the pizza categories, while the x-axis represents the number of orders per category.
 
![image](https://github.com/user-attachments/assets/d735537b-452b-492d-86a8-efa4f978956d)


  
- **📅 Sales Trends Over Time**  
  - This visualization presents daily pizza sales over time by converting the order_date column into a datetime format.  
  - It helps uncover trends, seasonal patterns, and sales spikes during the observed period.  
  - The line plot represents the number of pizzas sold each day.  

![image](https://github.com/user-attachments/assets/24a9cc84-7fc7-4754-a03a-2f6fbf817c75)



- **📅 Sales by Day of the Week**  
  - This visualization presents pizza sales categorized by the day of the week.  
  - It helps uncover which days see higher sales, identifying peak days and slower days.  
  - The line plot represents the number of pizzas sold each day of the week.  

![image](https://github.com/user-attachments/assets/ec24e6e1-8e85-4b23-859a-457da1bbeb8e)




## **📊 MODEL COMPARISON: MAPE SCORES**  
- This visualization summarizes total sales by day of the week to determine which days generate the highest revenue.  
- The data is grouped by `day_of_week`, with `total_price` summed for each day.  
- The x-axis displays the days of the week (Monday to Sunday), and the y-axis shows the corresponding total sales.  
- The bar plot highlights trends in customer purchasing behavior over the week.  





   | **Model**   | **MAPE** | **Rank** | **Best/Worst** |
   |-------------|----------|----------|----------------|
   | ARIMA       | 0.1976   | 1        |     Best       |
   | Prophet     | 0.2163   | 2        |                |
   | SARIMA      | 0.2327   | 3        |                |
   | LSTM        | 0.2345   | 4        |     Worst      |


## **📉 ARIMA MODEL FORECASTING:**  
This section outlines the process of utilizing the best-performing ARIMA model to forecast future sales effectively:  
- **📥 Model Loading:** The ARIMA model, which was previously trained and saved as `best_arima_model.pkl`, is loaded to produce precise sales predictions.  
- **🔮 Sales Forecasting:** The loaded model is used to predict sales for the upcoming 7 days (`n_forecast = 7`).

## **📊 RESULT:**  
- The ARIMA model was chosen as the best-performing model for forecasting pizza sales, with a Mean Absolute Percentage Error (MAPE) of **0.1976**. This low error rate reflects the model’s accuracy and dependability in predicting sales trends. The model’s hyperparameters were optimized using AutoARIMA, which automatically selected the optimal values for p (AR order), d (differencing order), and q (MA order) to ensure the best performance and stationarity of the time series data.  
- With this optimized ARIMA model, the project was able to forecast future sales with high accuracy, facilitating the creation of efficient purchase orders and precise ingredient planning. This approach helps reduce waste, avoid stockouts, and streamline inventory management.
