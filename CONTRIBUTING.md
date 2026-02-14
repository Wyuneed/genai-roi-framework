# Contributing to the GenAI ROI Framework

Thank you for your interest in contributing! This framework is community-driven and improves with every real-world perspective and use case added.

---

## Ways to Contribute

| Contribution Type | Examples |
|---|---|
| New use case playbooks | AI agents, image generation, RAG systems, voice AI, code review |
| Industry-specific ROI benchmarks | Healthcare, financial services, retail, manufacturing |
| Calculator improvements | New templates, better visualizations, export features |
| Framework refinements | Better formulas, new cost/benefit categories, corrections |
| Real-world case studies | Anonymized examples with actual numbers |
| Translations | Framework documentation in other languages |
| Bug fixes | Calculation errors, broken links, typos |

---

## Getting Started

### 1. Fork the Repository

Fork the repo and create a feature branch:

```bash
git clone https://github.com/Wyuneed/genai-roi-framework.git
cd genai-roi-framework
git checkout -b feature/your-contribution-name
```

### 2. Make Your Changes

Follow the guidelines below for each contribution type.

### 3. Submit a Pull Request

Push your branch and open a pull request against `main`. Fill out the PR template completely.

---

## Contribution Guidelines

### Adding a New Use Case Playbook

New use case playbooks go in `docs/use-cases/`. Use the following structure:

```markdown
# Use Case: [Name]

## Overview
[1-2 sentences + typical ROI range + payback period]

## What GenAI Enables
[Table of capabilities]

## Key Metrics to Track
[Before and after metrics]

## Cost Drivers
[Table with typical ranges]

## Benefit Drivers
[Each benefit with calculation formula]

## Worked Example
[Realistic organization profile + full ROI calculation showing your work]

## Tips for Measurement
[5+ practical tips for tracking this use case]

## Common Pitfalls
[Table format]

## Related Resources
[Links to framework docs and calculator]
```

**Quality bar:** The worked example must show complete calculations with realistic numbers. Cite your source for any benchmarks or industry statistics.

### Improving the Calculator

The calculator lives in `calculator/index.html`. It is a self-contained HTML/CSS/JS file with no external dependencies (by design — works offline).

When modifying the calculator:
- Maintain the zero-dependency requirement (no npm, no build step)
- Test in Chrome, Firefox, and Safari
- Ensure the calculator works on mobile (responsive design)
- If adding a new use case template, add it to both the template selector and the `TEMPLATES` object in the JavaScript
- Document any new formula in a comment

### Adding Industry Benchmarks

If you're adding industry-specific ROI data:
- Cite your source (include link or publication reference)
- Specify the date and context of the data
- Note the geographic/market scope
- Distinguish between reported and modeled figures

### Submitting Case Studies

Case studies are especially valuable. Requirements:
- All identifying information must be anonymized (no company names, industry is fine)
- Include the actual numbers, not just directional statements
- Describe the methodology used to measure results
- Get confirmation from your organization that sharing is permitted

---

## Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/). By contributing, you agree to uphold these standards.

In short:
- Be respectful and constructive
- Welcome different perspectives
- Accept feedback graciously
- Focus on what's best for the community

---

## Pull Request Checklist

Before submitting your PR, confirm:

- [ ] I have read the contribution guidelines above
- [ ] My changes follow the structure/format of existing content
- [ ] Calculations are correct and I've shown my work
- [ ] Any benchmarks or statistics are cited with source and date
- [ ] Links work (test all markdown links locally)
- [ ] I have not introduced any external dependencies to the calculator
- [ ] My contribution adds genuine new value (not duplicating existing content)

---

## What Makes a Good Contribution

**Good contributions:**
- Specific, actionable, and well-sourced
- Include real numbers, not just frameworks
- Correct errors with evidence and citations
- Solve a problem that others will face

**Contributions we'll ask you to revise:**
- Overly promotional of specific vendors or products
- Generic advice without supporting data
- ROI estimates that aren't grounded in realistic assumptions

**Contributions we'll decline:**
- Content that could be used to misrepresent AI ROI for deceptive purposes
- Submissions that violate the license or contain proprietary content without permission

---

## Questions and Discussion

- **Bug reports:** Open a GitHub Issue
- **Feature requests:** Open a GitHub Issue with the `enhancement` label
- **General discussion:** Use GitHub Discussions
- **Sensitive issues:** Email the maintainers directly (see repository contact info)

---

## Recognition

All contributors are recognized in the project's commit history and in release notes. Significant contributions (new use cases, major framework improvements) will be called out in the README.

Thank you for helping make GenAI ROI analysis more accessible to everyone.
