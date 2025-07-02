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
- The output of the Average Actual Price vs the Average Discount price was plotted on a column chart using Logarithmic values due to the large difference in numbers which made it difficult to see the price differences in some of the categories (with smaller prices) when plotted with the normal figures.

## Exploratory Data Analysis 
---
The Amazon Dataset was explored (using functions, pivot tables and charts) to answer and draw insights from some questions such as:
1. The average discount percentage by product category?

2. Products listed under each category?

3. Total number of reviews per category?

4. Products with the highest average ratings?

5. The average actual price vs the discounted price by category?

6. Products having the highest number of reviews?

7. Products with a discount of 50% or more?

8. Product-ratings Distribution (e.g., how many products are rated 3.0,4.0, etc.)?

9. Total potential revenue (actual_price × rating_count) by category?

10. Unique products per price range bucket (e.g., <₹200,₹200–₹500, >₹500)?
    
11. How does the rating relate to the level of discount?

12. Products having fewer than 1,000 reviews?

13. Which categories have products with the highest discounts?

14. The top 5 products in terms of rating and number of reviews combined.

## Analysis Outputs
---
Some Functions used during the process
- New Product Name Column.
=LET(text, LEFT(B2, 40),clean, PROPER(TRIM(LEFT(text, FIND("@", SUBSTITUTE(text & " ", " ", "@", LEN(text) - LEN(SUBSTITUTE(text, " ", "")))) - 1))),lastWord, TRIM(RIGHT(SUBSTITUTE(clean, " ", REPT(" ", 100)) ,100)), IF(OR(lastWord="For", lastWord="To", lastWord="On", lastWord="In", lastWord="By", lastWord="Of", lastWord="And", lastWord="&"),LEFT(clean, LEN(clean) - LEN(lastWord)- 1),clean))
- Main Category Column.
=IFERROR (LEFT(D2, FIND("|", D2)-1),D2).
