This project is centered around the analysis of **Pizza Sales and Customer Data**. It involves multiple datasets that, when combined, can provide comprehensive insights into sales performance, customer demographics, product details, and return trends.

Here's a detailed description of the project and the potential work that can be performed:

### Project Description

The project aims to provide a holistic view of a pizza business's operations through data analysis. It combines transactional sales data with various lookup tables for customer, product, and calendar information, along with data on product returns.

### Project Components (Files and their Contents)

* [cite_start]**`pizza_sales.csv` and `pizza_sales_excel_file.xlsx - pizza_sales.csv`**: These are the core transactional datasets[cite: 44352, 89039]. They contain detailed records of each pizza sold, including:
    * `pizza_id`: Unique identifier for each pizza item in an order.
    * `order_id`: Identifier for the overall customer order.
    * `pizza_name_id`: Short code for the pizza type.
    * `quantity`: Number of pizzas of that type in the order.
    * `order_date`: Date of the order.
    * `order_time`: Time of the order.
    * `unit_price`: Price of a single pizza.
    * `total_price`: Total price for the quantity of that pizza type in the order.
    * `pizza_size`: Size of the pizza (e.g., M, L, S).
    * `pizza_category`: Category of the pizza (e.g., Classic, Veggie, Supreme, Chicken).
    * `pizza_ingredients`: A list of ingredients for the pizza.
    * `pizza_name`: Full name of the pizza.

* [cite_start]**`Calendar Lookup.csv`**: This file contains date information[cite: 11]. It's primarily used for temporal analysis, allowing for sales trends to be analyzed over specific periods.

* [cite_start]**`Customer Lookup.csv`**: This dataset provides demographic information about customers[cite: 48303]. Key fields include:
    * `CustomerKey`: Unique identifier for each customer.
    * `Prefix`, `FirstName`, `LastName`, `EmailAddress`: Personal identification.
    * `BirthDate`, `MaritalStatus`, `Gender`, `TotalChildren`: Demographic details.
    * `AnnualIncome`, `EducationLevel`, `Occupation`, `HomeOwner`: Socioeconomic information.

* [cite_start]**`Product Lookup.csv`**: This file contains basic product information[cite: 91202]. It includes:
    * `ProductKey`: Unique identifier for a product.
    * `ProductSubcategoryKey`: Links to product subcategories.
    * `ProductSKU`: Stock Keeping Unit.
    * `ProductName`: Name of the product.

* [cite_start]**`Returns Data.csv`**: This dataset tracks product returns[cite: 91386]. It contains:
    * `ReturnDate`: Date of the return.
    * `TerritoryKey`: Geographic territory where the return occurred.
    * `ProductKey`: Identifier for the returned product.
    * `ReturnQuantity`: Number of units returned.

* **`Product Categories Lookup.csv` and `Product Subcategories Lookup.csv`**: These files are currently empty, indicating that detailed categorization beyond what is in `pizza_sales.csv` might not be available or needs to be populated.

* **`Sales (Unpivot).csv`**: This file is also empty, suggesting it might have been intended for a specific pivoted sales view that is not yet generated or provided.

### Potential Project Work and Analysis

With these datasets, the project can involve various analytical tasks and generate valuable business insights:

* **Sales Trend Analysis**:
    * Identify daily, weekly, monthly, and annual sales patterns and total revenue by analyzing `total_price` and `quantity` from `pizza_sales.csv` over time, using `order_date` and `Calendar Lookup.csv`.
    * Determine peak sales periods (e.g., specific days of the week or times of day) using `order_time`.
    * Analyze sales performance by `pizza_category` and `pizza_size`.

* **Product Performance Analysis**:
    * Identify top-selling and least-selling pizzas by quantity and revenue.
    * Understand the popularity of different pizza ingredients and combinations by analyzing the `pizza_ingredients` field.
    * Track the performance of individual products using `Product Lookup.csv` in conjunction with sales data.

* **Customer Segmentation and Behavior**:
    * While a direct link (customer ID) from `pizza_sales.csv` to `Customer Lookup.csv` is not immediately apparent, if such a link can be established or inferred, it would allow for analysis of sales patterns based on customer demographics (e.g., income, education, marital status).
    * Understand the purchasing habits of different customer segments.

* **Returns Analysis**:
    * Calculate return rates and identify products with high return rates using `Returns Data.csv` and `Product Lookup.csv`.
    * Analyze return trends over time to identify any recurring issues.

* **Data Management and Integration**:
    * Perform data cleaning, transformation, and validation across all datasets to ensure data quality.
    * Integrate data from various CSV files using common keys (e.g., joining sales data with calendar data on date, or returns data with product lookup on product key) for comprehensive analysis.
    * Develop data models and dashboards for visualization of key performance indicators (KPIs) and trends.

This project provides a robust foundation for a data-driven approach to understanding and optimizing a pizza business.
