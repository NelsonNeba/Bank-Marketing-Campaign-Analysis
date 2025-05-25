# Bank Marketing Campaign Analysis for Term Deposit Subscription

## Project Overview

This project analyzes a dataset from a direct marketing campaign conducted by a Portuguese banking institution. The campaign involved outreach via phone calls, aiming to encourage customers to subscribe to a term deposit. The primary goal of this analysis is to identify key factors influencing subscription success and provide actionable insights to optimize future marketing strategies.

The analysis was performed using [Mention your primary tool, e.g., Microsoft Excel, 

**Live Dashboard/Report (if applicable):** [Link to your deployed Power BI report, Tableau Public dashboard, Google Data Studio report, or a static image/PDF of your Excel dashboard]

## Table of Contents

*   [Business Problem](#business-problem)
*   [Data Source](#data-source)
*   [Methodology](#methodology)
    *   [Data Import & Cleaning](#data-import--cleaning)
    *   [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
    *   [Feature Engineering](#feature-engineering)
    *   [Visualization](#visualization)
*   [Key Questions Addressed](#key-questions-addressed)
*   [Key Findings & Insights](#key-findings--insights)
*   [Visualizations Showcase](#visualizations-showcase)
*   [Actionable Recommendations](#actionable-recommendations)
*   [Tools & Technologies](#tools--technologies)
*   [Project Structure](#project-structure)
*   [How to Use/Reproduce](#how-to-usereproduce)
*   [Future Work](#future-work)
*   [Author](#author)
*   [Acknowledgments](#acknowledgments)

## Business Problem

The banking institution aims to improve the efficiency and effectiveness of its direct marketing campaigns for term deposits. Key business objectives include:
*   Increasing the overall subscription rate for term deposits.
*   Identifying customer segments with a higher propensity to subscribe.
*   Optimizing campaign outreach strategies (e.g., contact timing, channels).
*   Understanding the impact of customer demographics and financial profiles on subscription decisions.

This analysis seeks to provide data-driven answers to inform these objectives.

## Data Source

The dataset used for this analysis is the "Bank Marketing Data Set" from the UCI Machine Learning Repository. It contains information on [Number] instances (customer contacts) with [Number] attributes, including customer demographics, last contact information, and previous campaign outcomes.

*   **Target Variable:** `y` - Has the client subscribed a term deposit? (yes/no)

## Methodology

### Data Import & Cleaning

*   The raw data (JSON/CSV format) was imported into [Your Tool, e.g., Excel using Power Query, Python using Pandas].
*   Initial data inspection was performed to understand data types, structure, and potential issues.
*   **Cleaning steps included:**
    *   Handling missing values (e.g., for `job`, `education` - specify your strategy).
    *   Standardizing categorical data (e.g., converting text to consistent case).
    *   Correcting data types (e.g., ensuring numerical fields were numeric, date fields were dates).
    *   Renaming columns for clarity (e.g., `y` to `SubscribedTermDeposit`).

### Exploratory Data Analysis (EDA)

Descriptive statistics and visualizations were used to understand the distribution of individual variables and their relationships with the target variable (`SubscribedTermDeposit`).
*   Analyzed the overall subscription rate (12.0%).
*   Examined distributions of numeric features (e.g., `Age`, `AccountBalance`, `CallDurationSeconds`) using histograms and summary statistics.
*   Investigated frequency distributions of categorical features (e.g., `Job`, `MaritalStatus`, `EducationLevel`).
*   Bivariate analysis was conducted to assess the impact of each feature on subscription rates using PivotTables/group-by operations and appropriate charts.

### Feature Engineering

New features were created to enhance the analysis and derive deeper insights:
*   `AgeGroup`: Categorizing customers into age brackets.
*   `WasPreviouslyContacted`: Binary flag based on `pdays`.
*   `CampaignDate`: Combining `day` and `month` into a proper date format.
*   `CallDurationMinutes`: Converting call duration from seconds to minutes.
*   `CombinedLoanStatus`: Categorizing customers based on housing and personal loan status ('No Loan', 'Only Housing Loan', etc.).

### Visualization

[Your Tool, e.g., Excel charts, Matplotlib/Seaborn, Tableau] was used to create a dashboard/set of visualizations to communicate findings effectively. Key charts include:
*   Bar charts for comparing subscription rates across categorical segments.
*   Line charts for trends (e.g., monthly rates, rates by days since last contact).
*   Pie chart for overall subscription breakdown.
*   [Mention other chart types you used]

## Key Questions Addressed

This analysis aimed to answer the following stakeholder-relevant questions:
1.  Which customer segments are most receptive to our term deposit offers, and how can we better target them?
2.  How effective was our previous campaign engagement in driving current subscriptions, and what's the optimal timing to re-engage past customers?
3.  Are our current campaign outreach strategies efficient? Which channels and contact frequencies yield the best results?
4.  Does a customer's existing financial relationship with us significantly impact their likelihood to subscribe?
5.  What is the overall success of this marketing campaign, and what are key indicators of engaged customers?

## Key Findings & Insights

*   **Overall subscription rate:** 12.0%.
*   **Previous Success is Key:** Customers with a previous successful campaign outcome have a **64.34%** subscription rate, significantly higher than any other group.
*   **Re-engagement Pays Off:** Previously contacted customers subscribe at 22.55%, compared to 9.10% for those not previously contacted. The optimal re-contact window appears to be 91-180 days post-last contact.
*   **Target Demographics:**
    *   `Retired` individuals show the highest subscription rates by job.
    *   Customers with `Tertiary` education are more likely to subscribe.
    *   `Single` and `Divorced` individuals have higher rates than `Married`.
*   **Financial Profile:**
    *   Customers with `No Loan` obligations subscribe at a higher rate (16.8%).
    *   Customers with lower `AccountBalance` (e.g., < €10,000) show higher propensity.
*   **Campaign Mechanics:**
    *   `Cellular` contact is the most effective channel.
    *   Longer `CallDurations` are strongly correlated with subscription success (avg. 9.21 mins for subscribers vs. 3.77 mins for non-subscribers).
    *   Subscription rates peak in `Oct` and are lowest in `December`.
*   **Low Impact Factor:** `Credit Default` status showed minimal difference in subscription rates.

## Visualizations Showcase

*(Embed 2-3 key static images of your best charts/dashboard here if your platform allows. Otherwise, describe them or link to a separate visual report.)*

**Example:**
*   A bar chart showing the dramatic difference in subscription rates by `PreviousOutcome`.
    ```
    [Image of your PreviousOutcome chart]
    ```
*   A bar chart highlighting subscription rates by `Job` or `LoanStatus`.
    ```
    [Image of your Job/LoanStatus chart]
    ```
*   [Link to full dashboard/report if hosted online]

## Actionable Recommendations

Based on the analysis, the following recommendations are proposed to the banking institution:
1.  **Prioritize Previously Successful Customers:** Dedicate resources to re-engage customers with a previous 'success' outcome, as they represent the highest conversion potential.
2.  **Optimize Re-contact Strategy:** Implement a re-contact schedule targeting previously contacted customers (especially non-successful ones) within the 91-180 day window.
3.  **Refine Target Segmentation:** Focus marketing efforts on:
    *   Demographic segments: Retired, Tertiary education, Single/Divorced.
    *   Financial segments: Customers with No Loans, lower account balances.
4.  **Enhance Channel & Call Strategy:**
    *   Maximize use of `Cellular` for outreach.
    *   Train agents on effective engagement techniques to foster longer, quality conversations, while being mindful that duration is an outcome of interest, not just a target.
5.  **Strategic Campaign Timing:** Plan campaigns to capitalize on higher response months (like May) and consider alternative strategies or offers for lower response months (like December).
6.  **De-prioritize Non-Differentiating Factors:** Credit default status may not require specific segmentation for this product.

## Tools & Technologies

*   **Data Cleaning & Transformation:** [e.g., Microsoft Excel (Power Query), 
*   **Data Analysis:** [e.g., Microsoft Excel (PivotTables, Formulas), 
*   **Data Visualization:** [e.g., Microsoft Excel (Charts), 
*   **Version Control (Optional):** [Git, GitHub]
*   **Project Management (Optional):** [Slake]

