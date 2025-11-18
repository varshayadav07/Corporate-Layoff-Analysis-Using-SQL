# Corporate-Layoffs-Analysis-Using-SQL

**Overview:**
This project focuses on analyzing corporate layoff data to uncover patterns, trends, and insights related to layoffs across different companies, locations, and industries. The project is divided into two main phases: Data Cleaning and Exploratory Data Analysis (EDA).

### Data Cleaning

**Objective:**
To prepare the dataset for analysis by removing duplicates, standardizing data, handling null values, and cleaning the data for inconsistencies.

**Steps Involved:**

1. **Create Staging Table:**
   - A staging table was created to work on the raw data while preserving the original dataset.

2. **Remove Duplicates:**
   - Identified and removed duplicate records based on multiple columns using `ROW_NUMBER()` and CTEs.
   - Manual inspection was performed to ensure the correctness of the records before deletion.

3. **Standardize Data:**
   - Fixed inconsistent entries in the `industry` column, such as variations of "Crypto".
   - Standardized the `country` column by removing trailing periods.
   - Converted the `date` column to a proper `DATE` format for consistency.

4. **Handle Null Values:**
   - Null values in the `industry` column were populated from other records where possible.
   - Columns with null values in `total_laid_off` and `percentage_laid_off` were assessed, and unnecessary rows were removed.

5. **Drop Unnecessary Columns:**
   - Columns such as `row_num` used for cleaning purposes were removed from the final dataset.

### Exploratory Data Analysis (EDA)

**Objective:**
To explore the cleaned dataset to identify trends, patterns, and outliers related to layoffs.

**Steps Involved:**

1. **Basic Statistics:**
   - Examined maximum values for `total_laid_off` and `percentage_laid_off` to understand the scale of layoffs.
   - Identified companies with 100% layoffs and investigated their background.

2. **Aggregate Analysis:**
   - Analyzed companies with the highest single-day layoffs and total layoffs over the dataset period.
   - Examined layoffs by location, country, industry, and stage of the company.

3. **Yearly and Monthly Analysis:**
   - Analyzed layoffs per year and identified top companies for each year using ranking.
   - Calculated the rolling total of layoffs per month to observe trends over time.

4. **Advanced Queries:**
   - Used CTEs to rank companies by layoffs each year and calculated rolling totals for more detailed insights.

**Key Findings:**

- **High Impact Layoffs:** Several startups and high-funding companies, like BritishVolt and Quibi, experienced significant layoffs or closures.
- **Geographical Trends:** Layoffs were observed across various countries with detailed insights into the distribution by location and country.
- **Industry Insights:** Certain industries, such as "Crypto," were affected by notable layoffs.
- **Temporal Trends:** Layoffs showed significant trends and patterns when analyzed over years and months, revealing periods of high activity.
