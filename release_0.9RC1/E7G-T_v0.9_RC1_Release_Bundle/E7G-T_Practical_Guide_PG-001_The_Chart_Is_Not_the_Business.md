# E7G-T Practical Guide — Chapter 1

# The Chart Is Not the Business

**Guide ID:** PG-001  
**Kernel compatibility:** E7G-T v0.9 draft  
**Related atlas entry:** APP-001 — AI Output as Projection  
**Related Proof-of-Path prototype:** POP-001 — Proof Assistant Session as Accountable Path  
**Status:** first practical-guide chapter draft  
**Date:** 2026-06-29  
**Primary use:** business reasoning, dashboard interpretation, management review, AI-assisted analysis, decision hygiene

---

## 1. The Everyday Mistake

A business chart looks simple.

Revenue went up.  
Sales went down.  
Conversion improved.  
Traffic collapsed.  
Profit margin narrowed.  
A region outperformed another region.  
A product looks like a winner.  
A campaign looks like a failure.

The temptation is immediate:

> “The chart shows what is happening.”

But this is already too strong.

A chart does not show the business.

A chart shows a **projection** of the business.

It is a selected, filtered, formatted, aggregated, time-bounded, context-dependent view of something richer.

That view may be useful. It may even be essential. But it is not the business itself.

The first practical rule is therefore:

> Do not let the chart become the business.

---

## 2. The E7G-T Repair

E7G-T repairs this mistake by asking a different first question.

Do not begin with:

> “What does the chart say?”

Begin with:

> “What is this chart a projection of?”

Then ask:

- What source produced it?
- What was selected?
- What was filtered out?
- What time window is active?
- What boundary was used?
- What structure is preserved?
- What structure is lost?
- What decision is this chart allowed to support?
- What decision would require source return?

This turns dashboard reading into projection-loss reading.

---

## 3. Simple OneLine

```text
E7-OneLine: The chart is treated as a D2 projection of a D4/D5 business system under reporting context; admissible move: inspect preservation, loss, and source data before causal decision; blocked overread: chart is not the business.
```

Plain meaning:

The chart is a visible surface view.  
The business is a richer, time-extended, possibility-bearing system.  
The chart may preserve useful metrics.  
It also loses causes, local exceptions, unrecorded events, and context.

---

## 4. Placement

### Compact placement

```text
Chart : D2 @ TR1 / ReportingContext
BusinessSystem : D4/D5 @ TR1-TR3 / OperatingContext
```

### Meaning

The chart is treated as:

- **D2** because it appears as a visible surface: graph, dashboard, table, or metric display;
- **TR1** because it is usually read in a local reporting moment;
- **ReportingContext** because the chart depends on selected reporting rules.

The business system is treated as:

- **D4** because it has history, process, operations, and time;
- **D5** because it contains alternatives, opportunities, risks, scenarios, and possible future branches;
- **TR1–TR3** because it includes actual sequence, current operations, and future scenarios.

The chart is not false because it is a projection.

It becomes dangerous only when its projection status is forgotten.

---

## 5. Projection Pattern

```text
BusinessSystem : D4/D5 @ TR1-TR3 / OperatingContext
  --π_Report^{4/5→2}-->
Chart : D2 @ TR1 / ReportingContext
[preserves: selected metric pattern;
 loses: causes, hidden variables, data exclusions, local exceptions, operational texture;
 use: management review, hypothesis generation, source-return trigger]
```

This is the basic dashboard grammar.

The chart preserves something.

The chart loses something.

The responsible manager asks both.

---

## 6. What the Chart May Preserve

A chart may preserve:

- trend direction;
- relative movement;
- comparison between periods;
- comparison between products;
- comparison between channels;
- metric magnitude;
- seasonality pattern;
- outlier signal;
- variance;
- ratio;
- target gap;
- reporting status;
- selected operational signal.

This is why charts are useful.

Without preservation, a chart would be noise.

---

## 7. What the Chart May Lose

A chart may lose:

- causes;
- data collection errors;
- stock availability;
- ad spend changes;
- price changes;
- seasonality;
- promotions;
- customer sentiment;
- supplier delays;
- logistics failures;
- website outages;
- tax or currency effects;
- team changes;
- unusual one-off events;
- local market conditions;
- product-quality problems;
- competitor actions;
- hidden segmentation;
- cancelled orders;
- returns;
- unpaid invoices;
- margin structure;
- human stories.

