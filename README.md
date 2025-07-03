# DSA_PROJECT AMAZON
---
## PROJECT TITLE
---
Amazon Product Review Analysis.
## PROJECT OVERVIEW
---
Amazon Product Review Analysis is a data analytics project focused on extracting insights from Amazon product listings and customer reviews. 

This project is a detailed Exploratory Data Analysis on an Amazon Product Review dataset involving data collection and careful study, data cleaning and processing, exploration (analysis based on single variables, and relationship between two or multiple variables), and Visualizations. 

The goal is to identify trends in pricing, discounts, and customer feedback/engagements (rating, rating counts) by products and category to support data-driven decision-making. Using Microsoft Excel, the project delivers key performance metrics and visualizations to highlight product performance and customer behavior.

## DATA SOURCE
---
The dataset used in this project originates from Amazon’s publicly available product and review data, and was provided through our incubator hub facilitators for educational and analytical purposes.

## TOOLS USED 
---
- Microsoft Excel for date cleaning, Analysis and visualization building.
- GitHub for portfolio building.

## DATA CLEANING AND PREPARATION 
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

## EXPLORATORY DATA ANALYSIS
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

## ANALYSIS OUTPUTS
---
Some Functions used during the process
- New Product Name Column.
=LET(text, LEFT(B2, 40),clean, PROPER(TRIM(LEFT(text, FIND("@", SUBSTITUTE(text & " ", " ", "@", LEN(text) - LEN(SUBSTITUTE(text, " ", "")))) - 1))),lastWord, TRIM(RIGHT(SUBSTITUTE(clean, " ", REPT(" ", 100)) ,100)), IF(OR(lastWord="For", lastWord="To", lastWord="On", lastWord="In", lastWord="By", lastWord="Of", lastWord="And", lastWord="&"),LEFT(clean, LEN(clean) - LEN(lastWord)- 1),clean))
- Main Category Column.
=IFERROR (LEFT(D2, FIND("|", D2)-1),D2).

Below are som pictorial extract from the analysis showing the pivot tables and the dashboard built by converting the pivot tables into charts.
- ![image](https://github.com/user-attachments/assets/826de7fe-a5c6-4c2f-9626-95f130067b95)
- ![image](https://github.com/user-attachments/assets/1b392438-392e-47c1-830a-24e3fd530e13)
- ![image](https://github.com/user-attachments/assets/b452dcff-c104-45a9-9990-32018d4abc78)

## ANALYSIS INTERPRETATIONS
---
- The Electronics Category had the highest Reviews and Potential Revenue implying that it had the highest purchase and customer engagement.
- Discount Increment and Rating were not directly proportional as some products were rated poorly despite having a higher discount, this implies that the rating was done in accordance to the product performance and customer satisfaction.
- A total of 1,234 products were rated high having a rating between 3.9 to 5.0 as against the total product number of 1,465. This implies that a large number of product performed greatly (good quality and customer satisfaction).
- Also, the analysis showed that the prices were not a problem to the customer but the needs of the customers, performance of the product and customers satisfaction, a clear example is seen between the bottom two categories (toys&games, and homeimprovement) and the too two categories (Electronics and Home&Kitchen) in terms of prices. The top two however had higher Potential Revenue and Reviews (customer engagement) compared to the bottom two despite the large difference in price.

## RECOMMENDATIONS
---
Below are some recommendations based in the insights drawn: 

- Focus on High-Engagement Categories Prioritize Electronics, Home & Kitchen, and Computer Accessories for marketing and inventory decisions.

- Refine Discount Strategy
Avoid excessive discounting (>50%) where possible, as it may affect product perception and average ratings.

- Increase Reviews for Low-Visibility Products
Launch post-purchase review campaigns and highlight under-reviewed high-quality items.

- Promote Top-Rated Products by Featuring the highest-rated items in ads, banners, or promotional emails to earn/drive trust and conversions.

- Support Niche Categories
Use niche-targeted campaigns to uplift low-performing categories like Toys & Games and Cars & Motorbikes (such as influencers).

- Build Company-Customer relationship to gain customer loyalty and trust by sending feedbacks to customers based on their rating and reviews.

## ABOUT ME
---
I'm Rachel Adenike Adebowale, a passionate Data Analyst, HND in Science Laboratory Technology (Chemistry) from Petroleum Training Institute. I’m skilled in tools like Microsoft Excel, Word, PowerPoint, Power BI, and SQL, and I enjoy uncovering insights from data to solve real-world problems.

Beyond analytics, I'm also a Drama Minister Who loves God passionately with a strong drive to contribute meaningfully to the Oil and Gas sector through innovation, research, and data-driven solutions.

I'm open to professional opportunities, collaborations, and faith-based engagements that align with my purpose and technical growth.

### CONTACTS 
---
📧 Email: adenikke2004@gmail.com

📞 Phone: +234 901 429 2606

