# RFM Segmentation and Customer Insight Analysis

A customer analytics project using **Recency, Frequency, and Monetary (RFM) analysis** to segment customers, understand purchasing behavior, and develop data-driven retention strategies.

## Project Overview

Understanding customer behavior helps businesses identify valuable customers, recognize customers who may need re-engagement, and make better decisions about retention and marketing.

This project applies RFM analysis to transaction data to evaluate:

* How recently customers made a purchase
* How frequently customers purchased
* How much customers spent

The analysis converts transaction-level data into customer-level insights and actionable business recommendations.

## Business Objectives

* Segment customers based on purchasing behavior.
* Identify high-value customers and potential retention opportunities.
* Compare revenue contribution across customer segments.
* Explore customer behavior across locations and weekdays.
* Translate analytical findings into practical business recommendations.

## Tools and Technologies

* **Python**
* **Pandas** — data cleaning and manipulation
* **NumPy** — numerical operations
* **Matplotlib / Seaborn** — data visualization
* **Jupyter Notebook** — exploratory analysis and documentation

*Update this list to match the libraries actually used in the final notebook.*

## Dataset Overview

The dataset contains **1,000 transaction records** and **946 unique customers**.

| Attribute           | Details                        |
| ------------------- | ------------------------------ |
| Observation period  | April 11 – June 10, 2023       |
| Transaction records | 1,000                          |
| Unique customers    | 946                            |
| Products            | 4 product labels               |
| Locations           | London, New York, Paris, Tokyo |
| Revenue analyzed    | 513,677.81                     |
| Currency            | Not specified in the dataset   |

The analysis uses a reference date of **June 11, 2023**, the day after the final transaction date.

## Methodology

### 1. Data Preparation

The transaction data was reviewed for data quality, including missing values and duplicate records.

### 2. RFM Feature Engineering

Customer-level metrics were calculated:

* **Recency:** Number of days since the customer's most recent transaction.
* **Frequency:** Number of transactions associated with the customer.
* **Monetary:** Total recorded spending associated with the customer.

### 3. Customer Segmentation

Customers were grouped into behavioral segments using the RFM metrics and the project’s segmentation rules.

### 4. Exploratory Analysis

The segments were analyzed to understand customer distribution, revenue contribution, repeat purchasing, geography, and weekday patterns.

### 5. Business Recommendations

The findings were translated into potential retention, engagement, and customer-value strategies.

## Customer Segments

The analysis uses the following segments:

| Segment             | Customers |
| ------------------- | --------: |
| Champions           |        62 |
| Loyal Customers     |       167 |
| Potential Loyalists |       158 |
| Recent Customers    |        39 |
| Big Spenders        |       202 |
| At Risk             |       174 |
| Hibernating         |        60 |
| Needs Attention     |        84 |
| **Total**           |   **946** |

These are project-specific segment definitions. They should not be interpreted as universal RFM classifications.

## Key Findings

### Big Spenders contribute a substantial share of revenue

* 202 customers, approximately **21.35%** of the customer base.
* Revenue contribution of **168,616.47**, approximately **32.83%** of total revenue.
* Average spending per customer: **834.74**.

This segment represents an important opportunity for value-based engagement. However, high spending alone does not necessarily indicate repeat-purchase loyalty.

### Champions show stronger repeat purchasing

* 62 customers were classified as Champions.
* 21 customers made repeat purchases during the observed period.
* Repeat-purchase rate: approximately **33.87%**.

The Champions segment had a higher observed repeat-purchase rate than Big Spenders, illustrating why customer value and customer loyalty should be evaluated separately.

### Repeat purchasing varies across segments

| Segment         | Observed Repeat-Purchase Rate |
| --------------- | ----------------------------: |
| Champions       |                        33.87% |
| Loyal Customers |                        11.38% |
| Big Spenders    |                         4.46% |
| At Risk         |                         1.15% |

The remaining segments had no observed repeat purchases during the analysis period. This does not necessarily mean those customers will never return; the dataset covers only a limited period.

### Geographic differences

* Tokyo had the highest customer count and total revenue.
* New York had the highest average revenue per customer.
* Big Spenders represented the highest-revenue segment across all four locations.

These findings can inform further market-level analysis, but they do not establish why geographic differences occurred.

## Business Recommendations

### 1. Retain high-value customers

Develop targeted engagement strategies for Champions and other high-value customers. Monitor whether these customers continue purchasing over time.

### 2. Encourage Big Spenders to return

Consider personalized follow-up campaigns or relevant repeat-purchase incentives. Evaluate campaign performance using repeat-purchase and revenue metrics.

### 3. Re-engage At Risk customers

Test targeted win-back campaigns for customers with declining or less recent activity. Track reactivation rates rather than assuming every customer can be recovered.

### 4. Nurture Potential Loyalists

Use relevant product recommendations and engagement campaigns to encourage a second purchase.

### 5. Validate geographic opportunities

Investigate whether differences across locations are associated with customer mix, product availability, pricing, or other operational factors before making major market decisions.

## Limitations

* The dataset covers approximately two months, limiting long-term behavioral conclusions.
* The currency is not specified; revenue values are reported without a currency symbol.
* The dataset contains one product label per transaction, so it cannot support reliable multi-product basket or co-purchase analysis.
* Returns, refunds, customer satisfaction, reviews, and complaint data are not available.
* RFM segments are based on the rules used in this project and may change with different thresholds or reference dates.
* Weekday patterns are descriptive and should be validated with a longer observation period before being used for campaign scheduling.

## Repository Structure

```text
rfm-customer-segmentation/
│
├── README.md
├── RFM_analysis.ipynb
├── data/
│   └── rfm_data.csv
├── report/
│   └── RFM_Segmentation_Formatted.pdf
├── presentation/
│   └── RFM_Customer_Insights_Storytelling.pdf
└── images/
    ├── rfm_segment_distribution.png
    ├── revenue_by_segment.png
    └── repeat_purchase_analysis.png
```

Adjust the file names and folders to match the final repository contents.

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries.
3. Open the notebook in Jupyter Notebook or JupyterLab.
4. Ensure the dataset path in the notebook matches the repository structure.
5. Run the notebook cells from top to bottom.

Example:

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook
```

## Project Deliverables

* Jupyter Notebook containing the analysis
* Formatted report documenting the findings
* Presentation communicating business insights and recommendations

## Conclusion

This project demonstrates how transaction data can be transformed into customer-level metrics, behavioral segments, and business recommendations.

The analysis highlights the importance of distinguishing **customer spending from repeat-purchase behavior** and using segmentation as a starting point for further customer-retention analysis.
