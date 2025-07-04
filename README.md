# Bank Term Deposit Campaign Performance Dashboard

## Project Overview

This project focuses on analyzing the effectiveness of a direct marketing campaign conducted by a Portuguese bank. The primary goal is to identify key patterns and provide actionable insights to improve subscription rates for term deposit products. The analysis is performed using Microsoft Excel, leveraging its powerful data transformation and visualization capabilities.

## Objectives

* **Analyze Campaign Effectiveness:** Evaluate the success metrics of the direct marketing campaign.

* **Identify Key Patterns:** Discover which customer segments and campaign strategies lead to higher term deposit subscriptions.

* **Provide Actionable Insights:** Generate data-driven recommendations for optimizing future marketing efforts and improving conversion rates.

## Tools and Technologies

* **Microsoft Excel:**

  * **Power Query:** Used for data ingestion, cleaning, transformation, and creating calculated columns (e.g., `AgeGroup`, `WasPreviouslyContacted`, `CallDuration (Minutes)`, `Combined Loan Status`).

  * **Power Pivot (Data Model):** Utilized for creating advanced DAX (Data Analysis Expressions) measures to calculate key performance indicators (KPIs) like conversion rates and average metrics.

  * **Pivot Tables:** Employed for multi-dimensional analysis and segmentation of customer data.

  * **Charts:** Used to visualize insights, making complex data easily understandable.

  * **Slicers:** Implemented for interactive filtering, allowing stakeholders to dynamically explore data segments.

* **Gemini API (LLM Integration - *Future Enhancement/Conceptual*):**

  * *While the core dashboard is Excel-based, this project can be extended with LLM capabilities (e.g., via a web interface) to:*

    * Generate natural language summaries of dashboard insights.

    * Provide predictive analysis on customer segments.

    * Suggest personalized campaign messages based on customer profiles.

## Key Features & Insights

The dashboard provides a comprehensive view of the campaign's performance, answering critical stakeholder questions:

* **Overall Campaign Performance:** Clear KPIs for total contacts, total subscriptions, and the overall conversion rate.

* **Customer Segmentation:** Analysis of subscription rates across various demographic segments, including:

  * **Age Groups:** Identifying which age demographics are most receptive.

  * **Job Titles & Education Levels:** Understanding the impact of professional and educational backgrounds.

  * **Marital Status & Loan Status:** Assessing the influence of personal circumstances.

* **Contact Strategy Effectiveness:** Insights into the best contact methods and months for outreach.

* **Previous Campaign Impact:** Analysis of how prior interactions (success, failure, unknown) affect current subscription likelihood.

* **Call Duration Optimization:** Examination of the relationship between call length and conversion success.

* **Financial Profile Analysis:** Understanding the average account balance of subscribers versus non-subscribers.

* **Interactive Dashboard:** Slicers enable dynamic filtering and exploration of data, allowing stakeholders to drill down into specific segments.

## How to Use / View the Project

1. **Download the Dataset:** Obtain the `Bank Marketing Campaign.csv` dataset.

2. **Open in Excel:** Load the `Bank Marketing Campaign.csv` file into Microsoft Excel.

3. **Utilize Power Query:** Ensure the data is loaded via Power Query, with all the specified transformations and conditional columns applied.

4. **Build Data Model & DAX Measures:** Confirm the data is added to the Data Model and the DAX measures (`Subscribed_Yes_Count`, `Total_Customers`, `Conversion_Rate_Percentage`, `Avg_Call_Duration_Subscribers_Mins`) are created as described in the project guide.

5. **Construct the Dashboard:** Follow the dashboard layout blueprint to create Pivot Tables, Charts, and Slicers, linking them to your Data Model and DAX measures.

## Insights and Recommendations

Based on the analysis, here are some key insights and actionable recommendations:

* **Target High-Potential Segments:**

  * Identify specific `AgeGroup`, `Job Title`, and `EducationLevel` combinations that consistently show higher subscription rates. Tailor future campaigns to prioritize these segments.

  * For instance, if "Middle-Aged Adults" in "Management" with "Tertiary" education have a significantly higher conversion, allocate more resources to reaching similar profiles.

* **Optimize Call Strategy:**

  * Analyze the `CallDuration (Minutes)` to identify an optimal range that correlates with higher subscription rates. Train sales representatives to aim for this duration, avoiding overly short or excessively long calls that might lead to disengagement.

  * For example, if calls between 3-5 minutes yield the best results, focus on concise and impactful pitches within that timeframe.

* **Leverage Previous Interactions:**

  * Customers with a `PreviousCampaignOutcome` of 'Success' are highly valuable; prioritize re-engagement with these individuals.

  * For those with 'Failure' or 'Other' outcomes, tailor the messaging to address past concerns or offer different product variations. Avoid treating them as completely new leads.

* **Seasonal Campaign Adjustments:**

  * Examine `ContactMonth` trends to identify peak performance months. Adjust campaign scheduling to maximize reach and conversion during these periods. Conversely, reduce efforts in low-performing months unless specific strategies can overcome seasonal challenges.

* **Loan Status Impact:**

  * Understand how `Combined Loan Status` (e.g., "Only Housing Loan" vs. "No Loan") influences subscription. This can help in segmenting customers for specific product offerings or financial advice, as their existing loan commitments might affect their willingness to invest in a term deposit.

* **Refine Messaging based on Financial Profile:**

  * If `AccountBalance` shows a significant difference between subscribers and non-subscribers, adapt marketing messages. For those with lower balances, emphasize the benefits of starting small or the security of term deposits. For higher balances, focus on growth and wealth management.

## Future Enhancements

* **Predictive Modeling:** Implement machine learning models (e.g., Logistic Regression) to predict subscription likelihood for new customers.

* **Advanced Segmentation:** Utilize clustering algorithms to identify new, high-value customer segments.

* **Automated Reporting:** Integrate with VBA or Python to automate report generation and distribution.



## Author

Nelson M.