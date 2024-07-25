# SmartHome

## **Project Overview: Optimizing Supply Chain and Production Planning**

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
