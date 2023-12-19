# CabInsights
CabInsights is a GitHub repository dedicated to the comprehensive analysis and exploration of diverse datasets related to cab transactions, customer demographics, and city details. The project aims to derive valuable insights by investigating the interconnections among the datasets and performing field transformations.

## Investigation and Understanding

### 1. Cab_Data.csv

#### Field Names and Data Types:
- **Transaction_ID**: Unique identifier for each transaction (int).
- **Date of Travel**: Date when the transaction occurred (datetime).
- **Company**: Cab company name (string).
- **City**: City where the transaction took place (string).
- **KM Travelled**: Distance traveled in kilometers (float).
- **Price Charged**: Amount charged for the cab service (float).
- **Cost of Trip**: Cost of the trip for the cab company (float).
- **Customer ID**: Unique identifier linking to customer details (int).
- **Payment_Mode**: Payment mode used (string).

#### Relationships:
- **Customer ID** links to **Customer_ID.csv**.
- **Transaction ID** links to **Transaction_ID.csv**.

### 2. Customer_ID.csv

#### Field Names and Data Types:
- **Customer ID**: Unique identifier for each customer (int).
- **Gender**: Gender of the customer (string).
- **Age**: Age of the customer (int).
- **Income (USD/Month)**: Monthly income of the customer (int).

#### Relationships:
- **Customer ID** links to **Cab_Data.csv** and **Transaction_ID.csv**.

### 3. Transaction_ID.csv

#### Field Names and Data Types:
- **Transaction ID**: Unique identifier for each transaction (int).
- **Customer ID**: Unique identifier linking to customer details (int).
- **Payment_Mode**: Payment mode used (string).

#### Relationships:
- **Customer ID** links to **Cab_Data.csv** and **Customer_ID.csv**.

### 4. City.csv

#### Field Names and Data Types:
- **City**: City name (string).
- **Population**: Population of the city (int).
- **Users**: Number of cab users in the city (int).

#### Relationships:
- **City** potentially links to **Cab_Data.csv**.

## Project Implementation

### Joining Data:
- **Cab_Data.csv**, **Customer_ID.csv**, and **Transaction_ID.csv** should be joined based on the common keys (**Customer ID** and **Transaction ID**).
- **City.csv** may be joined with other datasets based on the **City** field.

### Appending Data:
- If there are multiple datasets for different periods, appending vertically may be considered.

## Field/Feature Transformations

### Cab_Data.csv:
- **Date of Travel**: Convert to datetime format.
- **KM Travelled**, **Price Charged**, **Cost of Trip**: Ensure numerical data types.
- Potential creation of new features, such as profit margin.

### Customer_ID.csv:
- **Income (USD/Month)**: Convert to numerical data type.
- Create new features like age groups.

### City.csv:
- **Population**, **Users**: Ensure numerical data types.
- Normalize or scale numerical features if required.

### Hypotheses to Investigate:

1. **Seasonality in Cab Usage:**
   - **Hypothesis:** The number of customers using the cab service exhibits seasonality, with higher demand during specific months or times of the year.
   - **Investigation:** Analyze the monthly or quarterly trends in cab usage to identify any recurring patterns.

2. **Company with Maximum Cab Users:**
   - **Hypothesis:** One of the cab companies consistently has a higher number of users compared to the other during a specific time period.
   - **Investigation:** Explore the transaction data to determine which company has the maximum number of cab users, and if this varies over time.

3. **Effect of Time on Cab Usage:**
   - **Hypothesis:** The number of cab users varies across different times of the day, with peak usage during specific hours.
   - **Investigation:** Analyze transaction data by time of day to identify peak usage periods and potential factors influencing them.

4. **Relationship between Margin and Number of Customers:**
   - **Hypothesis:** The profit margin increases proportionally with an increase in the number of cab customers.
   - **Investigation:** Examine the relationship between the number of customers and the profit margin to determine if there is a consistent trend.

5. **Demographic Attributes of High-Value Customers:**
   - **Hypothesis:** Certain demographic attributes, such as higher income or age group, are associated with being high-value cab customers.
   - **Investigation:** Explore customer demographics and transaction data to identify attributes of segments with higher usage and spending.

6. **Effect of City Population on Cab Usage:**
   - **Hypothesis:** Cities with higher populations tend to have more cab users.
   - **Investigation:** Analyze the relationship between city population and the number of cab users to understand if there's a correlation.

7. **Payment Mode Preference by Time of Day:**
   - **Hypothesis:** The preferred payment mode for cab services varies based on the time of day.
   - **Investigation:** Examine the distribution of payment modes across different times of the day to identify any patterns or preferences.

### Methodology:

1. **Data Preparation:**
   - Clean and preprocess the datasets, ensuring consistency and accuracy.
   - Create additional features if needed for analysis.

2. **Exploratory Data Analysis (EDA):**
   - Visualize trends in cab usage over time, by company, and other relevant factors.
   - Calculate summary statistics to identify patterns and outliers.

3. **Statistical Analysis:**
   - Perform statistical tests to validate or reject hypotheses.
   - Utilize correlation analysis to explore relationships between variables.

4. **Segmentation Analysis:**
   - Segment customers based on demographics and usage patterns.
   - Identify characteristics of high-value customer segments.

5. **Time Series Analysis:**
   - Use time series analysis techniques to identify seasonality and trends in cab usage over time.

6. **Profitability Analysis:**
   - Examine the relationship between the number of customers and profit margins.
   - Consider factors influencing profitability.


## Conclusion

**CabInsights** is an in-depth exploration project providing a roadmap for analyzing cab-related datasets. The documentation serves as a guide for organizing code and conducting reproducible analyses. Collaborators can use this project to gain insights into the relationships between transactions, customer demographics, and city details.
