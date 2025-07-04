# Amazon_Review_Analysis_DSA

This Project analyzes Amazon product reviews using Excel to uncover insights that can guide product improvement, marketing strategies and customer engagement to ultimately drive more sales and generate more revenue.

## Project Description

A total of **1,465 Amazon products** were analyzed across multiple categories; covering pricing, discount trends, ratings and customer engagement indicators.

### Dataset Info
- **Source**: Web-Scraped Amazon Data
- **Records**: 1,465 rows
- **Fields**: 16
- <a href='https://github.com/chukwuemeliela/Amazon_Review_Analysis_DSA/blob/main/Amazon_Product_Review_DSA.xlsx'>View Excel File<a/>

### Business Questions Answered
1. Average discount by category
2. Number of products per category
3. Total reviews by category
4. Top-rated products
5. Average actual vs discount price
6. Most-reviewed products
7. Products with ≥50% discount
8. Rating distribution
9. Potential Revenue
10. Product count per price range
11. Rating vs discount trebd
12. Products with less than 1000 reviews
13. Categories with the highest discounts
14. Top 5 products (rating + review count)

## Analysis Tools

- **Excel**: Formulas, Conditional Formatting, Pivot Tables, Charts
- **Power Query**: For advanced data cleaning and transformation
- **Dashboard Features**: KPI cards, slicers, category filtering

## Data Cleaning Summary

To maintain the integrity of the source data, all cleaning was done on a copy of the original dataset. The following steps were carried out:

- **Duplicate Removal**: Based on the unique Product ID, 114 duplicate rows were removed leaving **1,351 unique products**.

- **Fields Reduction**: Fields not needed for the analysis were deleted to streamline the dataset.

- **Data Type Consistency**: Each column was checked and formatted correctly (numbers, general, accounting).

- **Missing and Inaccurate Values**: Two blank values in the 'Rating Count' column were replaced with 0, rather than deleted because it was noted that such replacement would not impact the analysis as significantly as total row deleting would.
Also, a non-numeric character "/" in the 'Rating' column was replaced with 0 and interpreted as **N/A** during analysis.

- **Category Cleanup (Power Query)**: The 'Product Category' field was cleaned and restructured to isolate parent categories. Used Power Query's **Split Column**, **Replace Values**, and **Text.Trim** to format and remove subcategories.

- **New Fields Created**:
    - Sort Order column
    - Price and Discount Range Buckets
    - Rating Score combining rating and review count
  
## Analysis

### Calculated Columns & Formulas
- **Rounded Rating**: Used 'MROUND' to round ratings to the nearest 0.5 to achieve a more defined rating range.

- **Potential Revenue**: Calculated as 'Actual Price x Rating Count' with a total of **₹113+ billion**.

- **Discount %**: Recalculated using the products actual prices vs discount prices to ensure maximum accuracy of data.

- **Bucketed Data**: Used
    - '=VLOOKUP' for price and discount grouping.
    - '=COUNTIF' to identify products with ≥50% discount (**653**) and less than 1000 reviews (**310**).
    - **Rating Scores**: Comined rating and number of reviews to rank products

### Pivot Tables
To answer the business questions, various pivot tables were created to group and summarize the dat. These tables allowed for quick aggregation and comparison across product categories, price ranges, discount levels, and customer engagement metrics.

### Anlaysis Interpretation
- **Top-Rated Products**: Products in the **Electronics** category dominate the list, with three achieving a perfect **5.0** rating.

- **Most Reviewed Product**: 'Amazon Basics Flexible HDMI Cable' (Product ID: 'B07KSMBL2H'), **Electronics** Category is the most reviewed product with a total review of **426,973**.

- **Top Products by Rating Score**: Top 5 products all came from **Electronics**, based on a comnibed score factoring rating and number of reviews.

- **Highest Discounted Product Category**: **Computer & Accessories** have the highest discount of **94.12%**, followed closely by **Electronics** with 91% discount.

- **Price Range With Most Product**: Products sold for **<₹1000** has the most products of **738** products.

- **Category With the Highest Potential Revenue**: **Electronics** has the highest Potential revenue of over **₹91+ Billion**.

- **Most Rating**: **789** products has an average rating of **4.0** (ranging from 3.8 - 4.2)

- **Most Reviewed Category**: **Electronics** is the most reviewed category with a total of **14,208,406** reviews.

- **Category With the Highest Number of Products**: **Electronics** with **490** products has the highest number of products.

- **Category With the Highest Average %Discount**: **Home Improvement** with **57.94%** discount has the highest average % discount.

## Visualizations

### Charts
The dataset was visualized using a variety of charts:
- Bar Charts
- Clustered Columns
- Line Charts
- KPI Cards.

### Dashoard
A dashboard was designed in Excel incorporating the charts above, along with slicers and KPI cards for interactivity.
<a href=h>View Dashboard,<a/> 

## Conclusion
