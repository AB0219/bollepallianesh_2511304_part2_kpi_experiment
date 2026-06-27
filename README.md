# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and early engagement. Users were randomly assigned to one of two groups:

* **Control Group:** Existing onboarding experience
* **Treatment Group:** New onboarding and activation campaign

The objective is to determine whether the new onboarding experience should be launched to all users based on experimental evidence.



## Business Problem

The company must decide whether the new onboarding experience should replace the existing onboarding process.

This decision impacts:

* Product Management
* Marketing Team
* Customer Success Team
* Revenue Growth

The desired outcome is to improve the paid conversion rate while maintaining healthy customer experience metrics.

Before recommending a full rollout, the experiment must demonstrate:

* Statistically meaningful improvement in the primary success metric.
* No unacceptable increase in refund requests.
* No increase in customer support burden.
* No decline in user engagement or revenue quality.



# Dataset Description

The dataset contains user-level experimental data for both the Control and Treatment groups.

Each record represents one user and includes information such as:

* Experiment Group
* Landing Page Visit
* Trial Started
* Onboarding Completion
* Paid Conversion
* Revenue
* Refund Status
* Support Tickets
* Engagement Score
* Days to Convert
* Region
* Device Type
* Traffic Source
* Plan Type



# Business Decision

**Decision Required**

Determine whether the Treatment group should be:

* Fully launched
* Not launched
* Rolled out only for selected user segments
* Tested further before launch



# North Star Metric

## Paid Conversion Rate

### Why it was selected

The primary objective of the onboarding campaign is to convert more users into paying customers.

Paid Conversion Rate directly measures whether the onboarding experience generates additional revenue.

### Supporting Metrics

The following are supporting KPIs:

* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Average Revenue Per User
* Average Revenue Per Converted User
* Engagement Score
* Days to Convert

These metrics explain *why* conversion changed rather than representing the ultimate business objective.

### Risk of Optimizing Only the North Star

Optimizing only Paid Conversion Rate may:

* Increase refund requests
* Increase support workload
* Reduce customer satisfaction
* Lower long-term retention
* Encourage low-quality conversions

Therefore, guardrail metrics are also evaluated.



# KPI Tree Summary

**North Star Metric**

* Paid Conversion Rate

**Primary Drivers**

1. User Acquisition Quality

   * Landing Page Visit Rate
   * Traffic Source Quality

2. Activation Quality

   * Trial Start Rate
   * Onboarding Completion Rate

3. Revenue Performance

   * Average Revenue Per User
   * Average Revenue Per Converted User

**Guardrail Metrics**

* Refund Rate
* Support Ticket Rate
* Engagement Score
* Average Days to Convert



# Data Cleaning & Preparation

The dataset was reviewed for:

* Missing values
* Duplicate User IDs
* Group counts
* Invalid binary values
* Revenue outliers
* Segment balance across experiment groups

The cleaned dataset was used for all subsequent analyses.



# Experiment Analysis Approach

The following metrics were compared between the Control and Treatment groups:

* User Count
* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Paid Conversion Rate
* Average Revenue Per User
* Average Revenue Per Converted User
* Refund Rate
* Support Ticket Rate
* Average Engagement Score
* Average Days to Convert

Segment-level analysis was also performed for:

* Region
* Device Type
* Traffic Source
* Plan Type



# Hypothesis Testing

A statistical hypothesis test was performed on the primary KPI.

**Null Hypothesis (H₀)**

There is no significant difference in Paid Conversion Rate between the Control and Treatment groups.

**Alternative Hypothesis (H₁)**

The Treatment group has a significantly higher Paid Conversion Rate than the Control group.

A significance level of **5% (α = 0.05)** was used.

The p-value obtained from the hypothesis test determined whether the observed improvement was statistically significant.



# Guardrail Metrics Evaluated

The recommendation was not based solely on conversion improvement.

The following guardrails were evaluated:

* Refund Rate
* Support Ticket Rate
* Engagement Score
* Average Days to Convert
* Revenue Quality
* Segment-level performance



# Final Recommendation

The recommendation is based on:

* North Star Metric performance
* Statistical significance
* Guardrail metrics
* Revenue impact
* Segment-level insights

The final recommendation is documented in:

`outputs/recommendation_memo.md`



# Repository Structure

```
part2_kpi_experiment/
│
├── data/
├── analysis/
├── outputs/
├── screenshots/
└── README.md
```



# Files Included

* campaign_experiment_data.xlsx
* experiment_analysis.xlsx
* experiment_summary.xlsx
* hypothesis_test_notes.md
* recommendation_memo.md
* kpi_tree.png
* summary_metrics.png
* hypothesis_test_output.png
* kpi_tree_preview.png



# Assumptions & Limitations

* Users were randomly assigned to experiment groups.
* The dataset accurately represents campaign performance.
* Statistical conclusions are based on the available sample.
* Long-term retention effects are outside the scope of this experiment.



# Screenshots Included

* Summary Metrics
* Hypothesis Test Output
* KPI Tree Preview



# Conclusion

The experiment evaluates whether the new onboarding experience creates measurable business value while protecting customer experience through guardrail metrics. The final rollout recommendation is supported by KPI analysis, hypothesis testing, and business reasoning.
