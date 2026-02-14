# Cost Model

## Overview

Accurate cost estimation is the foundation of a credible ROI analysis. GenAI projects have a distinct cost structure compared to traditional software — with high upfront investment, significant ongoing operational costs, and hidden costs that catch teams off-guard.

This document breaks down every cost category with estimation guidance and real-world benchmarks.

---

## Cost Categories

```
Total Cost = Development + Infrastructure + API/Model + Integration
           + Maintenance + Training + Governance
```

---

## 1. Development Costs

Development costs cover everything required to build the initial solution.

### What's Included

| Item | Description |
|---|---|
| Engineering time | Backend, frontend, ML/AI engineers, prompt engineers |
| Prompt engineering | Designing, testing, and iterating on prompts |
| Data preparation | Cleaning, formatting, chunking, embedding data |
| Evaluation framework | Building evals to measure model quality |
| Testing and QA | Unit tests, integration tests, user acceptance testing |

### Estimation Approach

```
Development Cost = Sum of (Role Hours × Blended Hourly Rate)
```

**Fully-loaded rate benchmarks (US market, 2024):**
| Role | Annual Salary | Fully-Loaded Rate |
|---|---|---|
| Senior ML/AI Engineer | $180,000–$250,000 | $115–$160/hr |
| Senior Backend Engineer | $150,000–$200,000 | $95–$130/hr |
| Product Manager | $130,000–$180,000 | $85–$115/hr |
| Prompt Engineer | $120,000–$160,000 | $75–$100/hr |
| QA Engineer | $100,000–$130,000 | $65–$85/hr |

### Typical Development Time Ranges

| Project Scope | Team Size | Duration | Total Cost Range |
|---|---|---|---|
| Small MVP (1 use case) | 2–3 people | 4–8 weeks | $40K–$120K |
| Medium deployment | 4–6 people | 8–16 weeks | $150K–$400K |
| Enterprise rollout | 8–15 people | 16–32 weeks | $500K–$2M+ |

---

## 2. Infrastructure Costs

Infrastructure covers the compute, storage, and networking required to run your solution.

### What's Included

| Item | Description |
|---|---|
| Vector database | Storing and querying embeddings (Pinecone, Weaviate, pgvector) |
| Application servers | Hosting the application layer |
| Caching layer | Redis or similar for response caching |
| Monitoring infrastructure | Logging, alerting, observability tools |
| Data storage | Object storage for documents, outputs, audit logs |

### Monthly Infrastructure Cost Ranges

| Scale | Monthly Users/Requests | Monthly Cost |
|---|---|---|
| Prototype | <1,000 req/day | $50–$300/mo |
| Small production | 1K–10K req/day | $300–$1,500/mo |
| Medium production | 10K–100K req/day | $1,500–$8,000/mo |
| Large production | 100K+ req/day | $8,000–$50,000+/mo |

---

## 3. API / Model Costs

This is the variable cost most teams focus on — but often underestimate at scale.

### Major Provider Pricing (approximate, check current rates)

| Model | Input (per 1M tokens) | Output (per 1M tokens) | Best For |
|---|---|---|---|
| GPT-4o | ~$2.50 | ~$10.00 | General purpose, reasoning |
| GPT-4o mini | ~$0.15 | ~$0.60 | High-volume, cost-sensitive |
| Claude 3.5 Sonnet | ~$3.00 | ~$15.00 | Coding, analysis, long context |
| Claude 3 Haiku | ~$0.25 | ~$1.25 | Fast, lightweight tasks |
| Gemini 1.5 Pro | ~$1.25 | ~$5.00 | Long context, multimodal |

### Estimating Token Usage

```
Monthly API Cost = (Avg Input Tokens + Avg Output Tokens) × Requests per Month
                 × Token Price / 1,000,000
```

**Token estimation rules of thumb:**
- 1 token ≈ 0.75 English words
- Short query + response: ~500–2,000 tokens
- RAG with document context: ~2,000–8,000 tokens
- Long-form document analysis: ~10,000–50,000 tokens

**Example calculation:**
- 10,000 support tickets/month
- Average 3,000 tokens per ticket (input + output)
- Using GPT-4o mini at $0.75/1M blended

