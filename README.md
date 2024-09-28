## Data Assessment Report
Quality Issues
NULL Values:
Tax 5% * Issue: 9 rows with missing values. * Action: Replace with calculated value: Total - (Price * Quantity).
Total: * Issue: 3 rows with missing values. * Action: Replace with calculated value: Price * Quantity + Tax.
Currency Symbols:
Customer Type: * Issue: 27 rows have non-standard entries. * Action: Replace with 'Normal'.
Time Format:
Time: * Issue: 1 row with time format '8:30 PM'. * Action: Standardize all time formats to 'HH:MM * AM/PM' (e.g., '01:27:00 PM').
Data Types:
UnitPrice: * Issue: 5 rows contain 'USD' as a suffix , Column is of type object instead of float. * Action: Remove 'USD' and Convert UnitPrice from object to float.
Duplicate Rows:

Issue: 6 duplicate rows.
Action: Drop duplicate rows.
Outliers:

Quantity: * Issue: 3 outliers with negative values [-8, -7, -1]. * Action: Replace negative values with their absolute values.
Tax 5%: * Issue: 7 values deemed as outliers [49.49, 49.65, 48.605, 49.26, 48.75, 48.685, 48.69]. * Action: No action required, values are not outliers.
Total: * Issue: 9 values in the range [1003.59, 1039.29, 1042.65, 1002.12, 1020.705, 1034.46, 1023.75, 1022.385, 1022.49]. * Action: No action required, values are not outliers.
Rating: * Issue: 1 outlier with value [97.]. * Action: Replace with 9.7.
Tideness Issues
Create a new column (branch_city)
Create a new column named branch_city by check on each city if its 1 but its name.
