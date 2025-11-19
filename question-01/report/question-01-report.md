## Question 1: Used Car Data Analysis

The goal of this analysis was to clean and preprocess a used car dataset and perform various data manipulation operations.

### Part A: Missing Values

- The `New_Price` column was found to have over 86% missing values. Due to this high proportion, imputing values would introduce significant bias, so the column was dropped.
- Other columns (`Mileage`, `Engine`, `Power`, `Seats`) had negligible missing values (<1%). The rows containing these missing values were removed to maintain data integrity without significantly reducing the dataset size.

### Part B: Unit Removal

- Units were successfully removed from `Mileage` (kmpl/km/kg), `Engine` (CC), and `Power` (bhp) columns.
- These columns were converted to numerical types for analysis. Rows with 'null bhp' were handled by converting to NaN and subsequently dropping them.

### Part C: One-Hot Encoding

- Categorical variables `Fuel_Type` and `Transmission` were converted into numerical binary columns using one-hot encoding (e.g., `Fuel_Type_Diesel`, `Fuel_Type_Petrol`, `Transmission_Manual`).

### Part D: Feature Engineering

- A new feature `Current_Age` was created by subtracting the `Year` of manufacture from the current year. This provides a more intuitive measure of the car's age.

### Part E: Data Manipulation

- **Selection & Filtering**: A subset of cars with `Price` > 10 Lakhs was selected.
- **Renaming & Mutation**: Columns were renamed for clarity, and a new `Price_Thousands` column was calculated.
- **Aggregation**: The data was grouped by `Location` to calculate the average price of these premium cars (>10 Lakhs).
- **Results**: The summary shows that **Coimbatore** and **Bangalore** have the highest average prices for used cars in this segment (approx. 27-28 Lakhs), while **Jaipur** and **Ahmedabad** have lower averages (approx. 18 Lakhs).