This is why charts are dangerous.

A chart can look precise while hiding what matters most.

---

## 8. Projection-Loss Ledger

Use this before making a decision from a chart.

| Question | Answer |
|---|---|
| What is the chart showing? | Name the exact metric. |
| What is the source? | Database, spreadsheet, CRM, ad platform, accounting system, manual entry, BI tool. |
| What is the time window? | Day, week, month, quarter, year, custom range. |
| What is the boundary? | Product, region, company, channel, team, customer segment, campaign. |
| What is preserved? | Trend, ratio, comparison, magnitude, variance, threshold, status. |
| What is lost? | Causes, exclusions, local anomalies, hidden assumptions, unrecorded events. |
| What does the chart allow? | Review, hypothesis, monitoring, alert, limited decision. |
| What does it not allow? | Causal conclusion, blame, strategy change, investment decision, firing, legal claim, unless further checked. |
| What source return is needed? | Raw data, filtered records, operational logs, customer feedback, accounting detail, interview, experiment. |
| What is the next move? | Verify, segment, compare, investigate, ask, test, wait, stop. |

---

## 9. Common Business Overreads

### 9.1 Trend equals cause

Bad reading:

> “Sales went down, so customers dislike the product.”

E7G-T repair:

Sales decline is a signal, not a cause.

Possible sources include:

- stockout;
- price increase;
- ad spend cut;
- search ranking loss;
- seasonal change;
- competitor promotion;
- review drop;
- delivery delay;
- payment issue;
- website bug;
- marketplace suppression;
- reporting error.

Blocked overread:

```text
Chart movement is not causal diagnosis.
```

---

### 9.2 Metric equals reality

Bad reading:

> “The dashboard says revenue is up, so the business is healthy.”

E7G-T repair:

Revenue may be up while:

- margin is down;
- cash flow is weak;
- returns are rising;
- customer acquisition cost is too high;
- stock is running out;
- supplier risk is growing;
- one customer dominates sales;
- unpaid invoices are increasing;
- team burnout is hidden;
- legal or tax risk is accumulating.

Blocked overread:

```text
One metric is not the business.
```

---

### 9.3 Slice equals whole

Bad reading:

> “This month was bad, so the product is failing.”

E7G-T repair:

A month is a slice.

Ask:

- What happened in the previous months?
- Is this seasonal?
- Was inventory normal?
- Did ad spend change?
- Did the marketplace algorithm change?
- Was there a holiday?
- Did one large customer delay purchase?
- Did reporting cut off early?

Blocked overread:

```text
Slice is not whole.
```

---

### 9.4 Dashboard equals source

Bad reading:

> “The dashboard says it, so it must be true.”

E7G-T repair:

The dashboard is downstream.

Return to:

- raw data;
- formulas;
- filters;
- sync status;
- time-zone settings;
- currency conversion;
- attribution model;
- data freshness;
- user permissions;
- manual overrides.

Blocked overread:

```text
Dashboard is not source.
```

---

### 9.5 Comparison equals fairness

Bad reading:

> “Region A is better than Region B.”

E7G-T repair:

Comparison requires boundary discipline.

Ask:

- Are the regions the same size?
- Do they have similar stock?
- Do they have similar ad spend?
- Are prices the same?
- Is the customer base comparable?
- Are logistics equal?
- Is the time window comparable?
- Are taxes, currency, and marketplace rules comparable?

Blocked overread:

```text
Comparison without boundary is not evaluation.
```

---

## 10. The Business Dashboard MiniCard

