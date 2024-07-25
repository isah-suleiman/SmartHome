# SmartHome

## **Project Overview: Optimizing Supply Chain and Production Planning**

![](assets/images/smarthomeinc.jpg)

### **Business Challenge**

SmartHome Solutions Inc. faces a critical challenge in optimizing its supply chain and production planning. The current approach, based on historical data and market forecasts, presents several obstacles:

1. **Inefficient Production:**
   - Relying on historical data often leads to overproduction or underproduction, resulting in operational inefficiencies and increased costs.
   
2. **Customer Disconnection:**
   - The company lacks a deep understanding of its diverse customer base, making it difficult to align production with specific customer demands.
   
3. **Inventory Management:**
   - Inefficient production planning has led to excess inventory, tying up valuable resources and impacting profitability.

### **Project Significance**

The logistics and supply chain industry is evolving rapidly, necessitating a data-driven approach. Here are the top reasons why this project matters:

1. **Operational Efficiency:**
   - Leveraging customer data streamlines production processes, reduces costs, and optimizes resource allocation.
   
2. **Customer Satisfaction:**
   - Understanding customer preferences enables better product availability and timely deliveries, enhancing overall satisfaction.
   
3. **Competitive Edge:**
   - Data-driven supply chain planning gives SmartHome Solutions Inc. a competitive advantage by adapting quickly to market changes.
   
4. **Cost Savings:**
   - Eliminating overproduction and minimizing excess inventory leads to significant cost reductions.
   
5. **Sustainability:**
   - Accurate production planning aligns with the company's sustainability goals.

### **Project Objectives**

1. **Customer Segmentation:**
   - Profile SmartHome Solutions Inc.'s customer base to gain insights into preferences, buying behaviors, and geographic distribution.
   
2. **Data-Driven Planning:**
   - Enhance production planning, inventory management, and distribution strategies based on customer segments.
   
3. **Customer-Centric Approach:**
   - Improve on-time deliveries, increase customer satisfaction, and align production with customer demands.

### **Data Description**

This case study includes four datasets:

1. **Customer Data:**
   - **Customer_ID:** Unique identifier for each customer.
   - **Age (years):** Customer age.
   - **Gender:** Male, Female, or Other.
   - **Income ($):** Annual income.
   - **Geographic Location:** City or state.

2. **Sales Data:**
   - **Transaction_ID:** Unique identifier for each sales transaction.
   - **Customer_ID:** Links sales to customers.
   - **Product SKU:** Unique product identifier.
   - **Quantity Sold (units):** Number of units sold.
   - **Timestamp:** Date and time of each transaction.
3. **Inventory:**
   - **Product SKU:** Unique product identifier.
   - **Current Inventory Level (units):** Number of units available
   - **Quantity Sold (units):** Number of units sold.
   - **Stockouts (days):** Number of days the product was out of stock
   - **Replenishment Lead Time (days):** Number of days it takes to restock
   - **Storage Location:** The warehouse where a product is located
   - **Shelf Life (days):** How long the product can stay.
4. **Production Schedule Data:**
   - **Production Schedule_ID:** A unique identifier for each production schedule.
   - **Lead Time (days):** The time required for production from order placement to completion.
   - **Production Capacities (units per hour):** The maximum production rate per hour.
   - **Resource Allocation:** Allocation of resources (e.g., machinery, labor) for production.

## **Data Cleaning and Preparation: A Step-by-Step Approach**

1. **Consolidate Data:**
   - Import and consolidate the relevant datasets into Microsoft Excel.
   
2. **Clean Data:**
   - Check for and handle any missing values, duplicates, and inconsistencies.
     - **a. Checking for Missing Values:**
       - Open your Excel dataset.
       - Select the range of data or the entire sheet.
       - Go to the 'Home' tab, click on 'Find & Select,' and choose 'Go To Special.'
       - Select 'Blanks' and click 'OK.' This highlights all empty cells.
     - **b. Find and Remove Duplicates:**
       - Select the range of data or the entire sheet.
       - Go to the 'Data' tab and click on 'Remove Duplicates.'
       - Choose the columns to check for duplicates, then click 'OK.'
       
