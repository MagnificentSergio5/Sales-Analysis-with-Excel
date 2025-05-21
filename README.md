# Retail Sales Data Analysis

## Overview

This project involves an in-depth analysis of profit performance by products, countries, sales segment, and months to understand patterns and seasonal variations. The objective is to provide actionable insights to help improve business decisions around inventory, marketing, and regional expansion strategies.

Using Microsoft Excel for data cleaning and interactive visualizations, this analysis highlights profit trends over time, products with highest profit, and underperforming sales segment.

## Tools and Technologies

* Microsoft Excel
* PivotTable

## Dataset

* **Source**: Fictional dataset based on real-world retail structures
* **Size**: 700 rows, 14 columns
* **Fields**: Segment, Country, Product, Discount Band, Units Sold, Manufacturing Price, Sales Price, Revenue, COGS, Profit, Date, Month Number, Month Name, Year

---

## Workflow

### 1. Data Cleaning

The analysis started with one of the most crucial features of a data analysis lifecycle: data cleaning.

#### Why Clean Data?

Unclean data leads to errors, incorrect analysis, and poor decision-making. Proper cleaning ensures accuracy, consistency, and efficiency in reporting. In other words, the conclusion from an analysis is as dependable and useful as the quality of the data.

#### Some of the issues encountered include:

* Inconsistent formatting
* Duplicate values
* Blank spaces
* Incorrect data types

---

### To resolve these glaring inconsistencies, I took the following steps:

#### ✅ Adjusting Rows and Columns

I adjusted the column size by highlighting the entire spreadsheet and double-clicking the edge of a column to make all the columns fit to width. This makes the spreadsheet more readable and organized.

#### ✅ Deleting Blank Rows

To remove blank cells, I highlighted the entire spreadsheet and pressed `Ctrl + G` to get to the "Go To Special" feature and clicked the “blank” option. This helped highlight all the blank rows in the dataset. Thereafter, I clicked the drop-down button of “Delete” in the “Cells” ribbon under the “Home” tab and clicked on “Delete Sheet Rows.” This efficiently removed all the highlighted blank rows that can disrupt formulas and analysis, and rows below the deleted rows were subsequently shifted upward. This ensures efficiency.

#### ✅ Removing Duplicates

It is undeniable that duplicate data can skew analysis. To avoid making wrong conclusions based on warped data, I removed duplicate values by using the "Remove Duplicates" tool in Excel to maintain uniqueness.

#### ✅ Clearing Messy Formatting

The data was also inconsistently formatted. There were different font sizes, colors, and cell styles. These can make a spreadsheet hard to read. To correct this error and make the spreadsheet more readable, I highlighted the entire spreadsheet and used the "Clear Formats" option in the editing ribbon under the home tab to reset formatting quickly.

#### ✅ Formatting Columns

Similarly, the date column was formatted as numbers. To make the column reflect the type data type of the records contained therein, I highlighted the entire column and changed it to short date format. The Sales Price, Gross Sales, COGS (cost of goods sold), and profit columns were also converted to currency format.

#### ✅ Converting Numbers Stored as Text to Numbers

Some of the numbers in the Manufacturing Price column were formatted as texts, which made those numbers aligned to the left side of their respective cell instead of the right side. (In an Excel spreadsheet, numbers are aligned to the right side of the cell, while texts are aligned to the left.) To correct this mistake, I typed `1` in an empty cell and then copied it. After copying the value from the cell by pressing `Ctrl + C`, I highlighted the Manufacturing Price column and clicked the drop-down button of “Paste” under the “Home” tab. Subsequently, I clicked on “Paste Special” at the bottom of the paste options and checked the “Multiply” option. This helped align all the numbers to the right, which makes them easy to be recognized as numbers by Excel, instead of as texts.

#### ✅ Changing Case

The records in the Country column were also not consistently formatted. To ensure text consistency, I converted records input as uppercase to proper case by using the `PROPER()` function.

