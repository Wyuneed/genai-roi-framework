# Measurement Plan Template

> **Purpose:** Define your KPIs, baseline measurements, data collection methods, and review cadence *before* you deploy. A measurement plan created after the fact is far less credible and harder to execute.

---

# Measurement Plan: [Project Name]

**Prepared by:** [Name]
**Date:** [Date]
**Review Cycle:** [Monthly / Quarterly]
**Plan Owner:** [Name, Title]

---

## 1. Measurement Objectives

> *What are you trying to prove? List 2–4 clear objectives.*

1. Demonstrate that [Project Name] reduces [primary metric] by at least [X%] within [N months].
2. Confirm that [secondary metric] improves or does not deteriorate after deployment.
3. Track actual costs vs. projected costs to validate the financial model.
4. [Optional: measure employee experience / satisfaction impact]

---

## 2. Primary KPIs

Primary KPIs are the 2–3 metrics that most directly measure the value promised in the business case.

| KPI | Definition | Measurement Unit | Data Source |
|---|---|---|---|
| [KPI 1] | [Precise definition — avoid ambiguity] | [Hours / $ / % / count] | [System/tool] |
| [KPI 2] | [Definition] | [Unit] | [System/tool] |
| [KPI 3] | [Definition] | [Unit] | [System/tool] |

---

## 3. Secondary KPIs

Secondary KPIs provide context, explain drivers of primary KPI change, and track potential negative side effects.

| KPI | Definition | Why It Matters | Data Source |
|---|---|---|---|
| [KPI 1] | [Definition] | [What it indicates] | [System/tool] |
| [KPI 2] | [Definition] | [What it indicates] | [System/tool] |
| [KPI 3] | [Definition] | [What it indicates] | [System/tool] |

---

## 4. Baseline Measurements

> **Critical:** Capture all baselines BEFORE deployment begins. If baselines are missing, results are unverifiable.

### Baseline Collection Schedule

| Metric | Baseline Period | Collection Method | Responsible | Status |
|---|---|---|---|---|
| [KPI 1] | [Start Date] – [End Date] | [Method] | [Name] | [ ] Not Started |
| [KPI 2] | [Start Date] – [End Date] | [Method] | [Name] | [ ] Not Started |
| [KPI 3] | [Start Date] – [End Date] | [Method] | [Name] | [ ] Not Started |

### Baseline Values

> *Fill in once baseline collection is complete.*

| Metric | Baseline Value | Measurement Date | Data Quality |
|---|---|---|---|
| [KPI 1] | | | High / Medium / Low |
| [KPI 2] | | | |
| [KPI 3] | | | |

**Data quality rating criteria:**
- **High:** Automated system data, >3 months of history, consistent methodology
- **Medium:** Partially manual, some gaps, <3 months history
- **Low:** Self-reported survey, single data point, high uncertainty

---

## 5. Targets

| Metric | Baseline | 3-Month Target | 6-Month Target | 12-Month Target | Rationale |
|---|---|---|---|---|---|
| [KPI 1] | [Value] | [Value] | [Value] | [Value] | [Why this target?] |
| [KPI 2] | [Value] | [Value] | [Value] | [Value] | |
| Cost: Monthly OpEx | $[X] projected | — | $[X] | $[X] | Per financial model |
| Adoption rate | 0% | [X%] | [X%] | [X%] | Per rollout plan |

---

## 6. Data Collection Plan

For each metric, define exactly how it will be collected post-deployment.

### [Metric Name 1]

| Item | Detail |
|---|---|
| **Data source** | [System name, API, report, survey] |
| **Collection method** | [Automated pull / Manual export / Survey] |
| **Collection frequency** | [Daily / Weekly / Monthly] |
| **Responsible person** | [Name] |
| **Storage location** | [Dashboard / Spreadsheet / Data warehouse] |
| **Known limitations** | [Any gaps or caveats with this data] |

### [Metric Name 2]

