# Airbnb-Insights-Analysis
Analysis of Airbnb listings in Paris to uncover trends in pricing, host activity, and neighborhood variability, with insights into the impact of regulations and opportunities for strategic decisions.

![image](https://github.com/user-attachments/assets/016d57d8-38ba-43bf-9424-c8da12d9d9e0)

Here’s a comprehensive summary and final report based on the objectives and tasks of your project:

---

**Comprehensive Report on Paris Airbnb Listings Analysis**

### **Objective 1: Data Profiling and Quality Assurance (QA)**
1. **Data Import and Cleaning**:
   - The Airbnb dataset contains 250,000+ listings across 10 cities, with Paris-specific data filtered to **64,690 rows and 5 columns**: `host_since`, `neighbourhood`, `city`, `accommodates`, and `price`.
   - Columns like `host_since` were converted to datetime for easier manipulation.

2. **QA Results**:
   - Missing Data: Only `host_since` had missing values (33 rows), while `neighbourhood`, `city`, `accommodates`, and `price` were complete.
   - Data Statistics:
     - `accommodates`: Ranges from 0 to 16, with an average of 3.
     - `price`: Ranges from 0 to 12,000, with a median of 80 and an average of 113. Some outliers (e.g., luxury listings or potential errors) were noted.
   - Anomalies: Identified **62 rows where price = 0** and **54 rows where accommodates = 0**, which required further investigation.

3. **Action**:
   - Rows where both `price = 0` and `accommodates = 0` were removed to maintain data quality, leaving valid records intact.

---

### **Objective 2: Data Preparation for Visualization**
1. **Average Price by Neighborhood**:
   - Created a table (`paris_listings_neighbourhood`) to group listings by `neighbourhood` and calculate average prices.
   - Notable Insights:
     - Most expensive neighborhoods: **Elysee (€211)**, **Louvre (€176)**, and **Passy (€161)**.
     - Most affordable neighborhood: **Menilmontant (€75)**.

2. **Average Price by Accommodates in the Most Expensive Neighborhood**:
   - Elysee was identified as the priciest neighborhood.
   - Prices for listings accommodating 2–3 people were consistent, while higher accommodations (e.g., 6+) showed price variability.

3. **Trends Over Time**:
   - Created a table (`paris_listings_over_time`) to analyze the number of new hosts and average prices by year.
   - Observations:
     - New hosts grew rapidly between 2008 and 2015, peaking at **12,147 in 2015**.
     - Average prices fluctuated, with a peak in **2009 (€159)** and subsequent stabilization around **€100–120**.

---

### **Objective 3: Data Visualization and Findings**
1. **Visualizations**:
   - **Horizontal Bar Chart (Average Price by Neighborhood)**: Highlighted price disparities across neighborhoods.
   - **Horizontal Bar Chart (Average Price by Accommodates in Elysee)**: Showed trends in pricing by listing size in Paris' most expensive neighborhood.
   - **Dual Axis Line Chart**:
     - Compared new host counts and average prices over time on a single graph.
     - Revealed steady growth in hosts alongside pricing trends.

2. **Impact of 2015 Regulations**:
   - The 2015 peak in new hosts followed by a decline may be linked to regulations introduced to limit short-term rental activity. Prices stabilized post-2015, suggesting market adjustments.
---

### **Conclusion and Recommendations**
1. **Findings**:
   - Paris' Airbnb market showcases a diverse price range across neighborhoods, catering to different customer preferences.
   - The growth in new hosts reflects increasing market interest, but regulations likely curbed expansion after 2015.

2. **Recommendations**:
   - **Hosts**: Focus on mid-range neighborhoods (e.g., Pantheon, Luxembourg) to attract a broader audience.
   - **Policy Makers**: Monitor regulations' impact on affordability and host participation.
   - **Researchers**: Study outliers (e.g., luxury listings) for deeper insights into pricing dynamics.

This project provided invaluable insights into the interplay of price, accommodation size, and host activity over time. Let me know if you'd like to refine any section! 😊
