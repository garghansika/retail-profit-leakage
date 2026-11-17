# Retail Profit Leakage Analysis

I analysed the Superstore sales dataset in Power BI to find where this retail business is losing profit, and how much it could recover.

![Dashboard](dashboard.png)

## The question
Where is the business losing money, and what would fixing it be worth?

## What I found
- Total sales were about $2.30M and total profit about $286K, a margin of 12.5%.
- Discounts above 20% are the main problem. Those 1,393 order lines (about 14% of all lines) lost around $135K combined.
- Profit is positive for orders with no discount or up to 20% off, and turns negative from 21% upward. It gets worse the higher the discount goes.
- Tables is the biggest loss-making sub-category (about -$17.7K). Without a discount it makes money, and almost all of the loss comes from orders discounted above 20%.
- The Central region has the lowest margin (7.9%) and the highest discounting. The West has the best margin (14.9%) and rarely discounts above 20%.
- If discounts were capped at 20%, profit could rise by roughly $135K to $179K. This assumes sales volume stays the same, so it is an upper estimate. The assumptions are in memo.md.

## What I did
1. Loaded the CSV (9,994 rows, 21 columns) into Power BI and checked it. There were no blanks and no duplicates.
2. Fixed the data types, including the US-format dates.
3. Added Profit Margin %, Order Year, Order Month and a Discount Band column (no discount, up to 20%, 21-40%, over 40%).
4. Looked at profit by sub-category, region and discount band.
5. Built a one-page dashboard with four KPI cards, three charts and slicers for year, region and category.
6. Wrote a short memo with my recommendation.

## Files in this repo
- `README.md` - this file
- `memo.md` - one-page recommendation
- `Sample - Superstore.csv` - the dataset
- `retail-profit-leakage.pbix` - the Power BI file
- `dashboard.png` - screenshot of the dashboard

## Tools
Power BI Desktop (Power Query and DAX)

## Data
Superstore sales dataset from Kaggle, covering 2014 to 2017. It is sample data, not a real company.

## About me
Hansika Garg, B.Tech Information Technology, VIT Vellore