```yaml
id: PG-001-dashboard-review
entity: business chart / dashboard
plainMeaning: A visible metric projection of a richer business system.
placement: Chart : D2 @ TR1 / ReportingContext
sourceSystem: BusinessSystem : D4/D5 @ TR1-TR3 / OperatingContext
boundary:
  includes:
    - selected metric
    - selected time window
    - selected product/channel/region/team/customer segment
    - reporting rules
  excludes:
    - unmeasured causes
    - hidden operational context
    - raw human explanations
    - future scenarios not included in the chart
projectionAccount:
  source: operational data + reporting model + dashboard rendering
  view: visible chart or metric
preserved:
  - selected trend
  - selected comparison
  - selected magnitude
  - selected variance
lost:
  - causes
  - local exceptions
  - hidden filters
  - data errors
  - operational texture
distortionRisk:
  - aggregation hides segment variation
  - time window creates false trend
  - metric chosen biases decision
  - dashboard makes weak signal look authoritative
reconstructionStatus: partial; requires source return
bridgeMode: operational
admissibleUse:
  - monitoring
  - hypothesis generation
  - limited review
  - trigger for investigation
nonAdmissibleUse:
  - final causal conclusion without further evidence
  - blame assignment without investigation
  - major strategy change from one metric
nextMove: inspect source, segment, compare, and test causal hypothesis
blockedOverread: chart is not the business
```

---

## 11. The 7-Minute Dashboard Review

Use this quick procedure before trusting a chart.

### Minute 1 — Name the metric

What exactly is being shown?

Revenue? Orders? Profit? Gross margin? Sessions? Conversion? Click-through rate? Cash collected? Invoices issued? Units shipped?

Do not accept vague labels.

### Minute 2 — Name the source

Where did the data come from?

Accounting? Marketplace? CRM? ERP? Ad platform? Spreadsheet? Manual entry? BI tool? Bank account? Warehouse report?

### Minute 3 — Name the boundary

What is included?

What is excluded?

What time period, product group, country, channel, team, customer segment, or currency is active?

### Minute 4 — Name what is preserved

What useful pattern does the chart preserve?

Trend? Outlier? Comparison? Gap? Threshold? Seasonality? Ratio?

### Minute 5 — Name what is lost

What could explain the chart but is not visible in it?

Inventory? Ads? Price? returns? reviews? logistics? tax? customer concentration? reporting error?

### Minute 6 — Name the allowed decision

Can this chart support:

- monitoring only?
- further investigation?
- minor adjustment?
- urgent escalation?
- strategic decision?

### Minute 7 — Name the next move

Choose one:

- accept as monitoring signal;
- inspect raw data;
- segment the chart;
- compare another metric;
- ask operational team;
- run test;
- verify source;
- stop.

---

## 12. Worked Example: Revenue Drop

Chart:

> Monthly revenue dropped by 28%.

Bad conclusion:

> “The product is failing.”

E7G-T review:

```text
Entity: monthly revenue chart
Placement: RevenueChart : D2 @ TR1 / MonthlyReportingContext
Source: BusinessSystem : D4/D5 @ TR1-TR3 / OperatingContext
Projection: π_MonthlyRevenue(BusinessSystem) = RevenueChart
Preserves: revenue decline signal
Loses: cause, stock status, channel mix, ad spend, conversion, traffic, returns, pricing, seasonality
Reconstruction: underdetermined
Bridge mode: operational
Admissible use: investigation trigger
Blocked overread: revenue drop is not product failure
Next move: inspect stock, traffic, conversion, ads, price, reviews, and channel segmentation
```

Better conclusion:

> “Revenue dropped by 28% in this reporting slice. The chart supports investigation, not yet causal diagnosis.”

---

## 13. Worked Example: Conversion Increase

Chart:

> Conversion rate increased from 2.1% to 3.4%.

Bad conclusion:

> “The website is performing better.”

E7G-T review:

Possible hidden causes:

- low-quality traffic disappeared;
- ad campaign changed;
- returning customers increased;
- discount was added;
- product mix changed;
- tracking changed;
- sessions fell while purchases stayed stable;
- bot traffic was filtered;
- page speed improved;
- checkout bug was fixed.

The chart preserves conversion ratio movement.

It loses traffic composition and cause.

Better conclusion:

> “Conversion improved in this slice, but the reason is not visible in the chart.”

---

## 14. Worked Example: Product Comparison

Chart:

> Product A sells twice as much as Product B.

Bad conclusion:

> “Product A is better.”

E7G-T review:

Ask:

- Was Product B in stock?
- Was Product A advertised more?
- Are prices comparable?
- Are margins comparable?
- Is Product B newer?
- Does Product B have fewer reviews?
- Are shipping times equal?
- Is Product A seasonal?
- Does Product B have higher repeat purchase?
- Does Product B produce better profit despite lower revenue?

