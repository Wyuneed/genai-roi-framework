# Break-Even Analysis

## Overview

Break-even analysis answers the most common executive question about any technology investment:

> **"When do we get our money back?"**

For GenAI projects, break-even typically occurs between Month 6 and Month 24, depending on upfront costs, adoption speed, and benefit magnitude.

---

## Core Concept: Cumulative Cash Flow

Break-even is the point where cumulative benefits equal cumulative costs. The payback period is the number of months (or years) to reach that point.

```
Break-Even Month = First month where:
  Cumulative Benefits ≥ Cumulative Costs
```

---

## The Break-Even Calculation

### Step 1: Map All Costs by Month

| Cost Type | When It Occurs |
|---|---|
| Development | Months 1–N of build phase |
| Integration | Months 1–N of build phase |
| Training | Month of launch + ongoing |
| Governance/Legal | Pre-launch + ongoing |
| Infrastructure | Monthly, starting at launch |
| API/Model | Monthly, scales with usage |
| Maintenance | Monthly, starting 1–3 months post-launch |

### Step 2: Model Benefits by Month

Apply the benefit ramp curve (see [Benefit Model](04-benefit-model.md)):

```
Monthly Benefit(t) = Full Annual Benefit / 12 × Adoption Rate(t)

Where Adoption Rate(t):
  Month 1–2:   15%
  Month 3–4:   40%
  Month 5–6:   60%
  Month 7–12:  75%
  Month 13+:   90%
```

### Step 3: Calculate Cumulative Curves

```
Cumulative Cost(t) = Σ Monthly Cost (months 1 to t)
Cumulative Benefit(t) = Σ Monthly Benefit (months 1 to t)
Net Position(t) = Cumulative Benefit(t) - Cumulative Cost(t)
```

Break-even = first `t` where `Net Position(t) ≥ 0`

---

## Worked Example: Customer Support Chatbot

### Assumptions

| Item | Value |
|---|---|
| Development cost | $120,000 (over 3 months) |
| Integration cost | $40,000 (month 3–4) |
| Training cost | $15,000 (month 4) |
| Monthly infrastructure | $1,200/month |
| Monthly API cost | $800/month |
| Monthly maintenance | $2,500/month (starting month 5) |
| Annual labor saving | $180,000/year ($15,000/month at full adoption) |
| Annual process saving | $60,000/year ($5,000/month at full adoption) |

### Monthly Cash Flow Model

| Month | Monthly Cost | Monthly Benefit | Cumulative Cost | Cumulative Benefit | Net Position |
|---|---|---|---|---|---|
| 1 | $55,000 | $0 | $55,000 | $0 | -$55,000 |
| 2 | $55,000 | $0 | $110,000 | $0 | -$110,000 |
| 3 | $50,000 | $0 | $160,000 | $0 | -$160,000 |
| 4 | $17,000 | $3,000 | $177,000 | $3,000 | -$174,000 |
| 5 | $4,500 | $8,000 | $181,500 | $11,000 | -$170,500 |
| 6 | $4,500 | $12,000 | $186,000 | $23,000 | -$163,000 |
| 7 | $4,500 | $15,000 | $190,500 | $38,000 | -$152,500 |
| 8 | $4,500 | $15,000 | $195,000 | $53,000 | -$142,000 |
| 9 | $4,500 | $15,000 | $199,500 | $68,000 | -$131,500 |
| 10 | $4,500 | $15,000 | $204,000 | $83,000 | -$121,000 |
| 11 | $4,500 | $15,000 | $208,500 | $98,000 | -$110,500 |
| 12 | $4,500 | $15,000 | $213,000 | $113,000 | -$100,000 |
| 18 | $4,500 | $18,000 | $240,000 | $203,000 | -$37,000 |
| 20 | $4,500 | $18,000 | $249,000 | $239,000 | -$10,000 |
| **21** | **$4,500** | **$18,000** | **$253,500** | **$257,000** | **+$3,500** |

**Break-even: Month 21**
**3-Year ROI: 147%**

---

## Payback Period Benchmarks by Use Case

Based on industry data and community contributions:

| Use Case | Typical Payback Period | Key Driver |
|---|---|---|
| Customer support chatbot | 12–24 months | Ticket deflection rate |
| Code generation assistant | 6–18 months | Developer adoption rate |
| Document processing | 8–18 months | Document volume |
| Content generation | 6–15 months | Content output value |
| Internal knowledge base | 12–24 months | Search query volume |
| Data analysis assistant | 9–18 months | Analyst time savings |

---

## Sensitivity Analysis

Break-even is highly sensitive to a few key variables. Always test your assumptions:

### Variables with High Impact on Break-Even

| Variable | Change | Break-Even Impact |
|---|---|---|
| Adoption rate (Year 1) | -20 percentage points | +4–8 months |
| Development cost overrun | +30% | +2–5 months |
| Benefit realization (lower than expected) | -25% | +3–6 months |
| Monthly operational costs | +20% | +1–3 months |

### Sensitivity Table (Example)

Using the chatbot example above, varying adoption rate and development cost:

| Dev Cost / Adoption | 50% Year 1 Adoption | 70% Year 1 Adoption | 90% Year 1 Adoption |
|---|---|---|---|
| $100K | Month 19 | Month 16 | Month 14 |
| $160K (base) | Month 25 | Month 21 | Month 18 |
| $200K | Month 29 | Month 25 | Month 22 |

---

## Net Present Value (NPV) for Larger Investments

For investments >$500K or multi-year programs, use NPV rather than simple payback period:

```
NPV = Σ (Net Cash Flow in Period t) / (1 + Discount Rate)^t - Initial Investment
```

**Typical discount rates:**
- Risk-free (government benchmark): 4–5%
- Corporate hurdle rate (most companies): 8–15%
- High-risk technology investment: 15–25%

A positive NPV means the investment creates value above your cost of capital. Use NPV to compare GenAI against alternative investments.

---

## Internal Rate of Return (IRR)

IRR is the discount rate at which NPV = 0. It tells you the effective annual return on your investment.

**Interpreting IRR:**
- IRR > cost of capital = good investment
- IRR > 25% = strong investment for tech projects
- IRR > 50% = exceptional (common for high-volume, low-cost GenAI applications)

---

## Presenting Break-Even to Stakeholders

### For Executives
Lead with the payback period and the 3-year return multiple:

> "This investment breaks even in Month 18 and delivers $2.40 back for every dollar spent over 3 years."

### For Finance
Show the full monthly cash flow table with NPV and IRR calculations. Include the sensitivity analysis to show you've stress-tested the assumptions.

### For Skeptics
Lead with the pessimistic scenario. Show that even with 30% higher costs and 50% of expected benefits, the project still breaks even within the acceptable window.

---

## Next Steps

- [Decision Guide →](06-decision-guide.md) — Is GenAI the right solution for your use case?
- [Use Case Library →](../use-cases/) — See break-even models for specific scenarios
- [Business Case Template →](../templates/business-case-template.md) — Package your analysis for stakeholders
- [Interactive Calculator →](../../calculator/index.html) — Get your break-even month instantly
