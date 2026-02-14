# Use Case: Chatbot & Customer Support

## Overview

AI-powered customer support is one of the most mature and well-benchmarked GenAI use cases. Organizations deploy LLM-powered chatbots and agent-assist tools to handle customer queries, reduce ticket volumes, and improve resolution quality.

**Typical ROI Range: 150–400%**
**Typical Payback Period: 12–20 months**

---

## What GenAI Enables

| Capability | Description |
|---|---|
| Automated ticket deflection | Resolving common queries without human intervention |
| Agent-assist | Suggesting responses, summarizing history, pulling relevant knowledge |
| Escalation routing | Intelligently routing complex issues to the right team |
| Sentiment detection | Flagging frustrated customers for priority handling |
| Multilingual support | Serving customers in their preferred language |
| After-hours coverage | 24/7 support without overnight staffing |

---

## Key Metrics to Track

### Before Deployment (Baseline)
- Average handle time (AHT) per ticket
- First contact resolution (FCR) rate
- Tickets per agent per day
- Escalation rate
- Customer Satisfaction Score (CSAT)
- Cost per ticket
- Agent utilization rate

### After Deployment (Outcome)
- Deflection rate (% of tickets fully resolved by AI)
- Containment rate (% that don't reach a human)
- Change in AHT for escalated tickets
- FCR rate change
- CSAT change
- Cost per ticket change
- Agent capacity freed

---

## Cost Drivers

| Cost Item | Typical Range | Notes |
|---|---|---|
| Development | $80K–$300K | Higher for custom integrations |
| CRM/helpdesk integration | $20K–$80K | Zendesk, Salesforce, ServiceNow |
| Knowledge base preparation | $10K–$50K | Chunking, embedding, testing |
| Monthly API costs | $200–$5,000/mo | Scales with ticket volume |
| Monthly infrastructure | $500–$3,000/mo | Vector DB, hosting, monitoring |
| Ongoing maintenance | $2,000–$8,000/mo | Prompt updates, KB refresh |

---

## Benefit Drivers

### 1. Labor Savings (Primary Driver)
The biggest benefit is reducing the number of agent-hours required per ticket.

```
Annual Saving = (Deflection Rate × Monthly Ticket Volume × AHT × Agent Cost/hr × 12)
              + (AHT Reduction for Assisted Tickets × Non-Deflected Tickets × Agent Cost/hr × 12)
```

### 2. Headcount Avoidance
As your business grows, AI allows you to handle more volume without proportional headcount growth.

```
Headcount Avoidance = Projected New Hires Without AI - Actual New Hires With AI
                    × Annual Fully-Loaded Agent Cost
```

### 3. CSAT and Retention Improvement
Faster, 24/7 support reduces churn.

```
Retention Benefit = Customers Retained Due to Better Support
                  × Average Customer Lifetime Value
```

---

## Worked Example

### Organization Profile
- B2C SaaS company, 50,000 active customers
- 8,000 support tickets/month
- 25 full-time support agents
- Average handle time: 15 minutes
- Agent fully-loaded cost: $65,000/year ($35/hr)
- Average CSAT: 3.8/5

### Investment
- Development + integration: $180,000
- Monthly operational (API + infra + maintenance): $6,500/month

### Expected Outcomes (Year 1)
- 40% deflection rate (3,200 tickets/month handled fully by AI)
- 20% AHT reduction for remaining tickets
- CSAT improvement to 4.2/5

### ROI Calculation

**Labor Savings — Deflection:**
```
3,200 deflected tickets/month × 0.25 hr × $35/hr × 12 months = $336,000/year
```

**Labor Savings — AHT Reduction:**
```
4,800 assisted tickets/month × (0.25 hr × 20%) × $35/hr × 12 = $100,800/year
```

**Total Annual Benefit (Year 1):** $436,800
**Total Annual Benefit (Year 2, 55% deflection):** ~$560,000

**Year 1 Total Cost:** $180,000 + ($6,500 × 12) = $258,000
**Year 1 Net Benefit:** $178,800
**Year 1 ROI:** 69%

**Year 2 Total Cost:** $78,000 (operational only)
**Year 2 Net Benefit:** $482,000
**3-Year ROI: 286%**

**Break-even: Month 11**

---

## Tips for Measurement

1. **Tag every deflected ticket** in your helpdesk. Create an "AI resolved" status that agents confirm when AI handles a ticket without human involvement.

2. **Track containment separately from deflection.** Deflection = AI resolves the issue. Containment = customer doesn't reach a human (may have abandoned — not always a success).

3. **Survey customers after AI interactions.** Low CSAT from AI interactions is a warning sign to address before scaling.

4. **Monitor for "shadow escalation"** — customers who get an AI response and then email/call anyway. This inflates apparent deflection while masking unresolved issues.

5. **Use A/B testing for CSAT impact.** Run a subset of customers without AI to establish a clean counterfactual.

---

## Common Pitfalls

| Pitfall | Impact | Prevention |
|---|---|---|
| Poor knowledge base quality | High hallucination rate, low CSAT | Invest in KB preparation before launch |
| Over-automating complex queries | Customer frustration, churn | Define clear escalation triggers |
| Ignoring multilingual needs | Excluding non-English speakers | Plan language coverage upfront |
| Forgetting change management | Agent resistance, poor adoption | Train agents on AI-assist features |
| No human override | Liability risk | Always provide easy escalation path |

---

## Related Resources

- [ROI Model](../framework/02-roi-model.md)
- [Cost Model](../framework/03-cost-model.md)
- [Interactive Calculator](../../calculator/index.html) — Select "Chatbot & Customer Support" template