3. **Data Transformation:**
   - Format and transform data as needed for analysis.
     - **c. Converting Text to Dates:**
       - Use the `=TEXT()` function to split the timestamp columns into date and time components.
       - Convert the date component using the `DATEVALUE()` function to ensure it is in the proper date data type.
       
4. **Checking Data Types:**
   - While Excel doesn't explicitly show data types like a programming language, you can infer:
     - Numbers are right-aligned by default.
     - Texts are left-aligned.

---

**Results:**

1. **Customer Data:**
   - No missing values detected.
   - Data Types: Mostly integers and objects (for categorical data like Gender and Geographic Location).

2. **Inventory Data:**
   - No missing values detected.
   - Data Types: Integers for numerical data and objects for categorical data (Storage Location).

3. **Production Data:**
   - No missing values detected.
   - Data Types: Integers for numerical data and objects for categorical data (Resource Allocation).

4. **Sales Data:**
   - No missing values detected.
   - Data Types: Integers for numerical data; the Timestamp column is an object and needs conversion to a datetime format.
## Up Next

### 1. **Customer Segmentation:**
   - **Objective:** Segment customers based on demographics (age, gender, income) and geographic location.
   - **Why It Matters:** Understanding customer segments helps tailor production and inventory strategies to specific needs.
   - **Action Items:**
     - Analyze customer data to identify distinct groups.
     - Look for patterns or trends within each segment.

### 2. **Inventory and Production Overview:**
   - **Objective:** Assess inventory levels, stockouts, and production capacities.
   - **Why It Matters:** Efficient inventory management ensures optimal resource allocation.
   - **Action Items:**
     - Evaluate current inventory levels.
     - Identify any discrepancies between production and inventory.

### 3. **Sales Analysis:**
   - **Objective:** Understand product preferences and customer buying behaviors.
   - **Why It Matters:** Sales data provides insights into demand patterns.
   - **Action Items:**
     - Analyze sales data to find top-selling products.
     - Understand customer preferences within each segment.

### 4. **Integrating Findings:**
   - **Objective:** Combine insights from customer segmentation, inventory, production, and sales data.
   - **Why It Matters:** Holistic insights drive supply chain optimization.
   - **Action Items:**
     - Propose strategies for efficient production planning and customer-centric supply chain management.

## **Customer Data Analysis and Segmentation**

### **Steps:**

1. **Explore Customer Data:**
   - Examine the distribution of age, gender, income, and geographic location using pivot tables and charts (e.g., histograms and bar charts) in Excel.

2. **Segment Customers:**
   - Create age groups:
     - **Adults:** Ages 18-40
     - **Middle-aged:** Ages 41-60
     - **Seniors:** Ages 61-69
   - Use Excel formulas to categorize each customer based on their age:
     - Formula: `=IF(B2>=60,"Seniors",IF(B2>=41,"Middle-aged","Adult"))`
   - Divide income into brackets (e.g., Low and High):
     - Use Excel's median function to determine the income threshold.
     - Formula: `=IF(D2<=0.8*$K$2,"Low","High")`
   - Demographic segmentation based on age group and income bracket:
     - **Adult + Low:** Type 1
     - **Adult + High:** Type 2
     - **Middle-aged + Low:** Type 3
     - **Middle-aged + High:** Type 4
     - **Senior + Low:** Type 5
     - **Senior + High:** Type 6

3. **Geographic Location:**
   - Geographic location is already present in the data.

4. **Visualize Distribution:**
   - Use Excel charts to visualize the distribution of each segment.

### **Results:**

Based on the exploration of columns, we found the following insights among SmartHome Solutions Inc.'s customers:

1. **Age Distribution:**
   - The age of customers is fairly evenly distributed, with a slight skew towards younger ages. This suggests a diverse range of age groups among the customer base.

2. **Gender Distribution:**
   - There is representation from different gender groups, but males slightly outnumber females. It's important to investigate if certain products or services are preferred by specific gender groups.

3. **Income Distribution:**
   - The income distribution shows variability, which is crucial for understanding purchasing power and preferences.

4. **Geographic Location Distribution:**
   - Customers are distributed across different geographic locations, with a concentration in "City C." This geographic distribution can impact logistics, inventory management, and product preferences.

Based on customer segments, we observed the following:

1. **Age Group Distribution:**
   - There are more adults than middle-aged and senior individuals.

2. **Income Bracket Distribution:**
   - The majority of customers fall under the high-income category.

