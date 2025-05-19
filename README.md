# Housing Data Cleaning and Preparation Using SQL

## Overview

The Housing Data Cleaning and Preparation project utilizes SQL Server to transform raw Nashville housing data into a structured, clean dataset suitable for detailed analysis. The project specifically addresses common data quality issues such as inconsistent date formats, incomplete addresses, improper field formatting, and duplicate records. By resolving these issues, the dataset becomes reliable for subsequent analytical tasks, helping stakeholders make informed real estate decisions.

## Purpose

The project's primary purpose was to enhance the usability and analytical potential of housing market data by systematically identifying and correcting inconsistencies, missing values, formatting errors, and duplicates within the data. This robust data cleaning process ensures the integrity and accuracy of the information, facilitating meaningful insights into housing market trends.

## Problems Addressed

This project addressed critical data quality issues:

* Standardized inconsistent date formats to ensure accurate date-based analyses.
* Populated missing address information, enhancing dataset completeness.
* Split compound address fields into structured, analyzable columns.
* Standardized field entries (e.g., changing "Y"/"N" to "Yes"/"No").
* Removed duplicate records to maintain dataset accuracy and uniqueness.

## Technology Stack

* **SQL Server:** Chosen for its powerful data manipulation capabilities, including aggregation, joins, conditional logic, string manipulation, and window functions.
* **Excel:** Used for initial exploratory analysis and quick validation of cleaned data.

## Project Execution

### Step-by-Step Technical Process

1. **Initial Data Exploration**

   * Conducted preliminary data assessment in SQL to identify key areas needing improvement (missing data, inconsistencies, duplicates).

2. **Data Cleaning and Standardization Using SQL**

   * **Date Format Standardization:** Utilized SQL date conversion functions to standardize all date entries into a uniform format.
   * **Populating Missing Data:** Implemented JOIN operations and conditional logic (ISNULL) to populate missing property addresses based on matching ParcelIDs from other records.
   * **Splitting Compound Address Fields:**

     * Leveraged SQL string functions (SUBSTRING, CHARINDEX) to split the 'PropertyAddress' into separate columns for address and city.
     * Employed PARSENAME and REPLACE functions to separate 'OwnerAddress' into individual columns for street, city, and state.
   * **Standardizing Categorical Data:**

     * Applied CASE statements to standardize inconsistent categorical data entries (e.g., converting "Y" and "N" in the 'SoldAsVacant' field to "Yes" and "No").
   * **Removing Duplicate Records:**

     * Utilized Window Functions (ROW\_NUMBER) with PARTITION BY logic to identify and eliminate duplicate rows based on critical attributes such as ParcelID, PropertyAddress, SalePrice, SaleDate, and LegalReference.

3. **Final Dataset Refinement**

   * Dropped unnecessary columns ('OwnerAddress', 'TaxDistrict', 'PropertyAddress', 'SaleDate') to streamline the dataset for analysis.

4. **Validation and Exploratory Analysis in Excel**

   * Imported cleaned SQL data into Excel to perform final data validation checks and exploratory analysis, ensuring readiness for detailed analytical tasks.

## Key Outcomes

* Achieved a clean, consistent, and analytically ready dataset.
* Enhanced data integrity and reliability through systematic cleaning processes.
* Provided structured data suitable for detailed analysis, forecasting, and decision-making in real estate contexts.

## Real-world Implications

This robust data cleaning project equips real estate analysts, investors, and policymakers to:

* Perform accurate and reliable housing market analyses.
* Develop informed investment and strategic decisions based on clean, structured data.
* Gain insights into housing market trends and opportunities.
