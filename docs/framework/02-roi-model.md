# The GenAI ROI Model

## Overview

The GenAI ROI Model is built on four pillars that collectively capture the full value of a Generative AI investment. Every benefit from a GenAI project maps to at least one of these pillars.

```
┌─────────────────────────────────────────────────────────┐
│                   GenAI ROI Model                        │
├──────────────┬──────────────┬─────────────┬─────────────┤
│    Cost      │   Revenue    │ Productivity│    Risk     │
│  Reduction   │   Growth     │   Gains     │ Mitigation  │
├──────────────┼──────────────┼─────────────┼─────────────┤
│ - Labor      │ - New        │ - Speed     │ - Error     │
│   savings    │   products   │   to market │   reduction │
│ - Tool       │ - Upsell     │ - Employee  │ - Compliance│
│   consolidat.│   opportunit.│   output    │ - Quality   │
│ - Infra      │ - Market     │ - Focus on  │   assurance │
│   reduction  │   expansion  │   high-value│ - Audit     │
│              │              │   work      │   readiness │
└──────────────┴──────────────┴─────────────┴─────────────┘
```

---

## The Core Formula

```
ROI (%) = ((Total Benefits - Total Costs) / Total Costs) × 100
```

### Expanded Definition

**Total Benefits** = Cost Savings + Revenue Gains + Productivity Value + Risk Reduction Value

**Total Costs** = Development + Infrastructure + API/Model Costs + Integration + Maintenance + Training + Governance

A positive ROI means benefits exceed costs. The higher the percentage, the better the return relative to what you spent.

---

## Pillar 1: Cost Reduction

Cost reduction is the most straightforward pillar to measure. It answers: **"What are we spending today that we'll spend less on after deploying GenAI?"**

### Sub-categories

| Sub-category | Examples |
|---|---|
| Labor savings | Reduced headcount growth, reallocation of FTEs from manual to strategic work |
| Tool consolidation | Replacing multiple point solutions with a single AI-powered platform |
| Infrastructure reduction | Lower server/storage costs from automated processing |
| Process elimination | Removing manual steps that GenAI handles end-to-end |

### How to Quantify

```
Annual Labor Saving = (Hours Saved per Task × Tasks per Year × Fully-Loaded Hourly Rate)
                      × Adoption Rate
```

**Example:** A document summarization tool saves a legal team 2 hours per contract review. The team reviews 500 contracts per year. An analyst's fully-loaded cost is $75/hr. At 80% adoption:

```
2 hrs × 500 reviews × $75/hr × 0.80 = $60,000/year
```

---

## Pillar 2: Revenue Growth

Revenue growth is harder to attribute directly to GenAI but is often the largest pillar for commercial applications. It answers: **"What new revenue does GenAI enable?"**

### Sub-categories

| Sub-category | Examples |
|---|---|
| New product/feature revenue | Charging for AI-powered features, new subscription tiers |
| Conversion rate improvement | Better personalization leading to higher close rates |
| Upsell and cross-sell | AI recommendations increasing average order value |
| Market expansion | Serving new segments previously too costly to reach |
| Speed to market | Shipping features faster than competitors |

### How to Quantify

Revenue attribution requires careful methodology. Use one of:

1. **A/B testing:** Compare conversion rates with and without AI features
2. **Incremental cohort analysis:** Track revenue for AI-assisted vs. non-assisted customers
3. **Feature adoption uplift:** Measure revenue uplift for customers using AI features vs. not

```
Revenue Gain = (Incremental Conversion Rate × Addressable Opportunities × Average Deal Value)
             + (Upsell Rate Increase × Existing Customer Base × Average Upsell Value)
```

---

## Pillar 3: Productivity Gains

Productivity gains capture the value of people doing more, better, and faster — without direct headcount reduction. It answers: **"What can our team accomplish now that they couldn't before?"**

### Sub-categories