3. **Demographic Segmentation Distribution:**
   The majority fall under segment Type 2 (adults with high income), while the least common segment is Type 5 (seniors with low income).
   - Regional insights:
     - For City A, Type 1 (adults with low income) dominates, while Type 5 is the least common.
     - For City B, Type 6 (seniors with high income) performs best, while Type 1 is the least common.
     - For City C, Type 1 (adults with high income) is the strongest segment, while Type 6 is the least common.

With these segmentations, we can now analyze sales data to identify product preferences and buying behaviors within each segment. This will help align production with customer demands and optimize inventory management.

## **Dataset Merging and Product Preference Analysis**

### **Steps:**

1. **Merging Datasets:**
   - Use the Power Pivot function in Excel to merge relevant datasets.
   
2. **Analyzing Product Preferences by Customer Segment:**
   - Identify popular products among customer segments and geographic locations.
   - Look for notable trends or patterns in purchasing behavior across these segments.
   
   - **Calculate Top Products for Each Segment:**
     - Create pivot tables in Excel to aggregate sales by product SKU within each customer segment.
     - Use the 'Sum' function in the pivot table to calculate the total sales quantities.
     - Sort the results to identify the top-selling products in each segment.

### **Results:**

The analysis reveals the top-selling products in each segment based on the quantity sold:

1. **Top Products for Each Customer Segment:**
   - **Type 1:** SKUs 21, 56, 20, 69, and 79.
   - **Type 2:** SKUs 36, 83, 41, 93, and 81.
   - **Type 3:** SKUs 83, 78, 99, 67, and 58.
   - **Type 4:** SKUs 89, 9, 90, 77, and 87.
   - **Type 5:** SKUs 90, 35, 61, 19, and 94.
   - **Type 6:** SKUs 87, 80, 78, 8, and 85.

2. **Top Products for Each Geographic Location:**
   - **City A:** SKUs 34, 69, 98, 68, and 14 are leading.
   - **City B:** SKUs 95, 85, 91, 1, and 53 are most popular.
   - **City C:** SKUs 79, 67, 83, 77, and 10 are in high demand.

3. **Sales Trend by Month for High-Value SKUs:**
   - To understand sales trends over time, create a bar chart showing total sales per month in 2026.
   - Focus on the following:
     - Add the Value column from the inventory data to the merged customer-sales data.
     - Select appropriate time intervals (daily, weekly, or monthly) for analysis.
     - Plot sales trends for the top SKUs in each demographic and geographic location.
     - Observe seasonal patterns, growth or decline trends, and significant fluctuations.

### **Observations:**

- In general, sales were highest in January and lowest in March.
- By customer types:
  - Most sales occurred in January for all segments except Type 4, where February had higher sales.
- By customer type for each city:
  - City A: More sales in January, except for Type 3 and Type 6 customers (higher sales in February).
  - City B: January sales dominate, except for Type 5 and Type 6 customers (more sales in February).
  - City C: General trend of more sales in February, except for Type 1 and Type 2 customers (higher sales in January).

## **Dashboard Design, Insights, and Recommendations**

### **1. Dashboard Design:**
   - Create a comprehensive dashboard to consolidate all findings.
   - Visualize key metrics and insights for easy reference.

### **2. Customer Types by Location:**
   - **Objective:** Understand customer popularity in each city.
   - **Visualization:**
     - Bar chart showing customer count by city.
   - **Insight:**
     - Identify which cities have the highest customer base.

### **3. Customer Types by Quantity Sold:**
   - **Objective:** Assess customer buying behavior.
   - **Visualization:**
     - Line chart showing monthly sales trend for each customer type.
   - **Insight:**
     - Observe which customer segments contribute most to sales.

### **4. Sales Quantity by Customer Type (Monthly):**
   - **Objective:** Analyze monthly sales by customer segment.
   - **Visualization:**
     - Stacked bar chart showing sales quantity for each customer type per month.
   - **Insight:**
     - Identify seasonal patterns or trends.

### **5. Current Inventory Levels by SKU:**
   - **Objective:** Assess inventory status.
   - **Visualization:**
     - Heatmap or table showing inventory levels for top SKUs by customer segment.
   - **Insight:**
     - Determine which SKUs need attention (low stock, excess stock).

