# Excel Dashboard Project: Layoffs Analysis

This project is based on a dataset originally sourced from Kaggle. The goal is to analyze layoffs across various industries, countries, and company stages using an interactive Excel dashboard.

## Files Included:
- Tech Layoff Dashboard.xlsx`: The Excel file containing the dashboard and all data visualizations.
- `layoff_dataset.xlsx`: The original dataset used for analysis.

## Data Modifications and Processing:
The following steps were taken to preprocess and clean the data:

1. **Data Import**:
   - Imported the data as a CSV file, originally sourced from Kaggle.

2. **Filtering**:
   - Applied filters to columns, enabling drop-down lists for easier navigation and data slicing.

3. **Data Inspection**:
   - Briefly examined column values for duplicates or misspellings, especially in the `Country` and `Continent` columns.

4. **Date Formatting**:
   - Converted the date column format from digits to `MM/DD/YYYY` for consistency.

5. **New Columns Creation**:
   - Added two new columns for `Month` and `Year` by using Excel’s `TEXT()` and `YEAR()` functions, allowing further slicing of data by these variables.

6. **Exclusion of 2024 Data**:
   - I decided not to include layoffs data for 2024, as it only covered the first six months. I wanted to focus the analysis on full, completed years to provide a more consistent and reliable view of trends over time.

7. **Percentage Laid Off Calculation**:
   - Created a new column for the percentage of employees laid off, using the formula:
     ```excel
     =([@[Company Size before Layoffs]] - [@[Company Size after Layoffs]]) / [@[Company Size before Layoffs]]
     ```

## Data Visualization:
The dashboard was designed with the following key components:

1. **Pivot Tables**:
   - Used pivot tables to summarize the total number of laid-off employees across different dimensions.

2. **Unique Observations**:
   - Utilized the `COUNTA(UNIQUE())` function to create cards that display the total count of unique observations for relevant metrics (e.g., companies, countries).

3. **Dashboard Design**:
   - Created text boxes to showcase aggregate data, such as:
     - Number of companies affected
     - Total layoffs
     - Affected industries
     - Countries impacted by layoffs

<img width="442" alt="Screenshot 2024-09-13 092620" src="https://github.com/user-attachments/assets/6aa799ed-4b31-4691-816c-44059cb7b373">

4. **Interactive Charts**:
   - Incorporated slicers for `Year`, `Country`, `Company`, `Industry`, and `Stage` to enable dynamic filtering.
   - Utilized various chart types, including:
     - **Bar charts**: To compare layoffs across countries and industries.
     - **Pie charts**: To visualize the proportion of layoffs by industry.
     - **Line charts**: To track layoffs over time.

## How to Use:
1. Download the `Tech Layoff Dashboard.xlsx` file.
2. Open the file in Excel to explore the interactive dashboard, pivot tables, and slicers for a detailed view of the layoffs data.

## Dataset:
- **Source**: Kaggle (https://www.kaggle.com/datasets/ulrikeherold/tech-layoffs-2020-2024)
- **Contents**: Data on company layoffs, including company size, layoffs, industry, and country.
