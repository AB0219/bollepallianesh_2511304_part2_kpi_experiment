# Hypothesis Test Notes

## Objective

The objective of this experiment is to determine whether the new onboarding and activation campaign (Treatment) results in a significantly higher Paid Conversion Rate compared to the existing onboarding experience (Control).



# Primary Metric

**Paid Conversion Rate**

Paid Conversion Rate = Number of users converted to paid ÷ Total users

This metric was selected because it directly reflects the primary business goal of increasing subscription revenue.



# Business Question

Should the company launch the new onboarding campaign to all users?



# Null Hypothesis (H₀)

There is **no statistically significant difference** in Paid Conversion Rate between the Control and Treatment groups.

[
H_0 : p_{Treatment}=p_{Control}
]



# Alternative Hypothesis (H₁)

The Treatment group has a **higher Paid Conversion Rate** than the Control group.

[
H_1 : p_{Treatment}>p_{Control}
]



# Test Type

**One-tailed Two-Proportion Z-Test**

### Reason

The business objective is specifically to determine whether the Treatment improves conversion rather than simply being different.

Therefore, a one-tailed hypothesis test is appropriate.



# Significance Level

[
\alpha = 0.05
]

Confidence Level = **95%**



# Test Inputs

The following inputs are used:

* Number of Control users
* Number of Treatment users
* Number of Paid Conversions in Control
* Number of Paid Conversions in Treatment

These values are obtained from:

`outputs/experiment_summary.xlsx`



# Test Statistic

A Two-Proportion Z-Test compares the conversion proportions of two independent groups.

The pooled conversion rate is calculated first.

The Z-statistic is then computed as:

[
Z=\frac{p_1-p_2}{SE}
]

where

* (p_1) = Treatment Conversion Rate
* (p_2) = Control Conversion Rate



# Decision Rule

If

* p-value < 0.05

Reject the Null Hypothesis.

Otherwise,

Fail to Reject the Null Hypothesis.



# Interpretation Logic

### Case 1

If p-value < 0.05

* Treatment significantly improves conversion.
* Proceed to evaluate guardrail metrics before recommending rollout.



### Case 2

If p-value ≥ 0.05

* Evidence is insufficient to conclude that Treatment performs better.
* Continue testing or retain the existing onboarding.



# Guardrail Metrics

The launch decision should not rely only on conversion improvement.

The following guardrails must also be evaluated:

* Refund Rate
* Support Ticket Rate
* Average Engagement Score
* Average Days to Convert
* Revenue Quality
* Segment-Level Performance


# Business Interpretation

A statistically significant increase in Paid Conversion Rate indicates that the Treatment campaign is more effective at converting users into paying customers.

However, if this improvement comes with:

* Higher refund rates
* Lower engagement
* Increased customer support
* Longer conversion time

then the Treatment may negatively affect long-term business performance.



# Final Recommendation Logic

Recommend **Launch** if:

* Paid Conversion Rate significantly improves.
* Refund Rate does not materially increase.
* Support Ticket Rate remains stable.
* Engagement Score does not decline.
* Revenue quality is maintained.

Recommend **Continue Testing** if:

* Statistical significance is not achieved.
* Guardrail metrics indicate elevated business risk.
* Performance improvements are inconsistent across customer segments.



# Conclusion

The hypothesis test provides statistical evidence to support the business decision regarding rollout of the new onboarding experience. The final recommendation should combine the hypothesis test results with guardrail metric evaluation and segment-level analysis rather than relying solely on the primary conversion metric.