### **6. Out-of-Stock Analysis:**
   - **Objective:** Identify out-of-stock items and replenishment needs.
   - **Visualization:**
     - Alert or indicator for out-of-stock SKUs.
     - Days until replenishment (if known).
   - **Insight:**
     - Prioritize restocking based on urgency.

### **7. Current Production Capacity by SKU (in Hours):**
   - **Objective:** Understand production capacity.
   - **Visualization:**
     - A bar chart showing the production capacity of each SKU.
   - **Insight:**
     - Ensure production aligns with demand.

### **8. Summary Cards:**
   - Display key metrics:
     - Number of SKUs
     - Number of Customers
     - Total Quantity of SKUs sold
     - Customer Segment breakdown

### **Strategic Recommendations:**
   - Based on insights, consider the following:
     - Adjust production schedules to meet demand.
     - Optimize inventory levels for top-selling SKUs.
     - Prioritize restocking for out-of-stock items.
     - Explore expansion opportunities in high-popularity cities.
    
![supplychain](https://github.com/user-attachments/assets/eeced4e3-2f5a-4148-94cd-f80bd4b86336)


## **Insights and Recommendations for SmartHome Solutions Inc.**

### **General Insights:**

1. **Diverse Customer Base:**
   - The even distribution across different ages and various gender groups indicates a wide-ranging customer base.

2. **Income and Age Group Correlation:**
   - The majority of customers are adults with high incomes, suggesting a focus on SKUs for this customer segment.

3. **Geographic Variability:**
   - Different preferences in different cities highlight the need for region-specific strategies.

4. **Product Preferences by Segment:**
   - Each customer segment (Type 1 to Type 6) exhibits distinct preferences for specific SKUs, emphasizing the importance of tailored product offerings.

5. **High-Value SKUs:**
   - Identifying top SKUs purchased by customers indicates focused demand for specific products.

6. **Sales Variability and Seasonality:**
   - Sales vary across months and locations and are influenced by different customer types.

### **Recommendations:**

1. **Product Strategy:**
   - **Diversification:**
     - Develop products that cater to the diverse needs of different age and income groups.
   - **Tailoring for High-Value SKUs:**
     - Focus production efforts on top SKUs within each customer segment to ensure availability.

2. **Inventory Management:**
   - **Dynamic Stocking:**
     - Adjust inventory levels based on sales trends for high-value SKUs within each customer type.
   - **Regional Focus:**
     - Customize inventory based on regional preferences in Cities A, B, and C.

3. **Marketing and Sales:**
   - **Segment-Specific Campaigns:**
     - Create targeted marketing campaigns for each customer segment, highlighting their preferred SKUs.
   - **Promotional Timing:**
     - Align marketing efforts with peak sales periods to maximize impact.

4. **Production Planning:**
   - **Demand-Driven Production:**
     - Adapt production schedules based on sales trends for top SKUs within each customer segment.
   - **Efficiency in Low-Demand Products:**
     - Adopt lean production practices for lower-value SKUs to minimize excess inventory.

5. **Regional Strategies:**
   - **Localized Offerings:**
     - Customize product offerings and stock levels based on preferences in each city.
   - **Distribution Optimization:**
     - Optimize logistics and distribution to meet unique demands in different geographic locations.

6. **Data-Driven Approach:**
   - **Continuous Monitoring:**
     - Regularly analyze sales data to adapt strategies in real time.
   - **Feedback Loops:**
     - Use customer feedback to refine product offerings and marketing approaches.

7. **Customer Engagement:**
   - **Community Building:**
     - Engage with customer groups to build brand loyalty and gain deeper insights into their preferences.
   - **Responsive Customer Service:**
     - Prioritize excellent service, especially for the dominant adult low-income segment, to foster long-term relationships.

### **Implementation Pathway:**

- **Short-Term:**
  - Focus on inventory adjustments and targeted marketing campaigns for key segments and high-value SKUs.
- **Medium-Term:**
  - Develop and refine products based on customer segment feedback and sales data analysis.
- **Long-Term:**
  - Invest in technology and processes to enhance understanding of customer preferences, enabling agile supply chain management.

By following these recommendations, SmartHome Solutions Inc. can better align its products and services with the diverse needs of its customer base, optimizing both customer satisfaction and operational efficiency.

---