| Item | Detail |
|---|---|
| **Data source** | |
| **Collection method** | |
| **Collection frequency** | |
| **Responsible person** | |
| **Storage location** | |
| **Known limitations** | |

*(Add sections for each metric)*

---

## 7. Reporting Cadence

| Report | Audience | Frequency | Format | Owner |
|---|---|---|---|---|
| Operational dashboard | Project team | Weekly | Live dashboard | [Name] |
| KPI summary report | Stakeholders | Monthly | Slide deck / email | [Name] |
| Quarterly business review | Leadership | Quarterly | Presentation | [Name] |
| Annual ROI assessment | Executive sponsor | Annually | Full report | [Name] |

### Escalation Criteria

Escalate to executive sponsor if:
- Any primary KPI is >20% below target for two consecutive reporting periods
- Monthly costs exceed budget by >15%
- Adoption rate is below [X%] at Month 3

---

## 8. Attribution Methodology

> *How will you isolate the impact of the GenAI project from other changes happening simultaneously?*

### Method Selected

- [ ] **A/B Testing** — Randomly assign some users/customers to treatment (with AI) and control (without AI). Compare outcomes.
- [ ] **Staggered Rollout** — Deploy to one team/region first, compare to others before their rollout begins.
- [ ] **Time-Series Comparison** — Compare metric performance before and after, adjusting for known confounds.
- [ ] **Management Estimate** — Where controlled comparison isn't possible, document assumptions for directional estimate.

### Known Confounds

List other changes happening during the measurement period that could affect results:

| Confound | Expected Impact | How to Handle |
|---|---|---|
| [e.g., Headcount change] | [+/- effect on metric] | [Control method] |
| [e.g., Seasonal pattern] | [Effect] | [Normalize for seasonality] |
| [e.g., Product launch] | [Effect] | [Exclude those periods] |

---

## 9. ROI Tracking

Track financial performance against the business case model monthly.

| Period | Projected Cost | Actual Cost | Projected Benefit | Actual Benefit | Variance |
|---|---|---|---|---|---|
| Month 1 | $[X] | | $[X] | | |
| Month 2 | $[X] | | $[X] | | |
| Month 3 | $[X] | | $[X] | | |
| Month 6 | $[X] | | $[X] | | |
| Month 12 | $[X] | | $[X] | | |
| Month 24 | $[X] | | $[X] | | |

**Variance trigger:** If actual ROI is >25% below projected for two consecutive periods, initiate a formal review.

---

## 10. Post-Launch Reviews

### 30-Day Check-In
- Is adoption on track?
- Are there technical issues affecting benefit realization?
- Any unexpected costs?
- Action items:

### 90-Day Milestone Review
- First quantitative comparison against baseline
- Adoption rate vs. target
- Initial cost validation
- Recommendation: Continue / Modify / Escalate

### 6-Month Business Case Validation
- Full KPI comparison to baseline
- Financial model update with actual data
- ROI reforecast
- Recommendation to proceed, scale, or pivot

---

## Appendix: Survey Templates

For metrics that require employee surveys, use these as a starting point.

### Time Savings Survey (pre- and post-deployment)

> *Administered via your HR/engagement tool or Google Forms. Compare pre vs. post results.*

1. "On average, how many hours per week do you spend [searching for information / completing [task]]?" (Numeric input)
2. "How satisfied are you with the tools available to help you [complete this task]?" (1–5 scale)
3. "In the last week, how many times did you need to ask a colleague for information you think should have been easily findable?" (Numeric input)

### AI Tool Experience Survey (post-deployment only)

1. "How often do you use [AI tool name]?" (Daily / Several times a week / Weekly / Rarely / Never)
2. "When you use [AI tool], how accurate are the results?" (Almost always / Usually / Sometimes / Rarely)
3. "Using [AI tool] has made my work [significantly easier / somewhat easier / no change / somewhat harder / significantly harder]"
4. "What's the most valuable thing [AI tool] helps you with?" (Open text)
5. "What should be improved?" (Open text)
