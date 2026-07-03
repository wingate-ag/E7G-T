# E7G-T Practical Guide Worksheet — PG-001

# Dashboard Projection-Loss Review

**Worksheet ID:** PG-001-W  
**Related chapter:** PG-001 — The Chart Is Not the Business  
**Kernel compatibility:** E7G-T v0.9 draft  
**Status:** reusable worksheet / pilot tool  
**Date:** 2026-06-29  
**Primary use:** dashboard review, management meetings, business analysis, AI-assisted chart interpretation, decision hygiene

---

## 1. Purpose

Use this worksheet whenever a chart, dashboard, KPI, table, or metric is being used to support a business conclusion.

The worksheet is built on one rule:

> The chart is not the business.

A chart is a projection. It preserves selected structure and loses other structure. Before relying on it, identify what it preserves, what it loses, and what decision it can responsibly support.

---

## 2. Fast OneLine

```text
E7-OneLine: This chart is treated as a D2 projection of a D4/D5 business system under reporting context; admissible move: inspect preservation, loss, and source return before decision; blocked overread: chart is not the business.
```

---

## 3. Worksheet — Quick Version

Use this version during meetings.

| Field | Answer |
|---|---|
| Chart / dashboard title |  |
| Metric shown |  |
| Source system |  |
| Time window |  |
| Boundary |  |
| What the chart preserves |  |
| What the chart loses |  |
| Possible distortions |  |
| Claim being made from the chart |  |
| Admissible decision tier |  |
| Non-admissible decision |  |
| Source return needed |  |
| Next move |  |
| Owner |  |
| Review date |  |
| Stop condition |  |

---

## 4. Worksheet — Full Version

### 4.1 Chart identity

**Chart / dashboard title:**  
`[insert title]`

**Metric shown:**  
`[revenue / profit / orders / conversion / traffic / margin / cash / retention / other]`

**Metric definition:**  
`[define exactly what is counted and how]`

**Unit:**  
`[currency / percentage / count / ratio / index / score / other]`

**Source system:**  
`[accounting / CRM / ERP / marketplace / ad platform / spreadsheet / BI tool / manual entry / other]`

**Data freshness:**  
`[live / daily / weekly / monthly / unknown]`

**Last updated:**  
`[date/time]`

---

### 4.2 Boundary

**Time window:**  
`[day / week / month / quarter / year / custom range]`

**Business boundary:**  
`[company / product / region / channel / customer segment / campaign / team / warehouse / other]`

**Included:**  

- 
- 
- 

**Excluded:**  

- 
- 
- 

**Boundary risk:**  
`[What may be hidden because of the chosen boundary?]`

---

### 4.3 Projection account

```text
BusinessSystem : D4/D5 @ TR1-TR3 / OperatingContext
  --π_Report^{4/5→2}-->
Chart : D2 @ TR1 / ReportingContext
```

**Plain-language projection account:**  
`[This chart projects which part of the business into which visible metric?]`

**What source reality is richer than this chart?**

- 
- 
- 

---

### 4.4 Preserved pattern

What does the chart preserve?

Tick or fill in:

- [ ] Trend direction
- [ ] Magnitude
- [ ] Period comparison
- [ ] Product comparison
- [ ] Channel comparison
- [ ] Regional comparison
- [ ] Ratio
- [ ] Variance
- [ ] Outlier
- [ ] Seasonality
- [ ] Target gap
- [ ] Threshold crossing
- [ ] Other: 

**Preserved pattern in one sentence:**  
`[The chart reliably shows...]`

---

### 4.5 Lost context

What might the chart lose?

Tick or fill in:

- [ ] Cause
- [ ] Stock availability
- [ ] Ad spend
- [ ] Pricing changes
- [ ] Discounts / promotions
- [ ] Seasonality
- [ ] Customer sentiment
- [ ] Reviews
- [ ] Returns
- [ ] Logistics issues
- [ ] Supplier issues
- [ ] Website / checkout problems
- [ ] Marketplace algorithm changes
- [ ] Competitor action
- [ ] Team capacity
- [ ] Tax / currency effects
- [ ] Unpaid invoices
- [ ] Margin structure
- [ ] Segment differences
- [ ] Data errors
- [ ] Manual overrides
- [ ] Other: 

**Lost context in one sentence:**  
`[The chart does not show...]`

---

### 4.6 Distortion risks

Tick any risk that applies:

- [ ] Aggregation hides segment differences.
- [ ] Time window creates false trend.
- [ ] Metric definition is unclear.
- [ ] Data source may be stale.
- [ ] Dashboard filter may be wrong.
- [ ] Attribution model may be misleading.
- [ ] Currency/tax settings may distort comparison.
- [ ] One-off event may dominate the result.
- [ ] Chart design exaggerates movement.
- [ ] AI interpretation added unsupported causes.
- [ ] Comparison groups are not equivalent.
- [ ] Other: 

**Main distortion risk:**  
`[insert]`

---

## 5. Claim Review

### 5.1 Claim being made

Write the claim someone wants to make from the chart:

```text
[Example: Sales are down because customers dislike the product.]
```

### 5.2 Claim type

Tick the type:

- [ ] Monitoring claim
- [ ] Descriptive claim
- [ ] Comparative claim
- [ ] Causal claim
- [ ] Forecast claim
- [ ] Blame / accountability claim
- [ ] Strategic decision claim
- [ ] Financial / accounting claim
- [ ] Legal / compliance claim
- [ ] AI-generated interpretation
- [ ] Other: 

### 5.3 Claim-strength check

