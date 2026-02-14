# Decision Guide: Is GenAI Right for Your Use Case?

## Overview

Not every problem is best solved by Generative AI. Before investing in a GenAI solution, use this guide to stress-test your use case and ensure you're choosing the right tool for the job.

This guide helps you answer four questions:
1. **Should you use AI at all?** (vs. process improvement, traditional software, or hiring)
2. **Should you use GenAI specifically?** (vs. classical ML, rules-based systems, or search)
3. **Should you build or buy?**
4. **Is your organization ready?**

---

## Question 1: Should You Use AI at All?

Before jumping to AI, verify that the problem isn't better solved by simpler means.

### The "Simpler Solution" Checklist

Run through this checklist. If any item is true, consider the alternative first:

| Check | If True, Consider |
|---|---|
| The process is broken due to unclear ownership or incentives | Process redesign, not AI |
| The task takes hours because of tool friction, not cognitive work | Better tooling or automation |
| The data doesn't exist or is poor quality | Data strategy first |
| The problem affects <5 people and <10 hours/week | Not worth the investment |
| A simple rule or template would solve 80% of cases | Rules-based automation |
| The task requires physical presence or sensory judgment | Wrong modality for AI |

**If none of these apply** and the problem involves significant knowledge work at scale, continue to Question 2.

---

## Question 2: Should You Use GenAI Specifically?

GenAI (large language models, diffusion models, etc.) excels at specific tasks. Make sure your use case matches.

### GenAI Strengths vs. Alternatives

| Task Type | Best Approach |
|---|---|
| Open-ended text generation, summarization, Q&A | **GenAI** (LLM) |
| Image/video/audio generation | **GenAI** (diffusion/multimodal) |
| Classification with labeled training data | Classical ML (faster, cheaper, more accurate) |
| Structured data prediction | Classical ML or statistical modeling |
| Exact pattern matching (emails, invoices) | Rules-based or regex automation |
| Database queries and reporting | SQL + BI tools |
| Semantic search over documents | GenAI (RAG) or hybrid search |
| Real-time decision-making (<50ms latency) | Classical ML or rules |

### GenAI Fit Score

Rate your use case on these dimensions (1 = low, 5 = high):

| Dimension | Score | Why It Matters |
|---|---|---|
| Requires natural language understanding | /5 | Core GenAI strength |
| High variability in inputs/outputs | /5 | GenAI handles variance well |
| Benefits from context and reasoning | /5 | Differentiating capability |
| Large volume of cases (>1K/month) | /5 | Justifies infrastructure cost |
| Humans currently do this task | /5 | Confirms cognitive load |
| Acceptable latency >2 seconds | /5 | GenAI is slower than rules |

**Score interpretation:**
- 20–30: Strong GenAI fit — proceed
- 12–19: Moderate fit — validate with a small pilot
- <12: Weak fit — explore alternatives

---

## Question 3: Should You Build or Buy?

Once you've confirmed GenAI is the right approach, decide on the delivery model.

### The Build vs. Buy Framework

| Factor | Favor Build | Favor Buy |
|---|---|---|
| Proprietary data advantage | Yes — custom model benefits | No — generic data, off-shelf fine |
| Deep workflow integration | Yes — needs custom embedding | No — standalone tool works |
| Vendor lock-in risk | High — critical business function | Low — easy to switch |
| Team AI capability | High — can build and maintain | Low — better to outsource |
| Speed to value required | No — can take time | Yes — need results in weeks |
| Unique/novel use case | Yes — no existing solutions | No — mature vendor landscape |
| Budget | >$200K available | <$200K or preference for OpEx |

### Common Delivery Models

| Model | Description | Best For |
|---|---|---|
| **Buy SaaS** | Subscribe to an AI product (Jasper, Intercom AI, GitHub Copilot) | Commodity use cases, fast start |
| **Buy + Configure** | Deploy a platform and configure for your workflows (Microsoft Copilot, Salesforce Einstein) | Enterprise with existing vendor relationships |
| **Build on API** | Use OpenAI/Anthropic/Gemini APIs to build custom solution | Unique workflows, proprietary data |
| **Fine-tune/Custom** | Fine-tune an open-source model on your data | Highest control, high volume, regulated industries |
| **On-premises** | Run models locally (LLaMA, Mistral) | Strict data sovereignty requirements |

---

## Question 4: Is Your Organization Ready?

The best technology fails without organizational readiness. Assess your readiness honestly.

### Readiness Assessment

Score each dimension 1–5:

#### Data Readiness
| Item | Score |
|---|---|
| Relevant data exists and is accessible | /5 |
| Data quality is sufficient (accurate, complete, current) | /5 |
| Data governance and privacy requirements are understood | /5 |
| Data pipelines can feed the AI system | /5 |
| **Data Readiness Score** | /20 |

#### People Readiness
| Item | Score |
|---|---|
| Executive sponsorship is confirmed | /5 |
| A product owner / AI champion is identified | /5 |
| End users are motivated to adopt AI tools | /5 |
| Legal/compliance team is engaged | /5 |
| **People Readiness Score** | /20 |

#### Technical Readiness
| Item | Score |
|---|---|
| Engineering team has AI/ML experience | /5 |
| Cloud infrastructure is in place | /5 |
| Security and access controls can be extended | /5 |
| Monitoring and observability capabilities exist | /5 |
| **Technical Readiness Score** | /20 |

### Interpreting Your Readiness Score

| Total Score (60 max) | Recommendation |
|---|---|
| 45–60 | Strong readiness — proceed with full deployment |
| 30–44 | Moderate readiness — start with a focused pilot |
| 15–29 | Low readiness — address gaps before investing |
| <15 | Not ready — foundational work needed first |

---

## The Go/No-Go Decision Matrix

Combine your GenAI Fit Score and Readiness Score:

```
                    Low Readiness    High Readiness
                    (< 30)           (≥ 30)
                  ┌────────────────┬────────────────┐
  High GenAI Fit  │   Build         │   Go — Full    │
  (≥ 20)          │   Readiness     │   Deployment   │
                  │   First         │                │
                  ├────────────────┼────────────────┤
  Low GenAI Fit   │   Stop —        │   Reconsider   │
  (< 20)          │   Wrong         │   Approach     │
                  │   Approach      │                │
                  └────────────────┴────────────────┘
```

---

## Red Flags: When to Walk Away

Stop the project (or pause until resolved) if any of these apply:

- **The ROI is only positive in the optimistic scenario.** A project must pencil out in the realistic case.
- **There is no measurable baseline.** You can't prove value without measurement.
- **Legal/compliance approval is blocked.** Don't build something that can't launch.
- **The champion has left the organization.** AI projects without internal advocates fail.
- **The underlying data doesn't exist.** No data = no AI value.
- **The budget doesn't cover the full 18-month runway.** Underfunded AI projects die slowly and expensively.

---

## Making the Final Decision

If you've worked through all four questions and the answers are positive, you have a strong foundation for a GenAI investment. Use the following summary template:

```
Use Case: [Name]
Business Problem: [1-sentence description]
GenAI Fit Score: [X/30]
Readiness Score: [X/60]
Estimated Break-Even: [Month X]
3-Year ROI (Realistic): [X%]
Biggest Risk: [Top risk and mitigation]
Recommendation: [Go / Pilot / Wait / Stop]
```

---

## Next Steps

- [Use Case Library →](../use-cases/) — See how your use case compares to benchmarks
- [Business Case Template →](../templates/business-case-template.md) — Turn your analysis into a stakeholder presentation
- [Interactive Calculator →](../../calculator/index.html) — Model your final numbers
