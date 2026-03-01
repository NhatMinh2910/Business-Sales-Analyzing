# Business Sales Analyzing Project
## Executive Summary

This project analyses product-level sales data from a global fashion brand (Zara), sourced from Kaggle, with the objective of identifying the key factors that influence **sales volume**. Each record in the dataset represents a single product’s sales volume and includes attributes related to product positioning, pricing, promotions, seasonality, and product characteristics. Understanding how these variables affect sales volume enables more effective decisions in merchandising, pricing strategy, and marketing execution.

The analysis focuses on evaluating the impact of three primary dimensions:

1. **Commercial and marketing factors** (price, promotion status, seasonal labeling, product position),
1. **Product attributes** (category, material, origin, brand-related features), and
1. **Merchandising context** (section placement and season alignment).

Through systematic exploratory data analysis and comparative evaluation, the project identifies patterns and relationships between these attributes and observed sales volume. 

Key findings include:

- Tóm tắt insights tìm dc

The outcome of this project is a set of **actionable, data-driven insights** that explain what drives sales volume at the product level. These insights can be directly applied to improve sales effectiveness by optimizing pricing strategies, prioritizing promotional efforts, refining product assortment, and enhancing product placement decisions. Overall, the project demonstrates how analytical reasoning and structured data analysis can support commercial decision-making in a real-world retail context.

## Project Objectives

- Analyze historical sales data to understand overall performance and key drivers.
- Segment customers and products to uncover purchasing behaviour patterns.
- Identify trends, seasonality, and anomalies in sales.
- Build a demand forecasting model to estimate future sales.
- Present insights through a clear and automated dashboard.

## Dataset Description

The dataset consists of the following attributes:

- **Product identifiers and positioning**: Product ID, Product Position
- **Marketing attributes**: Promotion, Seasonal
- **Product characteristics**: Product Category, Brand, Name, Description, Material, Origin
- **Sales-related variables**: Sales Volume, Price, Currency
- **Additional metadata**: URL, Terms, Section, Season

Each record represents a **single product**, along with its associated sales volume and contextual information.

## Methodology

### 1. Data Pre-Processing

### *Columns name standardization*

All column names were standardized to:

- Ensures consistency across the dataset
- Prevents errors during coding and analysis
- Improves readability and maintainability of scripts

### *Data type validation and conversion*

Each column was reviewed to ensure its data type matched its intended business meaning:

- Numeric fields (e.g., sales volume, price, product position) were converted to numeric types
- Non-convertible values were coerced into missing values

Accurate data types ensure that sales metrics, rankings, and summaries reflect true business performance.

### *Handling missing values*

The proportion of missing values was calculated for each column.\
Missing values were handled based on business logic rather than arbitrary imputation.

**Handling Strategy**

- **Critical identifiers (Product ID)**: Rows with missing values were removed
- **Categorical attributes (Brand, Material, Origin)**: Filled with placeholders such as *“Unknown”* or *“Not specified”*
- **Numeric sales-related fields**: Handled conservatively to avoid bias

### *Detect duplicates*

Duplicate entries were identified using the Product ID as the primary key.

Removing duplicates prevents double-counting products and ensures accurate product-level analysis.

### *Numeric value validation*

Numeric fields such as price and sales volume were validated against basic business rules:

- Prices must be greater than zero
- Sales volume must be non-negative

Outliers were examined using descriptive statistics.

### *Promotion and seasonal field normalization*

Promotion and seasonal indicators were standardized into boolean values.

Accurate promotion indicators are essential for evaluating marketing effectiveness.

### *Categorical cleaning*

Categorical fields (Product Category, Brand, Section, Season) were normalized by:

- Converting text to lowercase
- Removing unnecessary whitespace

Improves the reliability of category-based sales and product mix analysis.

### *Result*

Through a structured preprocessing pipeline, the dataset was transformed from raw input into a high-quality, reliable data source.\
The preprocessing steps ensured:

- Logical consistency with business rules
- Improved data quality and interpretability
- Readiness for exploratory analysis, visualization, and reporting

This systematic approach reflects best practices in data analysis and provides a strong foundation for subsequent business insights.

### 2. Data Analysis

After completing data cleaning, validation, and feature engineering, the dataset was analyzed using a structured, business-oriented analytical framework implemented in a multi-page Power BI report. The objective of the analysis was to understand sales volume patterns in the fashion retail context, with a specific focus on gender differences and the influence of seasonal and commercial factors. The analytical process was intentionally divided into four pages, each answering a distinct business question and progressively deepening insight.

### *Page 1 – Executive Overview*

The first page provides a high-level snapshot of overall sales performance. Key performance indicators (KPIs), including total sales volume, sales contribution by gender, and the proportion of seasonal products, were used to establish context and scale. This overview enables stakeholders to quickly understand the size of the business and identify which customer segment contributes most to overall sales. Importantly, total sales metrics were designed to remain independent of gender filters, ensuring consistent executive-level reporting while allowing deeper segmentation in subsequent analyses.

### *Page 2 – Gender-Based Sales Analysis*

The second page focuses on understanding how sales volume differs between male and female segments. Beyond comparing total sales, distributional analysis was applied to assess whether sales are driven by a small number of high-performing products or by consistent performance across product assortments. Additional visuals examine the relationship between sales volume, pricing, promotions, and product positioning across genders. This page highlights structural differences in purchasing behaviour and sensitivity to commercial levers, providing actionable insights for marketing and product strategy.

### *Page 3 – Seasonal and Contextual Analysis*

The third page explores the role of contextual factors, particularly seasonality. Sales volume is analyzed across seasonal versus non-seasonal products, individual seasons, and grouped terms or conditions associated with sales. This analysis clarifies how demand fluctuates throughout the year and whether seasonal strategies affect male and female customers differently. By separating contextual observation from causality, this page establishes the environmental conditions under which sales performance tends to improve or decline.

### *Summary*

Overall, the three-page Power BI report follows a clear analytical storyline: starting from a general overview, moving through segmentation and contextual understanding. This structure ensures that insights are both intuitive for stakeholders and analytically rigorous, transforming cleaned data into meaningful business intelligence and actionable recommendations.

### 3. Modeling and Forecasting (Optional)

## Key Insights and Findings

## Visualization and Dashboard

## Tools and Techniques

- Programming Language: Python
- Libraries: NumPy, Pandas, Matplotlib
- Visualization: Power BI
- Techniques: Exploratory Data Analysis, Feature Engineering, Machine Learning Forecasting

## Business Impact

The insights from this analysis can help the business:

- Optimize inventory levels and reduce stockouts or overstocking.
- Improve sales planning through data-driven demand forecasts.
- Focus marketing and sales efforts on high-performing products and regions.
- Establish a repeatable analytics workflow for future sales analysis.

## Conclusion
