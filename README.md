# Quantium Virtual Internship – Retail Strategy and Analytics  
This project showcases my completion of the Quantium Virtual Internship on the Forage website, focused on real-world data analysis in the retail sector. The project is split into three key tasks involving exploratory data analysis, customer segmentation, and campaign experimentation through uplift modeling:

## Task 1: Data Cleaning and Exploratory Data Analysis (EDA)  
In this phase of the project, the focus was on preparing the transactional and customer datasets for analysis and gaining initial insights into the data.
**Key Steps:**  
- Data Loading and Inspection  
- Date Formatting and Validation  
- Product Name Cleaning  
- Outlier Detection and Handling  
- Feature Engineering  
- Brand Distribution Analysis  
- Customer Data Exploration  
- Data Merging  

## Task 2: Customer Segment Analysis  
This task focuses on analyzing customer purchasing behavior by segmenting shoppers based on their Lifestage and Premium Status. The goal is to derive actionable marketing insights and identify key customer segments that contribute most to sales, volume, and pricing.
This analysis provides a solid foundation for segment marketing strategies, optimizing product placement, and guiding future promotional campaigns.
**Key Analyses Performed:**  
- Sales Distribution by Segment  
- Customer Count per Segment  
- Average Units per Customer  
- Average Price per Unit (*A t-test was applied to assess the statistical significance of price differences between Mainstream and Budget/Premium shoppers among young and mid-age singles/couples. Results showed significantly higher prices paid by Mainstream shoppers (*p* < 0.001))*  

**Affinity Analysis:**  
Compared brand and pack size preferences for the key segment: MAINSTREAM – YOUNG SINGLES/COUPLES. Findings include:
- 23% more likely to purchase Tyrrells  
- 27% more likely to purchase 270g packs  
- 56% less likely to buy Burger Rings  

**Results & Recommendations:**  
- High-Value Segments: Mainstream Young Singles/Couples & Budget Older Families  
- Targeted Strategies: Promotions, loyalty programs, off-location placements  
- Impulse Behavior opportunities through visibility-based promotions  

## Task 3: Experimentation & Uplift Analysis  
To assess the efficiency of a product replacement campaign, we conducted an analysis through two steps:

**Approach:**  
1. Matching trial stores with control stores based on pre-trial similarity (sales and customer count trend behaviors).
The key challenge was in this step. Initially, I combined sales and customer counts in a similarity function but later separated them, focusing first on sales. In the function itself, I tested a hybrid metric (Pearson correlation + magnitude distance) but realized magnitude could not explain post-trial trends (e.g., a control store with similar sales volume but opposite trends would skew results).
Final Approach: 
   - Sales-Based Matching (`best_match1`):
Identified stores with the strongest sales trend similarity (Pearson correlation) and selected the top 10 correlated stores. Narrowed to stores with sales within ±20% of the trial store’s mean, resulting in best_match1.
   - Customer-Based Matching (`best_match2`):
Repeated the process for customer count trends, creating best_match2.
   - Combined Metrics Matching (`best_match3`):
  Averaged scores from best_match1 and best_match2, then sorted the list based on combined scores to create best_match3.

2. Measured post-trial differences in sales (best_match1), customer count (best_match2), and combined metrics (best_match3) by validating significance using t-tests and confidence intervals.

**Results for Store 77:**  
- In the original project, three trial stores (77, 86, 88) were analyzed using a mixed function considering both total sales and customer counts. However, my deeper analysis focused on Store 77 using three distinct matching functions (sales-based, customer-based, and combined). This methodology is more precise and informative. The final solution requires applying these three functions to the other two trial stores to conclusively determine campaign effectiveness. For Store 77:

**Final Verdict (Campaign Effectiveness Conclusion):**  
Our comprehensive analysis using multiple control stores and metrics reveals mixed evidence for the product replacement campaign’s effectiveness. While comparisons with Store 233 consistently indicate success across both sales and customer metrics, alternative control stores (50, 35, and 162) suggest the observed improvements may be attributable to broader market trends. This inconsistency across benchmarks indicates the campaign likely had a positive but modest effect that is sensitive to control store selection. The campaign shows promise but requires further testing with refined methodology before full-scale implementation can be confidently recommended.


### Little notice: for running the whole project, you first have to run orderly, because the **mdata** file will be created at the end of task1, and will be used in the other tasks.

---