| Question | Answer |
|---|---|
| Does the chart directly support the claim? |  |
| Does the claim require cause? |  |
| Does the claim require another metric? |  |
| Does the claim require raw data? |  |
| Does the claim require human/operational explanation? |  |
| Does the claim require expert review? |  |
| Should the claim be downgraded? |  |

### 5.4 Safer rewritten claim

Rewrite the claim in a safer form:

```text
[Example: Revenue dropped in this reporting slice. The chart supports investigation, but not yet causal diagnosis.]
```

---

## 6. Source-Return Checklist

Return to source before a strong decision.

Tick what needs to be checked:

- [ ] Raw data
- [ ] Dashboard filters
- [ ] Data refresh status
- [ ] Metric formula
- [ ] Accounting records
- [ ] Marketplace reports
- [ ] CRM records
- [ ] Ad platform data
- [ ] Website analytics
- [ ] Stock/inventory records
- [ ] Pricing history
- [ ] Promotion history
- [ ] Returns/refunds
- [ ] Customer feedback
- [ ] Reviews
- [ ] Logistics/shipping data
- [ ] Supplier records
- [ ] Team notes
- [ ] Competitor/market context
- [ ] Other: 

**Required source return:**  

1. 
2. 
3. 

---

## 7. Decision Tier

Choose the highest decision tier this chart can support **before** source return.

| Tier | Decision level | Allowed? |
|---|---|---|
| Tier 0 | Notice | [ ] |
| Tier 1 | Monitor | [ ] |
| Tier 2 | Investigate | [ ] |
| Tier 3 | Hypothesise | [ ] |
| Tier 4 | Test | [ ] |
| Tier 5 | Decide | [ ] |
| Tier 6 | Commit | [ ] |

### Tier rule

A chart alone rarely supports Tier 5 or Tier 6.

**Selected tier:**  
`[insert]`

**Reason:**  
`[insert]`

---

## 8. Admissible and Non-Admissible Uses

### Admissible use

This chart can responsibly be used for:

- [ ] Monitoring
- [ ] Alerting
- [ ] Hypothesis generation
- [ ] Management discussion
- [ ] Source-return trigger
- [ ] Minor adjustment
- [ ] Test design
- [ ] Decision support after additional checks
- [ ] Other: 

### Non-admissible use

This chart should **not** be used for:

- [ ] Final causal conclusion
- [ ] Blame assignment
- [ ] Layoff / personnel decision
- [ ] Major investment decision
- [ ] Legal/compliance claim
- [ ] Financial reporting without reconciliation
- [ ] Strategy change without source return
- [ ] AI-generated causal conclusion without verification
- [ ] Other: 

---

## 9. Next Move

Choose one next move:

- [ ] Accept as low-risk monitoring signal.
- [ ] Inspect raw data.
- [ ] Segment by product / region / channel / customer group.
- [ ] Compare with another metric.
- [ ] Check stock, price, ads, traffic, conversion, returns, reviews.
- [ ] Ask operations/team for explanation.
- [ ] Run an experiment.
- [ ] Reconcile with accounting.
- [ ] Verify AI interpretation.
- [ ] Downgrade claim.
- [ ] Stop.

**Next move in one sentence:**  
`[insert]`

**Owner:**  
`[insert]`

**Deadline / review date:**  
`[insert]`

---

## 10. Stop Conditions

Stop or downgrade the chart-based claim if:

- [ ] The metric is undefined.
- [ ] The source is unknown.
- [ ] The time window is unclear.
- [ ] The boundary is hidden.
- [ ] The chart is stale.
- [ ] The chart aggregates incompatible segments.
- [ ] The causal claim exceeds the data.
- [ ] Decision risk is high.
- [ ] The chart conflicts with another source.
- [ ] Accounting or operational data has not been checked.
- [ ] AI interpretation adds unsupported causes.
- [ ] The action would affect people, finances, legal exposure, or strategy without source return.

**Stop condition triggered:**  
`[yes/no]`

**Reason:**  
`[insert]`

---

## 11. Completed Review Summary

Use this block at the end of the review.

```text
The chart shows: [metric/pattern].

It preserves: [preserved structure].

It loses: [lost context].

The strongest admissible claim is: [safe claim].

The chart does not support: [blocked overread].

The decision tier is: [tier].

The next move is: [next move].

Owner: [name].

Review date: [date].
```

---

## 12. Example Completed Summary

```text
The chart shows a 28% monthly revenue drop.

It preserves the selected revenue decline in the monthly reporting slice.

It loses cause, stock status, ad spend, traffic composition, conversion detail, pricing history, returns, and channel segmentation.

The strongest admissible claim is: revenue dropped in this reporting slice.

The chart does not support: the product is failing.

The decision tier is: Tier 2 — Investigate.

The next move is: inspect stock, traffic, conversion, ad spend, returns, and channel-level revenue.

Owner: Sales operations.

Review date: 2026-06-30.
```

---

## 13. AI Prompt Version

Use this prompt with an AI assistant:

```text
Use E7G-T PG-001 Worksheet: Dashboard Projection-Loss Review.

Treat the chart/dashboard as a D2 projection of a richer D4/D5 business system.

Do not treat the chart as the business.

Identify:
1. metric definition;
2. source system;
3. time window;
4. boundary;
5. preserved pattern;
6. lost context;
7. distortion risks;
8. claim being made;
9. admissible decision tier;
10. non-admissible use;
11. source-return checklist;
12. safer rewritten claim;
13. next move;
14. stop condition.

Block any unsupported causal claim.
```

---

## 14. Closing Reminder

The chart is not the business.

The dashboard is not the source.

The metric is not the cause.

The slice is not the whole.

Return to source when reliance matters.