| Sub-category | Examples |
|---|---|
| Output increase | More tickets handled, more code shipped, more content published |
| Quality improvement | Fewer errors, better first-draft quality, higher accuracy |
| Speed increase | Faster time-to-first-draft, faster code review, shorter research cycles |
| Focus shift | High-cost employees focusing on high-value work |

### How to Quantify

Productivity value is typically expressed as the value of additional output or the value of reallocated time:

```
Productivity Value = (Time Saved per Person per Week × Weeks per Year
                     × Fully-Loaded Weekly Cost × Number of Users)
                   × Productivity Capture Rate
```

> **Productivity Capture Rate** (typically 50–70%) reflects that not all saved time converts to productive output — some is absorbed by meetings, context-switching, and non-billable activities.

---

## Pillar 4: Risk Mitigation

Risk mitigation captures defensive value — costs avoided by reducing errors, improving compliance, and ensuring quality. It answers: **"What bad outcomes are we preventing?"**

### Sub-categories

| Sub-category | Examples |
|---|---|
| Error reduction | Fewer customer service mistakes, fewer code bugs, fewer compliance violations |
| Regulatory compliance | Automated audit trails, policy checking, regulatory monitoring |
| Quality assurance | Consistent output quality, reduced rework |
| Reputational protection | Fewer public-facing errors or inappropriate responses |

### How to Quantify

Risk mitigation is calculated using expected value:

```
Risk Mitigation Value = Probability of Incident × Cost of Incident × Reduction in Probability
```

**Example:** A financial services firm faces an average of 3 compliance violations per year at $200,000 each. GenAI compliance checking reduces violation probability by 60%:

```
3 violations × $200,000 × 60% = $360,000/year in avoided costs
```

---

## Multi-Year Modeling

GenAI investments typically have three distinct phases:

### Year 1: Investment and Ramp
- High upfront costs (development, integration, training)
- Low initial benefits (adoption curve, calibration period)
- Typically negative or breakeven ROI
- **Goal:** Validate the model, hit adoption targets

### Year 2: Acceleration
- Costs normalize to operational steady-state
- Benefits ramp as adoption grows and workflows mature
- ROI turns positive for most use cases
- **Goal:** Scale usage, optimize performance

### Year 3+: Compounding Returns
- Costs are mostly fixed operational
- Benefits compound as AI improves and usage deepens
- ROI accelerates
- **Goal:** Expand to adjacent use cases, reinvest returns

---

## Scenario Modeling

Always present three scenarios:

| Scenario | Description | Typical Multipliers |
|---|---|---|
| **Pessimistic** | Low adoption, high costs, conservative benefits | Benefits × 0.5, Costs × 1.3 |
| **Realistic** | Expected adoption, slight cost overrun, moderate benefits | Benefits × 0.8, Costs × 1.1 |
| **Optimistic** | High adoption, costs on budget, full benefits realized | Benefits × 1.0, Costs × 1.0 |

The realistic scenario is your headline number. The pessimistic scenario is your downside protection case. The optimistic scenario shows upside potential.

---

## Common ROI Mistakes

| Mistake | Impact | Fix |
|---|---|---|
| Counting 100% of saved time as value | Overestimates ROI by 2–3× | Apply productivity capture rate (50–70%) |
| Forgetting ongoing maintenance costs | Underestimates total cost | Add 15–20% of development cost annually |
| Assuming Day 1 = Full adoption | Overestimates Year 1 ROI | Model adoption ramp (30% → 70% → 90% over 3 years) |
| Ignoring change management costs | Understates cost by 20–30% | Add training + process redesign costs |
| Double-counting across pillars | Inflates benefits | Map each benefit to exactly one pillar |

---

## Next Steps

- [Cost Model →](03-cost-model.md) — How to estimate every cost category accurately
- [Benefit Model →](04-benefit-model.md) — How to quantify and measure each benefit type
- [Break-Even Analysis →](05-break-even-analysis.md) — How to calculate payback period
