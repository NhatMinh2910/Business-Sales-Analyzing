# Business Sales Analyzing Project 🌐
## Executive Summary 🌟

This project analyses product-level sales data from a global fashion brand (Zara), sourced from Kaggle, to identify the key factors that influence **sales volume**. Each record in the dataset represents a single product’s sales volume and includes attributes related to product positioning, pricing, promotions, seasonality, and product characteristics. Understanding how these variables affect sales volume enables more effective decisions in merchandising, pricing strategy, and marketing execution.

The analysis focuses on evaluating the impact of three primary dimensions:

1. **Commercial and marketing factors** (price, promotion status, seasonal labeling, product position),
1. **Product attributes** (category, material, origin, brand-related features), and
1. **Merchandising context** (section placement and season alignment).

Through systematic exploratory data analysis and comparative evaluation, the project identifies patterns and relationships between these attributes and observed sales volume. 

Key findings include:

- Female customers drive nearly 70% of total sales volume, making them the core revenue segment and the primary focus for merchandising and marketing strategies.
- Male sales volume is lower but shows growth potential, particularly through targeted promotion and cross-merchandising rather than essential, need-based products.
- Female sales performance is more consistent across products, indicating broader demand rather than reliance on a small number of top-selling items.
- Price and promotion sensitivity differ by gender, suggesting that differentiated pricing and promotional strategies could improve overall sales efficiency.
- Autumn and Winter account for the majority of sales volume, with Autumn slightly outperforming Winter due to early purchasing behavior as customers prepare for colder seasons.
- Gender has minimal impact on seasonal purchasing behavior, indicating that seasonal demand is driven primarily by product relevance rather than customer demographics.
- Promotions are significantly more effective for seasonal products, suggesting they should be strategically timed around peak seasons to maximize sales impact.

The outcome of this project is a set of **actionable, data-driven insights** that explain what drives sales volume at the product level. These insights can be directly applied to improve sales effectiveness by optimizing pricing strategies, prioritizing promotional efforts, refining product assortment, and enhancing product placement decisions. Overall, the project demonstrates how analytical reasoning and structured data analysis can support commercial decision-making in a real-world retail context.

## Project Objectives 🌟

- Analyze historical sales data to understand overall performance and key drivers.
- Segment customers and products to uncover purchasing behaviour patterns.
- Identify trends, seasonality, and anomalies in sales.
- Build a demand forecasting model to estimate future sales.
- Present insights through a clear and automated dashboard.

## Dataset Description 🌟

The dataset consists of the following attributes:

- **Product identifiers and positioning**: Product ID, Product Position
- **Marketing attributes**: Promotion, Seasonal
- **Product characteristics**: Product Category, Brand, Name, Description, Material, Origin
- **Sales-related variables**: Sales Volume, Price, Currency
- **Additional metadata**: URL, Terms, Section, Season

Each record represents a **single product**, along with its associated sales volume and contextual information.

## Methodology 🌟

### 1. Data Pre-Processing

All of the data handling process mentioned below are handled using Python Pandas, the Python notebook is included in the repository.

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

## Visualization and Dashboard 🌟
### Page 1: Executive Overview

<img width="975" height="547" alt="image" src="https://github.com/user-attachments/assets/7e3dd2ea-c6e2-4e19-ad26-264c6abb8d89" />

### Page 2: Gender Sales Analysis

<img width="975" height="546" alt="image" src="https://github.com/user-attachments/assets/7afc0ad6-c715-44a1-9a56-e51d651fa286" />

### Page 3: Season Factors Analysis

<img width="1143" height="640" alt="image" src="https://github.com/user-attachments/assets/497405d3-566a-4ec3-9f7f-b6f16a1c7d46" />

## Key Insights and Findings 🌟

### *Page 1: Executive Overview*
**Gender Contribution to Total Sales Volume**

The Executive Overview reveals a clear dominance of female customers in overall sales performance. Female customers contribute approximately 67.8% of total sales volume, which is nearly double the contribution from male customers (32.2%). This indicates that sales volume is primarily driven by female demand within the dataset.
To interpret this result meaningfully, it is important to consider the underlying business context of the data source. Two plausible scenarios can be examined:

•	**Scenario 1**: Female-oriented product assortment
The product portfolio may contain a higher number of female-focused items, both in terms of variety and quantity. In this case, the observed sales imbalance is structurally driven by supply-side decisions, where the brand or retailer prioritizes female fashion categories.

•	**Scenario 2**: Balanced assortment, demand-driven difference
Alternatively, if male and female product assortments are relatively balanced, the difference in sales volume would indicate stronger demand from female customers. This would suggest that female shoppers are either purchasing more frequently, buying higher volumes per transaction, or being more responsive to fashion-related stimuli.
Since this is a hypothetical dataset rather than a real operational project, both scenarios are considered valid analytical paths. In practice, further investigation into product mix, inventory allocation, and merchandising strategy would be required to validate the correct interpretation.

**Behavioral and Contextual Interpretation**

From a consumer behavior perspective, higher fashion-related purchase activity among female customers is consistent with well-established market patterns. Female consumers typically exhibit higher engagement with apparel shopping, driven by greater variety in fashion cycles, trends, and usage occasions.\
If the data originates from online shopping, external benchmarks on gender-based e-commerce participation could be used to assess whether a 67% female contribution is within a reasonable range. If the figure aligns with industry norms, it would further validate the dataset’s representativeness.\
If the data originates from in-store purchases, additional behavioral factors may apply. For example, studies often show that female customers shop alone or with other female companions more frequently, while shopping trips involving male companions may present opportunities for cross-selling. In such a context, merchandising strategies such as:
- Placing selected men’s fashion items near women’s sections,
-	Promoting couple or matching outfits,
-	Highlighting visually appealing male items (e.g., jackets, shoes)

