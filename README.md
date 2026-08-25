# dqlab-finance-branch-performance
Data analysis project to evaluate DQLab Finance branch performance using Power BI.

# DQLab Finance – Branch Performance Analysis

📊 Project Overview

This project analyzes the branch performance of DQLab Finance for May 2020 using Power BI.

The analysis focuses on identifying high- and low-performing branches, evaluating branch performance based on branch age, and investigating underperforming branches within the same age group.

This project is based on a DQLab Finance case study and was developed as part of my Data Analyst portfolio to demonstrate skills in data analysis, business insight generation, and data visualization.

---

🎯 Business Problem

DQLab Finance has been expanding by opening new branches every month. Because branches have different operating ages, comparing their performance directly may not provide a fair evaluation.

Management needs to understand:

* Which branches performed the best and worst in May 2020?
* How does branch age relate to branch performance?
* Which branches underperformed compared with branches of similar age?
* What operational factors may contribute to low branch performance?
* What actions could be taken to improve branch performance?

---

🎯 Project Objectives

The objectives of this analysis are to:

1. Analyze branch performance during May 2020.
2. Identify the top 5 and bottom 5 branches based on total loan disbursement.
3. Calculate branch age based on the first loan disbursement date.
4. Compare branch performance across different age groups.
5. Identify underperforming branches within each age group.
6. Investigate possible operational factors behind low branch performance.
7. Provide business recommendations based on the findings.

---

📁 Dataset

The dataset contains 9,754 loan transactions with 5 variables:

| Column         | Description                           |
| -------------- | ------------------------------------- |
| `loan_id`      | Unique identifier for each loan       |
| `tanggal_cair` | Loan disbursement date                |
| `cabang`       | Branch where the transaction occurred |
| `agen`         | Field agent responsible for the loan  |
| `amount`       | Loan disbursement amount              |

The dataset covers the period from January to May 2020.

There are:

* 9,754 transactions
* 22 branches
* 52 agents
* 5 variables

---

🛠 Tools

* Power BI – Data analysis and visualization
* Data Cleaning & Transformation – Preparing transaction data for analysis
* Data Visualization – Branch performance comparison
* Descriptive Analysis – Identifying performance patterns and outliers

---


🔎 Analysis Process

The analysis was conducted through the following steps:

 1. Filter Data for May 2020

The dataset was filtered to include only transactions occurring during May 2020.

The May 2020 dataset contains:

* 3,768 loan transactions
* 22 branches
* 52 active agents
* Rp1.1463 billion total disbursement
* Rp304,220 average disbursement per loan

---

### 2. Branch Performance Summary

Branch performance was measured using total loan disbursement amount.

The branches were ranked to identify the top 5 and bottom 5 performers.

### Top 5 Branches

| Rank | Branch | Total Disbursement |
| ---: | ------ | -----------------: |
|    1 | AC     |           Rp83.99M |
|    2 | AB     |           Rp81.44M |
|    3 | AD     |           Rp76.08M |
|    4 | AA     |           Rp75.71M |
|    5 | AG     |           Rp74.08M |

AC was the highest-performing branch in May 2020, generating approximately Rp83.99 million in total disbursement.

### Bottom 5 Branches

| Rank | Branch | Total Disbursement |
| ---: | ------ | -----------------: |
|    1 | AV     |           Rp30.28M |
|    2 | AS     |           Rp31.74M |
|    3 | AT     |           Rp34.84M |
|    4 | AU     |           Rp35.61M |
|    5 | AO     |           Rp39.12M |

AV recorded the lowest total disbursement at approximately Rp30.28 million.

---

## 📈 Branch Age Analysis

Because DQLab Finance opens new branches over time, branch age was calculated based on the first recorded loan disbursement date.

For this analysis, branch age was evaluated as the number of months from the first disbursement until the May 2020 analysis period.

### Branch Age Groups

| Branch Age | Branches           |
| ---------: | ------------------ |
|   0 months | AS, AT, AU, AV     |
|    1 month | AN, AO, AP, AQ, AR |
|   2 months | AI, AJ, AK, AL, AM |
|   3 months | AE, AF, AG, AH     |
|   4 months | AA, AB, AC, AD     |

The analysis shows a general pattern:

> Older branches tend to have higher total disbursement than newer branches.

This is reasonable because older branches have had more time to establish their operations, develop their agent networks, and build their customer base.

However, branch age alone does not explain all performance differences.

---

## 🚨 Underperforming Branch Analysis

To make branch comparisons more meaningful, branches were compared with other branches within the same age group.

An underperforming branch was identified using the Q1 − IQR threshold within each branch-age group.

The analysis identified two notable underperforming branches:

| Branch |      Age | Total Disbursement |
| ------ | -------: | -----------------: |
| AE     | 3 months |           Rp54.20M |
| AL     | 2 months |           Rp40.65M |

### Branch AE

Branch AE generated Rp54.20 million, considerably lower than other 3-month-old branches.

For example:

* AE: Rp54.20M
* AF: Rp68.04M
* AG: Rp74.08M
* AH: Rp73.84M