Better conclusion:

> “Product A shows higher sales under this reporting boundary. Product quality, profitability, and strategic value require additional projections.”

---

## 15. AI-Assisted Business Analysis

AI can help interpret charts, but the AI answer is also a projection.

This creates a projection stack:

```text
BusinessSystem
  --π_Dashboard-->
Chart
  --π_AIInterpretation-->
AIAnalysis
```

Loss accumulates.

The AI may lose even more:

- source data;
- formulas;
- operational detail;
- hidden filters;
- business context;
- local exceptions;
- current events;
- domain constraints.

### Safe AI use

Use AI to:

- generate hypotheses;
- list possible causes;
- create checklists;
- suggest segmentation;
- draft questions;
- identify missing data;
- structure a review.

### Unsafe AI use

Do not use AI to:

- make final causal claims without data;
- replace accounting;
- replace legal/tax review;
- blame a person or team;
- decide layoffs;
- approve major investment;
- infer customer psychology without evidence.

### AI dashboard OneLine

```text
E7-OneLine: AI dashboard analysis is treated as a D2/D7 projection of an already projected chart under user-query context; admissible move: use as hypothesis list and verify against source; blocked overread: AI interpretation of chart is not business reality.
```

---

## 16. The Business Review Card

Use this before a management meeting.

```yaml
meeting:
chart:
metric:
source:
timeWindow:
boundary:
preservedPattern:
lostContext:
possibleCauses:
  - 
requiredSourceReturn:
  - 
decisionRequested:
admissibleDecision:
nonAdmissibleDecision:
riskOfOverread:
nextMove:
owner:
deadline:
```

---

## 17. Decision Tiers

| Tier | Meaning | Chart use |
|---|---|---|
| Tier 0 | Notice | Chart can alert. |
| Tier 1 | Monitor | Chart can support ongoing observation. |
| Tier 2 | Investigate | Chart can trigger source return. |
| Tier 3 | Hypothesise | Chart can support possible explanations. |
| Tier 4 | Test | Chart can inform experiment design. |
| Tier 5 | Decide | Chart plus sufficient evidence can support action. |
| Tier 6 | Commit | Decision requires broader evidence, ownership, and accountability. |

### Tier rule

A chart alone rarely supports Tier 5 or Tier 6 decisions.

---

## 18. Practical Prompts

### Prompt 1 — Basic chart review

```text
Use E7G-T to review this chart. Treat it as a projection, not the business itself. Identify the source, boundary, preserved pattern, lost context, possible distortions, admissible use, blocked overread, and next move.
```

### Prompt 2 — Causal claim check

```text
This chart seems to suggest [claim]. Use E7G-T to test whether that causal conclusion is justified. Separate signal, possible causes, missing evidence, and next investigation steps.
```

### Prompt 3 — Dashboard meeting preparation

```text
Prepare a business review card for this dashboard. For each major metric, identify what it preserves, what it loses, what decision it can support, what decision it cannot support, and what source return is required.
```

### Prompt 4 — AI interpretation check

```text
Review this AI-generated business analysis as a projection of a projection. Identify where the AI may overread the chart, where source return is needed, and what claims must be downgraded.
```

---

## 19. Stop Conditions

Stop or downgrade the chart-based claim when:

- the metric is undefined;
- the source is unknown;
- the time window is unclear;
- the boundary is hidden;
- the chart is based on stale data;
- the chart aggregates incompatible segments;
- the causal claim exceeds the data;
- the decision risk is high;
- the chart conflicts with another source;
- the chart has not been reconciled with accounting or operations;
- the AI interpretation adds unsupported causes;
- the action would affect people, finances, legal exposure, or strategy without source return.

---

## 20. Chapter Summary

A chart is useful because it preserves selected structure.

A chart is dangerous because it loses structure.

The business is richer than the chart.

The responsible move is not to reject charts.

The responsible move is to read them as projections.

The practical question is:

> What does this chart preserve, what does it lose, and what may I responsibly do next?

---

## 21. Closing Rule

The chart is not the business.

The dashboard is not the source.

The metric is not the cause.

The slice is not the whole.

Return to source when reliance matters.