could help increase male product exposure and impulse-driven purchases. Essential male items, which are typically need-based rather than emotion-driven, are less dependent on such strategies.

**Strategic Implications**

Overall, the significantly higher sales volume contribution from female customers appears reasonable and expected within a fashion retail context. The strategic priority should therefore be twofold:

- Maintain and strengthen the female segment, which represents the core revenue driver.
-	Gradually develop male-focused strategies, particularly through cross-merchandising and targeted product placement, to improve male sales without disrupting the dominant female segment.

**Seasonal vs Non-Seasonal Sales**

The comparison between seasonal and non-seasonal sales volume shows a relatively balanced distribution, with no substantial dominance from either group. The difference is not large enough at this stage to suggest a strong seasonal dependency or a compelling standalone narrative.
### *Page 2: Gender Sales Analysis*
**Product Category Performance**

Across both genders, the ranking of best-selling product categories is highly consistent, indicating similar consumption preferences between male and female customers. The sales volume ranking from highest to lowest is:

***Jackets → Sweaters → T-shirts → Shoes → Jeans***

This consistency suggests that core product categories drive demand for both genders. From a business perspective, the brand should continue to prioritize investment and innovation in these key categories, while also identifying underperforming categories (e.g. jeans) for potential improvement or repositioning.

Despite similar category preferences, female sales volume remains approximately twice that of male sales across all categories, mirroring the overall gender sales split. This indicates that the difference lies in purchase intensity, not in fundamentally different product choices.

**Product Position Impact**

Products placed in aisle positions generate the highest sales volume, while items located at the front of the store perform the weakest for both genders. This highlights the importance of in-store placement strategy. High-demand or strategic products should be prioritized for aisle placement to maximize visibility and conversion, while front-of-store areas may require stronger visual merchandising or promotional support.

**Promotion Sensitivity**

Promotions have a stronger impact on female customers than on male customers. Female purchase activity under promotion is notably higher, suggesting greater sensitivity to promotional cues and emotionally driven buying behavior.

This observation aligns with existing consumer behavior research, which frequently finds that female shoppers respond more strongly to discounts, limited-time offers, and promotional framing. From a strategic standpoint, promotion-led campaigns are likely to yield higher returns when targeted toward female customers, while male-focused strategies may benefit more from value-driven or functional messaging.

**Price vs Sales Volume (Scatter Plot Insight)**

The scatter plot reveals that the highest sales volumes for both genders are concentrated around the $20 price point, identifying this range as a clear mass-market sweet spot. Within this price range, female sales volume is approximately twice that of male sales, reinforcing the earlier insight that female demand is stronger at accessible price levels.

However, at higher price points (above $90), the sales volume gap between genders narrows significantly, with male and female purchases becoming nearly equivalent. This suggests that:

At lower prices, purchases are more frequent and emotion-driven, favoring female customers.

At higher prices, purchases are more deliberate and need-based, reducing gender differences in buying behavior.

This insight implies that premium-priced products can be positioned as gender-neutral offerings, while mid- to low-priced products should primarily be optimized for the female segment.
### *Page 3: Seasonal Factors Analysis*

Based on the seasonal sales distribution, **Autumn** and **Winter** are the two strongest seasons, contributing approximately 36% and 27% of total sales volume, respectively, while Summer records the lowest sales. This pattern aligns well with findings from Page 2, where jackets and sweaters are the top-selling categories, both of which are primarily autumn–winter products.

Interestingly, Autumn slightly outperforms Winter in total sales volume. A plausible explanation is that customers tend to purchase early in late Autumn to prepare for Winter, leading to higher accumulated sales during the Autumn period despite jackets being worn more frequently in Winter.

From a strategic perspective, this seasonality pattern provides clear guidance for **product planning** and **inventory management**. The business should prioritize launching new outerwear collections in Autumn, limit production volumes during Summer to reduce inventory risk, and use Spring and Summer promotions to stimulate demand during lower sales periods.

The seasonal purchase ratio between **male and female customers is nearly identical**, suggesting that **gender does not significantly influence whether customers buy seasonal products**. This indicates that seasonal demand is driven more by product utility and climate factors than by customer demographics.

Promotion effectiveness shows a clear interaction with seasonality. **Seasonal products are significantly more likely to be purchased when promotions are active**, whereas non-seasonal products rely less on promotional incentives. This suggests that **promotions should be strategically timed and concentrated on seasonal items to maximize sales impact.**

Finally, category-level analysis confirms that **most products perform best in their intended seasons**, with **jackets and sweaters exhibiting the strongest seasonal dependency**. The large sales gap between seasonal and non-seasonal periods for these categories highlights their high sensitivity to seasonal timing, reinforcing the importance of accurate season-based assortment planning.

## Tools and Techniques 🌟

- Programming Language: Python
- Libraries: NumPy, Pandas, Matplotlib
- Visualization: Power BI
- Techniques: Exploratory Data Analysis, Feature Engineering, Machine Learning Forecasting

## Business Impact 🌟

The insights from this analysis can help the business:

- Optimize inventory levels and reduce stockouts or overstocking.
- Improve sales planning through data-driven demand forecasts.
- Focus marketing and sales efforts on high-performing products and regions.
- Establish a repeatable analytics workflow for future sales analysis.

## Conclusion 🌟
