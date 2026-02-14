# Use Case: Internal Knowledge Base & Enterprise Search

## Overview

Enterprise knowledge is typically scattered across Confluence, SharePoint, Google Drive, Notion, Slack, email, and dozens of other systems. GenAI-powered search and knowledge management solutions (commonly built on Retrieval-Augmented Generation / RAG) enable employees to find accurate answers instantly — instead of spending hours searching, asking colleagues, or reinventing existing work.

**Typical ROI Range: 150–400%**
**Typical Payback Period: 12–24 months**

---

## What GenAI Enables

| Capability | Description |
|---|---|
| Semantic search | Finding content by meaning, not just keywords |
| Conversational Q&A | Ask questions, get answers with cited sources |
| Expert knowledge capture | Preserving institutional knowledge as employees leave |
| Onboarding acceleration | New hires getting answers instantly |
| Policy and procedure lookup | Employees self-serving compliance questions |
| Meeting and decision search | Finding past decisions, rationale, and context |
| Cross-system search | Single search interface across all knowledge systems |
| Knowledge gap identification | Surfacing areas where documentation is missing |

---

## Key Metrics to Track

### Before Deployment (Baseline)
- Time employees spend searching for information per day (survey)
- Number of "knowledge requests" sent to colleagues or experts per week
- Time to onboard new employees to productivity
- Frequency of reinvented work (duplicate efforts)
- Help desk tickets related to internal information requests
- Employee satisfaction with knowledge access (survey)

### After Deployment (Outcome)
- Change in time spent searching (survey)
- Knowledge request volume change
- Onboarding time to productivity
- Duplicate effort reduction (survey)
- Help desk tickets related to knowledge requests
- Employee satisfaction with knowledge access

---

## Cost Drivers

| Cost Item | Typical Range | Notes |
|---|---|---|
| Development | $60K–$250K | RAG pipeline, chat interface, access controls |
| Data ingestion and indexing | $20K–$80K | Connecting all source systems, parsing, embedding |
| Access control integration | $15K–$40K | Ensuring users only see content they're authorized for |
| Monthly API costs | $200–$3,000/mo | Embedding + generation, scales with query volume |
| Monthly vector DB | $100–$2,000/mo | Pinecone, Weaviate, Qdrant, or pgvector |
| Content maintenance | $1,000–$5,000/mo | Keeping knowledge base current and accurate |

---

## Benefit Drivers

### 1. Employee Time Savings (Primary Driver)
McKinsey research found that employees spend 1.8 hours per day on average searching for and gathering information. Even modest reductions have significant value.

```
Annual Saving =
  (Hours Saved per Employee per Week) × (Number of Employees) × (Fully-Loaded Hourly Rate)
  × (Weeks per Year) × (Productivity Capture Rate)
```

### 2. Onboarding Acceleration
New hires reach productivity weeks earlier when they can get instant answers to their questions.

```
Onboarding Value = (Weeks Saved) × (New Hires per Year) × (Fully-Loaded Weekly Cost)
```

### 3. Expert Time Preservation
Senior employees spend significant time answering repetitive questions. AI handles these, freeing expert time for higher-value work.

```
Expert Time Value =
  (Hours per Week Senior Experts Answer Repetitive Questions)
  × (Number of Experts) × (Expert Hourly Rate) × (Weeks per Year)
  × (% Deflected to AI)
```

### 4. Knowledge Retention
When employees leave, institutional knowledge often walks out with them. AI-captured knowledge reduces this risk.

---

## Worked Example

### Organization Profile
- 500-person technology company
- Knowledge spread across Confluence (2,000 pages), Google Drive (50,000 files), Notion, Slack
- Average employee: $90,000 salary, $120,000 fully-loaded ($65/hr)
- Estimated 1.5 hrs/day per employee searching for information
- 60 new hires per year, 12-week average ramp to productivity
- 20 senior experts spending 5 hrs/week answering repetitive questions

### Investment
- Development + integration: $180,000
- Monthly API + infra: $3,000/month
- Monthly maintenance: $2,000/month

**Total Year 1 Cost:** $180,000 + ($5,000 × 12) = $240,000

### Expected Outcomes
- Search time reduction: 40% (1.5 hrs → 0.9 hrs/day)
- Onboarding acceleration: 3 weeks per new hire
- Expert question deflection: 50%
- Employee adoption: 70% in Year 1
- Productivity capture rate: 55%

### ROI Calculation

**Employee Time Saving:**
```
0.6 hrs/day × 500 employees × 70% adoption × 250 working days × $65/hr × 55% capture
= 0.6 × 350 × 250 × $65 × 0.55
= $1,876,125/year
```

**Onboarding Acceleration:**
```
60 new hires × 3 weeks × $2,308/week ($120K/52) = $415,385/year
```

**Expert Time Value:**
```
20 experts × 5 hrs/week × 50 weeks × $100/hr × 50% deflected = $250,000/year
```

**Total Annual Benefit:** $2,541,510
**Year 1 Total Cost:** $240,000
**Year 1 ROI:** 958%

> Note: These numbers assume a reasonably large organization (500 people) where even small per-person savings aggregate substantially. For smaller organizations, scale the employee count proportionally.

**Break-even: Month 2**

---

## Architecture Overview: RAG-Based Knowledge System

```
User Query
    ↓
Query Embedding (text → vector)
    ↓
Vector Similarity Search
    ↓
Retrieve Top-K Relevant Chunks
    ↓
LLM Prompt Assembly (query + chunks + system instructions)
    ↓
LLM Generation (answer + citations)
    ↓
User Response with Source Links
```

**Key design decisions:**
- **Chunking strategy:** How you split documents dramatically affects retrieval quality
- **Embedding model:** Determines semantic search quality
- **Retrieval strategy:** Dense only, sparse only, or hybrid (usually best)
- **Access control:** Must be enforced at retrieval layer, not just display layer
- **Citation design:** Always show sources so users can verify

---

## Tips for Measurement

1. **Run an "information search" time survey** before deployment and 3 months after. Ask employees to estimate hours per week spent searching for information. Even self-reported data captures the trend.

2. **Track query volume by category.** Categorize questions (HR/policy, technical, product, etc.) to identify the highest-value knowledge domains and gaps.

3. **Monitor answer quality through thumbs up/down feedback.** Require a simple feedback mechanism. Target >80% positive feedback after the first 60 days.

4. **Track the "I had to ask a colleague" rate.** Add a question to your internal survey: "In the last week, how many times did you ask a colleague a question you think AI should have been able to answer?" This measures unsatisfied demand.

5. **Measure content freshness.** Stale knowledge is dangerous. Track the % of retrieved content that is >12 months old and flag for review.

---

## Common Pitfalls

| Pitfall | Impact | Prevention |
|---|---|---|
| Indexing everything including outdated docs | Hallucinations from old info | Set content freshness thresholds and date filters |
| Broken access controls | Sensitive data exposed | Security review before launch, test with unprivileged accounts |
| No content governance | Knowledge base degrades | Assign content owners and set review schedules |
| Hallucination without citations | Users trust wrong answers | Require citations and confidence scores in every answer |
| Low initial content quality | Poor early experience, low adoption | Curate top 20% of most-used content before launch |

---

## Related Resources

- [ROI Model](../framework/02-roi-model.md)
- [Cost Model](../framework/03-cost-model.md)
- [Decision Guide](../framework/06-decision-guide.md) — Build vs. buy considerations
- [Interactive Calculator](../../calculator/index.html) — Select "Internal Knowledge Base" template