```
10,000 × 3,000 × $0.75 / 1,000,000 = $22.50/month
```

> This is often surprisingly affordable at modest scale — but scales linearly with volume.

---

## 4. Integration Costs

Integration covers connecting GenAI to your existing systems.

### What's Included

| Item | Description |
|---|---|
| CRM/ticketing integration | Salesforce, Zendesk, ServiceNow connectors |
| Data pipeline integration | Connecting to data warehouses, document stores |
| Authentication/SSO | Enterprise identity integration |
| Webhook/API wiring | Connecting GenAI outputs to downstream workflows |
| Legacy system adapters | Special handling for older systems |

### Estimation

Integration costs are typically **20–40% of development costs** for standard enterprise environments. Complex legacy environments can push this to 50–60%.

---

## 5. Maintenance Costs

Ongoing costs to keep the system accurate, performant, and compliant.

### What's Included

| Item | Description | Annual Cost as % of Dev |
|---|---|---|
| Model updates | Adapting to new model versions | 5–10% |
| Prompt maintenance | Updating prompts as use cases evolve | 5–15% |
| Data refresh | Re-embedding updated knowledge bases | 3–8% |
| Bug fixes | Ongoing engineering support | 10–15% |
| Performance optimization | Latency and cost tuning | 3–5% |

**Rule of thumb:** Budget **15–25% of initial development cost** annually for maintenance.

---

## 6. Training Costs

Often underestimated, training is critical for adoption and ROI realization.

### What's Included

| Item | Description |
|---|---|
| End-user training | Teaching employees to use the AI effectively |
| Manager enablement | Coaching managers on AI-assisted workflows |
| Change management | Process redesign, communication, adoption support |
| Documentation | User guides, SOPs, FAQs |
| Ongoing reinforcement | Refresher training, new hire onboarding |

### Estimation

```
Training Cost = (Number of Users × Hours of Training × Hourly Employee Cost)
              + Materials and Platform Costs
              + Change Management Consulting (if applicable)
```

**Benchmark:** $200–$800 per employee for initial rollout training across all roles.

---

## 7. Governance Costs

Governance ensures responsible, compliant, and auditable AI usage.

### What's Included

| Item | Description |
|---|---|
| Legal review | Privacy, IP, and liability assessment |
| Security assessment | Penetration testing, data flow review |
| Compliance monitoring | Ongoing regulatory compliance checks |
| AI policy development | Usage policies, acceptable use guidelines |
| Audit logging | Infrastructure for compliance evidence |
| Ethics/bias review | Evaluating outputs for fairness and accuracy |

### Estimation

Governance costs vary significantly by industry:

| Industry | Governance Overhead |
|---|---|
| Healthcare, Finance | 15–25% of total project cost |
| Legal, Insurance | 10–20% of total project cost |
| Tech, Retail, Media | 5–10% of total project cost |

---

## Total Cost of Ownership (TCO) Model

For a 3-year TCO analysis:

```
Year 1 Cost = Development + Integration + Training + Governance
            + (Infrastructure × 12) + (API × 12) + (Maintenance × 0.5)

Year 2 Cost = (Infrastructure × 12) + (API × 12) + (Maintenance × 12)
            + (Training × 0.3)  ← refresher/new hire training

Year 3 Cost = (Infrastructure × 12) + (API × 12) + (Maintenance × 12)
            + (Training × 0.2) + (Governance × ongoing)
```

Note: API costs grow proportionally with usage volume. Model this as a separate scaling factor.

---

## Cost Optimization Strategies

| Strategy | Potential Savings | Complexity |
|---|---|---|
| Caching frequent responses | 20–40% API cost reduction | Low |
| Right-sizing models (use smaller models for simple tasks) | 30–70% API cost reduction | Medium |
| Prompt compression | 15–30% token reduction | Medium |
| Batching requests | 20–40% throughput improvement | Medium |
| Fine-tuning (for high-volume repetitive tasks) | 50–80% API cost reduction | High |

---

## Next Steps

- [Benefit Model →](04-benefit-model.md) — How to quantify and measure each benefit type
- [Break-Even Analysis →](05-break-even-analysis.md) — Combining costs and benefits into a payback timeline
- [Interactive Calculator →](../../calculator/index.html) — Plug in your numbers