#### ✅ Removing Spaces, Line Breaks, and Non-Printing Characters

The presence of white spaces in the Country column also necessitated the use of `TRIM()` function to clean them up.


### 2. Exploratory Data Analysis (EDA) with the PivotTable:

### PivotTable Analysis

To gain quick insights into regional profit performance, I used **Excel PivotTable** to aggregate and analyze the total profits by country. The steps taken are outlined below:

#### ✅ Steps Taken
1. **Insert PivotTable**:

   * Selected the cleaned dataset.
   * Navigated to the **Insert** tab and clicked **PivotTable**.
   * Chose to place the PivotTable in a **new worksheet** to make it more readable and organized.

2. **Configure PivotTable Fields**:

   * **Rows**: Dragged the `Country` field into the **Rows** area to list each country.
   * **Values**: Dragged the `Profit` field into the **Values** area and ensured it was set to **Sum of Profit**.
   * This aggregated the total profit made in each country.

3. **Sort Data**:

   * Sorted the results in descending order of profit to quickly identify high-performing and underperforming regions.

4. **Format Output**:

   * Applied **Currency formatting** to the profit values for readability.
   * Adjusted column width and layout to make it cleaner and more presentable.

#### 📊 Result

| Country | Sum of Profit |
| ------- | ------------- |
| France  | \$3,781,021   |
| Germany | \$3,680,389   |
| Canada  | \$3,529,229   |
| USA     | \$2,995,541   |
| Mexico  | \$2,907,523   |

This simple yet powerful aggregation made it easy to compare regional performance and identify that **France** had the highest total profit, while **Mexico** recorded the lowest.

> 📌 *Insight*: The USA and Mexico underperformed in terms of profits compared to their European and Canadian counterparts.

### PivotTable Analysis: Profit by Month
Analyzing monthly profit performance reveals seasonal patterns and highlights peak business periods. Below is a breakdown of profits by month:

| Month | Profit      |
| ----- | ----------- |
| Jan   | \$814,029   |
| Feb   | \$1,148,547 |
| Mar   | \$669,867   |
| Apr   | \$929,985   |
| May   | \$828,640   |
| Jun   | \$1,473,754 |
| Jul   | \$923,866   |
| Aug   | \$791,066   |
| Sep   | \$1,786,735 |
| Oct   | \$3,439,781 |
| Nov   | \$1,370,103 |
| Dec   | \$2,717,330 |

> 📌 *Insight*: Profits peaked in **October** and **December**, suggesting heightened consumer activity during these months—possibly due to end-of-year promotions, holidays, or budget cycles. **March** recorded the lowest profit, which may indicate a slower sales period or lower customer demand.


### PivotTable Analysis: Profit by Segment

| Segment          | Sum of Profit |
| ---------------- | ------------- |
| Government       | \$11,388,173  |
| Small Business   | \$4,143,169   |
| Channel Partners | \$1,316,803   |
| Midmarket        | \$660,103     |
| Enterprise       | -\$614,546    |

> 📌 *Insight*: The **Government** segment significantly outperformed all others, generating over **\$11M** in profit. Conversely, the **Enterprise** segment recorded a **loss**, indicating a potential area for investigation or strategic overhaul.

### PivotTable Analysis: Profit by Product

This breakdown highlights the profitability of each product, enabling targeted decisions on inventory and marketing strategies:

| Product   | Profit      |
| --------- | ----------- |
| Amarilla  | \$2,814,104 |
| Carretera | \$1,826,805 |
| Montana   | \$2,114,755 |
| Paseo     | \$4,797,438 |
| Velo      | \$2,305,992 |
| VTT       | \$3,034,608 |

> 📌 *Insight*: **Paseo** stands out as the top-performing product with the highest profit, while **Carretera** recorded the lowest profit, indicating potential areas for reevaluation in pricing, promotion, or distribution.


### 3. Visualization:

Created insightful bar charts, line graphs, and column charts.

Built an interactive dashboard with slicers.