This indicates that AE was not simply performing poorly because it was a relatively new branch. It was also underperforming compared with branches of the same age.

---

## 👥 Agent-Level Investigation

To understand the possible reason behind AE's low performance, agent activity was analyzed.

Branch AE

| Agent | Active Days | Loans | Total Disbursement |
| ----- | ----------: | ----: | -----------------: |
| AE-1  |          21 |    86 |           Rp25.85M |
| AE-2  |          18 |    73 |           Rp23.38M |
| AE-3  |           4 |    16 |            Rp4.97M |

Agent AE-3 was active for only 4 days during May, compared with 18–21 active days for the other agents.

AE-3 generated only Rp4.97 million, which was substantially lower than the other agents.

This suggests that agent activity and loan volume may be important drivers of branch performance.

---

⭐ Comparison with a High-Performing Branch

Branch AH provides a useful comparison because it belongs to the same 3-month age group but achieved a much higher total disbursement.

Branch AH

| Agent | Active Days | Loans | Total Disbursement |
| ----- | ----------: | ----: | -----------------: |
| AH-1  |          21 |    81 |           Rp24.41M |
| AH-2  |          21 |    86 |           Rp26.96M |
| AH-3  |          19 |    74 |           Rp22.47M |

All three AH agents were active for approximately 19–21 days.

This resulted in a total branch disbursement of approximately Rp73.84 million, compared with Rp54.20 million for AE.

The comparison suggests that consistent agent activity contributes to higher loan volume and branch performance.

---

💡 Key Insights

1. Branch age is associated with performance

Older branches generally generated higher total disbursement.

The oldest branches, operating for approximately 4 months, occupied the top positions in the May 2020 performance ranking.

However, branch age should not be considered the only performance driver.

2. The top-performing branch was AC

Branch AC achieved the highest May 2020 total disbursement at approximately:

Rp83.99 million

3. The lowest-performing branch overall was AV

Branch AV generated approximately:

Rp30.28 million

However, because AV was a newly established branch, its performance should be evaluated in the context of its branch age.

4. AE was a notable underperformer among 3-month-old branches

AE generated Rp54.20 million, while other branches of the same age generated approximately Rp68–74 million.

5. Agent activity appears to be an important operational factor

The investigation of AE showed that one agent was active for only 4 days during May.

Compared with AH, where all agents were active for approximately 19–21 days, AE's lower agent activity was accompanied by lower loan volume and total disbursement.

---

🎯 Business Recommendations

Based on the analysis, several actions could be considered by management:

1. Monitor agent activity

Management should monitor the number of active days and loan volume generated by each agent.

Agents with significantly lower activity should be investigated to understand the underlying reasons.

2. Evaluate underperforming branches within their peer group

Branch performance should not be evaluated solely using an overall ranking.

Branches should first be compared with branches of similar age to create a fairer benchmark.

3. Use high-performing branches as benchmarks

Branches such as AC and AH can be used as benchmarks to identify operational practices that contribute to stronger performance.

4. Investigate low agent productivity

For branches such as AE, management should investigate why certain agents have significantly fewer active days.

Possible factors could include:

* customer acquisition difficulties;
* geographic or operational constraints;
* agent availability;
* differences in customer demand;
* workload or territory allocation.

Further operational data would be required to determine the exact cause.

5. Establish regular branch monitoring

A recurring Power BI dashboard could be used to monitor:

* Total loan disbursement
* Number of loans
* Active agents
* Agent activity
* Branch performance by age
* Underperforming branches

This would allow management to identify performance issues earlier.

---

📊 Dashboard

The Power BI dashboard developed for this project is available below:

[View Power BI Dashboard PDF](./dashboard/Project%20Data%20Analysis%20for%20Finance%20Performa%20Cabang.pdf)

The dashboard contains the main analysis covering:

* May 2020 branch performance
* Top and bottom performing branches
* Branch age analysis
* Underperforming branches by age group

---

 📌 Conclusion

The analysis shows that branch age is associated with branch performance, with older branches generally achieving higher total loan disbursement.

However, comparing branches only by overall performance can be misleading because branches operate for different lengths of time.

A more meaningful approach is to compare branches within similar age groups and then investigate operational factors behind significant performance differences.

The comparison between branches AE and AH highlights the importance of agent activity. AE had one agent active for only 4 days during May, while AH's agents were active for approximately 19–21 days. This difference was accompanied by a substantial gap in loan volume and total disbursement.

Therefore, branch performance monitoring should combine branch-level metrics with agent-level activity to provide a more actionable view for management.

---

📂 Project Structure

📁 dashboard
   └── Project Data Analysis for Finance Performa Cabang.pdf

📁 data
   └── Project Data Analysis for Finance Performa Cabang.csv

📁 powerbi
   └── Project Data Analysis for Finance Performa Cabang.pbix

📄 README.md
---

 📚 Project Reference

This project is based on the DQLab Finance branch performance case study.

The analysis was independently implemented using Power BI as part of my Data Analyst portfolio.
