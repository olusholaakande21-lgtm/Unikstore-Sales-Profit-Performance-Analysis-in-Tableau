# Unikstore Sales & Profit Performance Analysis in Tableau

An interactive Tableau project analysing 9,994 Superstore records from 2014 to 2017 to investigate sales growth, profitability, discount impact, product performance, and regional differences.

The project combines two dashboards—Sales Performance and Profitability Analysis—to identify opportunities for improving business performance.


### Business Problem

Revenue growth does not always translate into sustainable profitability. Businesses need to understand which products, customer segments, regions, and pricing practices contribute to profit and which undermine financial performance.

This project investigates:

- How did sales and profit change between 2014 and 2017?
- Which product categories and sub-categories generated the highest and lowest profits?
- How were discount levels associated with profitability?
- Which regions and states performed well or poorly?
- Which customer segments contributed most to revenue?
- What actions could improve profitability?

## Dashboard 1: Sales Performance


*<img width="923" height="413" alt="Sales Dashboard" src="https://github.com/user-attachments/assets/47309efd-75d0-4e55-b7b7-3ee9ff2c331a" />


The Sales Dashboard presents:

- Total Sales
- Total Profit
- Order count
- Profit Margin
- Sales trends from 2014 to 2017
- Top customer performance
- Sales by customer segment
- Sales by product category

## Dashboard 2: Profitability Analysis

<img width="929" height="415" alt="Profit Dashboard" src="https://github.com/user-attachments/assets/359b4765-dcb5-4fd7-aa11-367164f637fb" />


The Profit Dashboard explores:

- Profit by region
- Profit by sub-category
- Profit by discount classification
- Profit by state
- Loss-making products
- Differences in profitability across geographic markets

## Key Performance Indicators

| Metric | Result |
|---|---:|
| Total Sales | Approximately $2.297M |
| Total Profit | Approximately $286K |
| Overall Profit Margin | Approximately 12.45% |
| Records Analysed | 9,994 |
| Distinct Customers | 793 |
| Analysis Period | 2014–2017 |

*Figures are rounded where indicated. The profit margin should be calculated from the underlying total profit and total sales values.*

## Analytical Workflow

### 1. Data Preparation

- Connected Tableau to the Superstore Excel dataset.
- Reviewed dimensions, measures, and date fields.
- Retained all 9,994 records.
- Prepared the data for trend, product, geographic, and customer analysis.

### 2. Calculated Fields

**Profit Margin**
```text
SUM([Profit]) / SUM([Sales])
```

**Average Order Value**
```text
SUM([Sales]) / COUNTD([Order ID])
```

**Discount Classification**
```text
IF [Discount] > 0.20 THEN "High Discount"
ELSE "Low Discount"
END
```

Core KPIs included Total Sales, Total Profit, order count, and customer count.

### 3. Exploratory Analysis

- Monthly and annual sales trends.
- Sales and profit by category and sub-category.
- Identification of loss-making product lines.
- Profitability by region and state.
- Sales by customer segment.
- Customer revenue ranking.
- Comparison of high- and low-discount groups.

### 4. Dashboard Development

Developed two interactive Tableau dashboards using KPI cards, trend charts, product comparisons, geographic visualisations, and customer analysis.

## Key Findings

### Sales Growth

- Sales increased from approximately $484K in 2014 to $733K in 2017.
- Sales grew by approximately 51% between 2014 and 2017.
- Profit increased from approximately $49.5K to $93.4K, representing growth of about 89%.
- The overall profit margin was approximately 12.45%.

### Product Category Performance

- Technology generated approximately $836K in sales and $145K in profit.
- Furniture generated approximately $742K in sales but only $18K in profit.
- Furniture's profit margin was approximately 2.5%.

### Loss-Making Products

| Sub-category | Sales | Profit |
|---|---:|---:|
| Tables | $207K | −$17.7K |
| Bookcases | $115K | −$3.5K |
| Supplies | $47K | −$1.2K |

Copiers, Phones, and Accessories were among the strongest profit contributors.

### Discount Impact

Transactions with discounts above 20% generated approximately $363K in sales but recorded a combined loss of about $135K.

Transactions with discounts of 20% or less generated approximately $422K in profit.

This indicates a strong association between high discount levels and negative profitability in the dataset, although additional analysis is required to establish the drivers of these losses.

### Geographic Performance

- West: approximately $108K in profit.
- Central: approximately $40K in profit.
- Texas: approximately $25.7K in losses.
- Ohio: approximately $17K in losses.
- Pennsylvania: approximately $15.6K in losses.

### Customer Segments

Consumer generated approximately $1.161M in sales, followed by Corporate at $706K and Home Office at $430K.

The top 10 customers accounted for approximately 6.7% of total sales.

## Business Recommendations

1. Review high-discount transactions and introduce approval controls for discounts that threaten margins.
2. Reassess pricing, supplier costs, and fulfilment expenses for loss-making product lines.
3. Investigate the drivers of negative profitability in Texas, Ohio, and Pennsylvania.
4. Prioritise profitable product lines and identify opportunities for sustainable growth.
5. Strengthen customer retention and develop Corporate and Home Office sales.

## Skills Demonstrated

- Tableau dashboard development
- Data preparation and validation
- Calculated fields and KPI design
- Sales and profitability analysis
- Time-series analysis
- Product and customer segmentation
- Geographic analysis
- Discount impact analysis
- Business insight generation
- Data-driven recommendations

## Repository Contents

Suggested project structure:

```text
unikstore-sales-profitability-tableau/
├── README.md
├── Sales Dashboard.png
├── Profit Dashboard.png
└── Superstore_Sales_Analysis.twbx
```

Include the Tableau workbook only if it is available. Include the source dataset only if redistribution is permitted.

## Conclusion

This project demonstrates how Tableau can be used to move beyond revenue reporting and investigate the commercial factors affecting profitability.

The analysis identified strong sales growth alongside low-margin product categories, loss-making sub-categories, and substantial losses among highly discounted transactions.

The main takeaway is that **business performance should be evaluated through both revenue growth and profit contribution**.

*Developed as part of my data analytics learning journey.*
