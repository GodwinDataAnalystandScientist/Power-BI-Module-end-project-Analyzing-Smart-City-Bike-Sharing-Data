Power BI Data Preparation Summary
1. Data Source
File: bike-stations-sharing-data.xlsx
Total Records: 2856
Total Columns: 12
Columns: number, name, address, position, banking, bonus, status, Contract Name, Bike Stands, Available Bike Stands, Available Bikes, Last Update
2. Data Cleaning
Removed extra spaces using Power Query (Trim and Clean).
Standardized column names for better readability.
3. Data Transformation
Converted numeric fields to Whole Number and text fields to Text.
Converted Last Update column to Date/Time and extracted Date for analysis.
4. Duplicate Removal
Removed duplicate records based on StationID using Power Query: Home → Remove Rows → Remove Duplicates.
5. Data Model
Fact Table: Fact_BikeAvailability (StationID, BikeStands, AvailableBikeStands, AvailableBikes).
Dimension Table: DimStation (StationID, StationName, Address, ContractName, Status).
6. Measures
Total Bikes = SUM(AvailableBikes)
Total Bike Stands = SUM(BikeStands)
Available Stand % = DIVIDE(SUM(AvailableBikeStands), SUM(BikeStands))
7. Outcome
Dataset cleaned, transformed, duplicates removed, and optimized for Power BI dashboard reporting.
