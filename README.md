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

## Conclusion

**CabInsights** is an in-depth exploration project providing a roadmap for analyzing cab-related datasets. The documentation serves as a guide for organizing code and conducting reproducible analyses. Collaborators can use this project to gain insights into the relationships between transactions, customer demographics, and city details.
