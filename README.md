# SwiftConnect Telecom: Customer Support Operations Optimization

## Table of Contents
1.  [Introduction & Business Problem](#1-introduction--business-problem)
2.  [Methodology](#2-methodology)
3.  [Executive Summary](#3-executive-summary)
4.  [Key Findings & Insights](#4-key-findings--insights)
5.  [Actionable Recommendations](#5-actionable-recommendations)
6.  [Thought Process, Challenges & Solutions](#6-thought-process-challenges--solutions)
7.  [Project Deliverables](#7-project-deliverables)
8.  [Contact Information](#8-contact-information)

---

## 1. Introduction & Business Problem

**SwiftConnect Telecom** is a major telecommunications provider facing challenges in its customer support operations. Despite heavy investment, there are fluctuations in customer satisfaction (CSAT) and perceived inefficiencies.

**The Business Problem:**
The core problem is to understand and address the bottlenecks and inefficiencies in the customer support process. This project aims to identify common customer issues, analyze ticket resolution times, assess agent performance, and understand the drivers of customer satisfaction to ultimately reduce resolution times, improve CSAT, and optimize staffing/training.

**Objectives:**
* To analyze historical customer support ticket data.
* To uncover insights into operational performance.
* To identify specific areas for improvement.
* To provide actionable recommendations to the Customer Service leadership team.

---

## 2. Methodology

This project followed a structured data analysis pipeline, leveraging Python for data manipulation and exploratory analysis, and Power BI for interactive visualization and reporting.

**Data Source:**
The analysis utilized the **"Technical Support Dataset"** from Kaggle, providing detailed records of customer support tickets, including status, priority, source, timestamps, agent details, and survey results.

**Tools Used:**
* **Python:** Pandas for data manipulation, Matplotlib and Seaborn for initial exploratory data visualization.
* **Power BI Desktop:** For advanced interactive dashboard creation and final reporting.

**Project Phases:**

1.  **Data Acquisition & Initial Exploration:** Loaded the raw dataset, inspected its structure, data types, and identified initial data quality issues.
2.  **Data Cleaning & Preprocessing:** Addressed missing values (imputing where appropriate or confirming meaningful NaNs), and standardized categorical variables.
3.  **Feature Engineering:** Derived new, analytically rich features from existing data, such as actual response and resolution durations (in minutes/hours), time-based attributes (day of week, hour of day, month, year), and numerical SLA compliance flags.
4.  **Exploratory Data Analysis (EDA) & Insights Generation:** Performed in-depth analysis by segmenting data across various dimensions (channel, priority, topic, time) and examining relationships between key metrics. This phase involved extensive use of descriptive statistics and data visualization.
5.  **Findings, Recommendations & Presentation:** Synthesized all insights into actionable recommendations and structured them into a professional, interactive Power BI report.

---

## 3. Executive Summary

The analysis of SwiftConnect Telecom's customer support operations reveals a mixed performance. While the front line demonstrates strong initial responsiveness, significant challenges exist in overall resolution efficiency and customer satisfaction.

**Overall Performance Snapshot:**

* **Overall Average First Response Time:** 26.07 minutes (Good)
* **Overall Average Resolution Time:** 33.24 hours (Long, area of concern)
* **Overall First Response SLA Compliance:** 86.65% (Decent)
* **Overall Resolution SLA Compliance:** 66.39% (Low, major red flag)
* **Overall Average CSAT Score:** 3.51/5 (Mediocre)

**Key Takeaway:** Systemic issues in resolving problems, rather than initial contact, are the primary drivers of customer dissatisfaction. The overall Resolution SLA compliance is concerningly low, directly impacting the average CSAT score.

**Power BI Report: Executive Summary Page**
*A high-level view of the report's purpose and overall key performance indicators.*

![Executive Summary & Overall Performance](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/visualizations/Executive_Summary_&_Overall_Performance.png?raw=true)

---

## 4. Key Findings & Insights

Detailed analysis across various dimensions revealed several critical insights into SwiftConnect's customer support operations:

### Finding 1: Channel Performance Disparities
**Insight:** The Phone channel consistently underperforms, showing the slowest average resolution time (~38.5 hrs) and the lowest average CSAT (3.42). In contrast, the Chat channel is the most efficient, resolving tickets fastest (~27.7 hrs) and achieving the highest CSAT (3.54).

**Power BI Report: Channel Performance Analysis Page**
*Visualizing average response and resolution times, and CSAT across different support channels.*

![Channel Performance Analysis](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/visualizations/Channel_Performance_Analysis.png?raw=true)

### Finding 2: Inefficient Priority Management
**Insight:** A critical operational flaw exists in priority handling. Low priority tickets are resolved the fastest on average, while Medium priority tickets are the slowest. This counter-intuitive result suggests a systemic issue in workflow or triage. High priority tickets, while receiving fast first responses, are not resolved optimally.

**Power BI Report: Priority Management Inefficiencies Page**
*Exploring how different priority levels impact resolution time and customer satisfaction.*

![Priority Management Analysis](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/visualizations/Priority_Management_Analysis.png?raw=true)

### Finding 3: Time-Based Demand & Performance Bottlenecks
**Insight:** SwiftConnect experiences peak ticket volume on Wednesdays, which worryingly correlates with the lowest weekly CSAT score. Saturdays, despite low volume, suffer from the slowest average resolution times, suggesting potential understaffing or process slowdowns during weekends.

**Power BI Report: Time-Based Demand & Performance Page**
*Analyzing ticket volume and performance metrics by hour and day of the week.*

![Time-Based Trends](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/visualizations/Time_Based%20_Trends.png?raw=true)

### Finding 4: Topic-Specific Resolution Challenges
**Insight:** 'Training request' and 'Pricing & licensing' tickets are significant pain points, exhibiting the longest resolution times and low customer satisfaction. This indicates these topics are complex and may require specialized agent knowledge or better support documentation.

**Power BI Report: Topic-Specific Challenges Page**
*Identifying which types of customer inquiries are most problematic in terms of resolution time and CSAT.*

![Topic Analysis](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/visualizations/Topic_Analysis.png?raw=true)

### Finding 5: CSAT Driven by Qualitative Factors, Not Just Speed
**Insight:** Resolution duration has a negligible linear correlation with the final CSAT score. Customers can be highly satisfied even with very long resolutions, and dissatisfied with quick ones. This strongly suggests that other qualitative factors (e.g., resolution quality, communication effectiveness, expectation management) are more influential than mere speed.

**Power BI Report: Driving Customer Satisfaction Page**
*A deeper look into what truly drives customer satisfaction beyond just the speed of resolution, including illustrative examples.*

![Customer Satisfaction Driver](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/visualizations/Customer_Satisfaction_Driver.png?raw=true)

---

## 5. Actionable Recommendations

Based on these findings, the following actionable recommendations are proposed to SwiftConnect Telecom's Customer Service leadership:

1.  **Optimize Phone Channel for Efficiency & Satisfaction:**
    * Conduct a root cause analysis of the phone channel's slow resolution and low CSAT. Review call recordings, agent scripts, and workflows to identify and address specific bottlenecks. Implement targeted training and process refinements.
2.  **Urgent Review and Redefinition of Priority Management & Support Workflow:**
    * Audit the end-to-end workflow for all priority levels. Address why Medium priority tickets are the slowest and why Low priority tickets resolve faster than High. Revise triage rules and agent focus to align with true business urgency and improve SLA adherence.
3.  **Optimize Workload Distribution and Staffing Aligned with Demand & Performance:**
    * Adjust staffing schedules to better handle peak volume on Wednesdays and address the efficiency drop on Saturdays. Ensure skilled agents are available during critical periods to prevent backlogs and maintain service quality.
4.  **Develop Targeted Expertise and Streamline Processes for Complex Topics:**
    * Investigate 'Training request' and 'Pricing & Licensing' inquiries. Develop specialized training, enhance knowledge base articles, and refine escalation paths for these and other complex topics to improve resolution efficiency and customer satisfaction.
5.  **Prioritize Qualitative Aspects of Service and Proactive Expectation Management to Drive CSAT:**
    * Shift focus from pure resolution speed to resolution quality, communication, and expectation management. Implement agent training on empathetic communication, transparent updates, and ensuring complete issue resolution, as these are key CSAT drivers.

**Power BI Report: Key Recommendations & Next Steps Page**
*A consolidated view of all actionable recommendations with an interactive drill-down for details.*

![Key Recommendations](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/visualizations/Key_Recommendations.png?raw=true)

---

## 6. Thought Process, Challenges & Solutions

This project involved navigating typical data analysis challenges, which shaped the final insights and solutions.

**Thought Process:**
The approach was iterative and focused on deriving actionable business insights from raw data. Each phase built upon the previous one, ensuring data integrity before analysis and feature engineering before drawing conclusions. The emphasis was always on answering "why" behind the numbers and translating technical findings into business language.

**Key Challenges & Solutions:**

* **Missing Values in Time Fields:**
    * **Challenge:** Initial inspection revealed numerous missing values in `First response time`, `Resolution time`, and `Close time`. Naively filling these would skew results.
    * **Solution:** Conducted a careful analysis correlating missing timestamps with ticket `Status`. For `Open` or `In Progress` tickets, `NaN`s were recognized as meaningful (event not yet occurred) and left as is. For `Resolved` tickets missing a `Close time`, it was reasonably imputed with the `Resolution time`, assuming effective closure upon resolution.
* **Negative First Response Time:**
    * **Challenge:** Identified two instances of negative `Actual_First_Response_Duration_Minutes` for the 'Phone' channel, indicating data logging errors.
    * **Solution:** Given the small number, these anomalous values were set to `0`, representing an effectively instantaneous response, preventing distortion of channel-specific averages while retaining the valid parts of the ticket data.
* **Categorical Data Standardization:**
    * **Challenge:** Inconsistent casing or leading/trailing spaces in categorical columns could create duplicate categories.
    * **Solution:** Applied `.str.lower().str.strip()` consistently across all text-based categorical columns to ensure uniformity.
* **Datetime Handling across Tools:**
    * **Challenge:** Ensuring date/time fields remained `datetime` objects in Python after loading/saving to CSV and then correctly imported as date/time types in Power BI was crucial for calculations.
    * **Solution:** Explicitly re-converted datetime columns using `pd.to_datetime()` after `pd.read_csv()` in Python, and verified Power BI's automatic type detection during import, adjusting manually where necessary.
* **Weak Linear Correlations:**
    * **Challenge:** Key intuitive relationships, like `Resolution Duration` and `CSAT`, showed negligible linear correlation, which was initially surprising.
    * **Solution:** Instead of forcing non-existent linear relationships, the analysis pivoted to investigate other, more qualitative and contextual factors (Channel, Priority, Topic, Communication Quality, Expectation Management) which proved to be stronger drivers of CSAT. This led to a more nuanced and impactful set of recommendations.
* **Power BI Design & Interactivity:**
    * **Challenge:** Presenting a large volume of insights clearly and making the report interactive without overwhelming the user.
    * **Solution:** Utilized multi-page structure, consistent UI/UX principles, strategic use of reference lines, and importantly, implemented **Bookmarks and Buttons** to create expandable/collapsible insights on each page, allowing users to drill down into details as desired.

---

## 7. Project Deliverables

* **Python Notebooks:**
    * [`01_data_exploration_cleaning.ipynb`](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/notebooks/01_data_exploration_cleaning.ipynb)
    * [`02_feature_engineering.ipynb`](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/notebooks/02_feature_engineering.ipynb)
    * [`03_EDA_and_Insights.ipynb`](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/notebooks/03_EDA_and_Insights.ipynb)
* **Data Files:**
    * **Raw Data:** [`Technical Support Dataset.csv`](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/data/raw/Technical%20Support%20Dataset.csv?raw=true)
    * **Cleaned Data:** [`technical_support_data_cleaned.csv`](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/data/technical_support_data_cleaned.csv?raw=true)
    * **Engineered Data:** [`technical_support_data_engineered.csv`](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/data/technical_support_data_engineered.csv?raw=true)
* **Power BI Report File:**
    * [`SwiftConnect Telecom Dashboard.pbix`](https://github.com/mrluke269/swiftconnect-support-analysis/blob/main/visualizations/SwiftConnect%20Telecom%20Dashboard.pbix)


---

## 8. Contact Information

**Analyst:** Luke Mai
**Email:** luke.trmai@gmail.com
**GitHub:** [mrluke269 (Luke Mai)](https://github.com/mrluke269)
