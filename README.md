# DSA_project-Amazon
## Project Title
---
Amazon Product Review Analysis.
## Project Overview 
---
Amazon Product Review Analysis is a data analytics project focused on extracting insights from Amazon product listings and customer reviews. 

This project is a detailed Exploratory Data Analysis on an Amazon Product Review dataset involving data collection and careful study, data cleaning and processing, exploration (analysis based on single variables, and relationship between two or multiple variables), and Visualizations. 

The goal is to identify trends in pricing, discounts, and customer feedback (rating, rating counts) by products and category to support data-driven decision-making. Using Microsoft Excel, the project delivers key performance metrics and visualizations to highlight product performance and customer behavior.

## Data Source
---
The dataset used in this project originates from Amazon’s publicly available product and review data, and was provided through our incubator hub facilitators for educational and analytical purposes.

## Tools Used 
---
- Microsoft Excel for date cleaning, Analysis and visualization building.
- GitHub for portfolio building.

## Cleaning and Preparation 
---
The following steps were taken to clean and prepare the dataset for Analysis 
- Duplicate Check (No duplicate was found)
- Seven New Columns were created namely:
  1. New Product Name (using a combination of multiple excel functions involving LET,TEXT,LEFT,PROPER,TRIM,CLEAN,FIND,SUBSTITUTE,LEN,RIGHT, AND REPT to reduce the length of the product name)
  2. Main Category (this was also done by using a combination of IFERROR, LEFT AND FIND functions).
  3. Potential Revenue (Sum function).
  4. Price Range (IF function)
  5. Review Tier (< or > 1000 reviews( IF function)).
  6. Discount >=50% (IF function).
  7. Rating and Review together (SUM function).
- Data type was checked and changed where necessary.
- Columns involving money were formatting and currency signs added (Actual price, Discounted price, price range, and Potential revenue).
- Two rows under the rating Count Column were replaced with zeros (0) because they were blank and the actual figures ware not gotten (rows "284" and "326").
- Row "1281" under the Rating Column had a sign "|" instead of a value, o had to replace with an imaginary value of "4.1".
