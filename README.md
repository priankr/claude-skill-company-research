# Company Research Claude Skill

---

A comprehensive Claude Skill for conducting professional company and product research. Generates structured reports ideal for competitive analysis, market research, and job interview preparation.

## Context

Traditional company research is time-consuming and inconsistent. While we can use AI to enhance this process, the results can be inconsistent. This skill was created to address the need for consistent, high-quality company research. It standardizes the process while maintaining depth and quality.

This skill can be helpful in three key scenarios:

1. **Job Search Preparation** - Research companies before interviews, understand culture and values, and prepare talking points.
2. **Competitive Analysis** - Analyze competitors' products, positioning, and market strategy
3. **Market Research** - Understanding industry players or evaluating potential customers, partners, or investment targets

### About Claude Skills

[Claude Skills](https://www.anthropic.com/news/claude-skills) extend Claude's capabilities with specialized knowledge and workflows. Skills are reusable packages that teach Claude how to perform domain-specific tasks consistently and professionally.

**Learn more:**

- [Introduction to Claude Skills](https://www.anthropic.com/news/claude-skills)
- [How to Create Custom Skills](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)
- [Claude Skills Documentation](https://docs.anthropic.com/en/docs/build-with-claude/skills)

## What This Skill Does

The Company Research Claude Skill (**cs-company-research**) provides a structured workflow for researching companies and products. It transforms Claude into a professional research assistant that:

- Conducts thorough research using 8-15+ verified sources
- Generates comprehensive 10-section company research reports
- Creates detailed 17-section product deep dive documents
- Provides actionable insights for job applicants
- Maintains professional citations and formatting
- Handles single or multiple companies in one request

---

## Project Files

| File | Purpose |
| --- | --- |
| **cs-company-research.skill** | Company Research Claude Skill **Install this** |
| [cs-company-research.md](http://cs-company-research.md/) | Skill Instructions Used By Claude(For Reference) |
| skill_usage_guide.md | Skill Usage Instructions & Guidance |
| skill_customization_guide.md | Skill Customization Instructions & Guidance |
| example_company_research_substack.md | Example Company Research File |
| example_deep_dive_substack_notes.md | Example Product Deep Dive File |
| [research-guidelines.md](http://research-guidelines.md/) | Research Quality Standards |

---

## Installation

### Prerequisites

- Claude account (Pro or Team plan)
- Access to the Claude Skills feature

### Steps

1. **Download the skill file -** `cs-company-research.skill`.
2. **Install in Claude**
    - Open [Claude](https://claude.ai/)
    - Go to Settings → Skills
    - Click "Add Skill"
    - Upload the `cs-company-research.skill` file
3. **Start using**
    - Use the skill in any conversation with prompts like:
    
    ```
    Use cs-company-research to research [Company] at [URL]
    
    ```
    

## Usage

**Note:** See [skill_usage_guide.md](https://github.com/priankr/claude-skill-company-research/blob/main/skill_usage_guide.md) for detailed instructions on how to use the skill.

### Basic Syntax

```
Use cs-company-research to research [Company Name] at [URL]

```

### Single Company Research

```
Use cs-company-research to research Anthropic at <https://anthropic.com>

```

**Output:** `Anthropic-Research.md` (10-section report, ~3,000-5,000 words)

---

### Multiple Companies

```
Use cs-company-research to research:
- Company A at <https://companya.com>
- Company B at <https://companyb.com>
- Company C at <https://companyc.com>

```

**Output:** Three separate markdown files, researched sequentially

---

### Example With Product Deep Dive

```
Use cs-company-research to research Substack Notes at <https://substack.com/home>
and create a detailed product deep dive

```

**Output:**

- `Substack-Notes-Research.md`
- `Sublime-Notes-Features-and-Functionality.md`

---

## What You'll Get

### Company Research Report

1. **Company Mission** - Official mission statement and core intent
2. **Company Values** - Explicit values and cultural principles
3. **Key Facts** - Founding, location, size, leadership, milestones
4. **Products or Services** - Product catalog with descriptions
5. **Product Deep Dive** - Detailed analysis with subsections:
    - 5.1. How [Product] Works
    - 5.2. What Problems It Solves
    - 5.3. Recent Updates
6. **Industry and Market** - Sector, positioning, trends, competition
7. **Customers and Use Cases** - Target audience, segments, case studies.
8. **Pricing Model** - Pricing tiers, plans, business model
9. **Insights for Applicants** - 3-5 actionable interview/application tips
10. **Complete Source List** - All sources cited throughout

**Length:** ~3,000-5,000 words

**Sources:** 8-15+ with inline citations

**Format:** Professional markdown with headers, bullets, bold emphasis

---

### Product Deep Dive Document (17 Sections)

1. Executive Summary with Key Differentiators
2. Core Architecture / Product Overview
3. Core Features (organized by category with subsections)
4. AI/Automation Features (if applicable)
5. Visual Workspace / Creation Tools (if applicable)
6. Collaboration & Sharing
7. Integrations & Extensions
8. Pricing & Plans
9. User Experience & Interface
10. User Workflows (with comparison tables)
11. Competitive Positioning (with comparison tables)
12. Target User Profile
13. Product Metrics & KPIs (inferred)
14. Product Roadmap Insights
15. Technical Implementation (for technical products)
16. User Feedback & Sentiment
17. Conclusion with Key Takeaways
18. Sources

**Length:** ~5,000-8,000 words

**Format:** Executive summary, numbered subsections, tables, metadata

## Research Quality

Refer to [research_guidelines.md](https://github.com/priankr/claude-skill-company-research/blob/main/research-guidelines.md) for more details.

---

## Use Cases

### 1. Job Interview Preparation

**Scenario:** You have an interview at Stripe for a Product Manager role next week.

**Prompt:**

```
Use cs-company-research to research Stripe at <https://stripe.com>

```

**Output:**

- Company mission, values, and culture insights
- Product portfolio and key features
- Market position and competitive landscape
- 3-5 specific, actionable interview preparation tips

---

### 2. Competitive Analysis

**Scenario:** Your startup is entering the project management software space. You need to understand the competition.

**Prompt:**

```
Use cs-company-research to research these competitors:
- Asana at <https://asana.com>
- Monday.com at <https://monday.com>
- Linear at <https://linear.app>

```

**Output:**

- Three separate comprehensive reports
- Pricing models and feature comparisons
- Market positioning and differentiation
- Customer segments and use cases

---

### 3. Product Deep Dive

**Scenario:** Your team is considering integrating with Notion's API. You need to understand their product capabilities.

**Prompt:**

```
Use cs-company-research to research Notion at <https://notion.so> and create a detailed product deep dive.
```

**Output:**

- Company research report (10 sections)
- Comprehensive product analysis (17 sections)
- Technical capabilities and integrations
- User workflows and competitive positioning

---

## Limitations

### 1. Information Availability

- **Limitation:** Private companies may have limited public information
- **Impact:** Some sections (like revenue, employee count) may be unavailable
- **Mitigation:** Skill explicitly notes when information is not publicly available

### 2. Real-Time Data

- **Limitation:** Claude's knowledge cutoff is January 2025
- **Impact:** Very recent company changes (post-January 2025) require web search
- **Mitigation:** Skill uses web search tools to find current information

### 3. Subjective Analysis

- **Limitation:** Skill focuses on factual research, not strategic recommendations
- **Impact:** Won't provide "should you join this company" type advice
- **Mitigation:** Provides objective insights that inform your own decisions

### 4. Private/Stealth Companies

- **Limitation:** Companies in stealth mode or with no web presence can't be researched
- **Impact:** Output may be minimal or unavailable
- **Mitigation:** Best for companies with public websites and presence

### 5. Research Depth vs. Time

- **Limitation:** Thorough research takes 5-10 minutes per company
- **Impact:** Not suitable for quick, superficial overviews
- **Mitigation:** Quality over speed - the depth justifies the time

### 6. Language Support

- **Limitation:** Optimized for English-language sources
- **Impact:** May have reduced quality for non-English companies
- **Mitigation:** Works best with companies that have English documentation

### 7. Technical Products

- **Limitation:** Deeply technical products (enterprise software, developer tools) may require additional technical expertise to fully evaluate
- **Impact:** Product deep dives are comprehensive but may not replace hands-on evaluation
- **Mitigation:** Skill provides a thorough feature analysis as a strong foundation

## Customization Guide

**Note:** See [skill_customization_guide.md](https://github.com/priankr/claude-skill-company-research/blob/main/skill_customization_guide.md) for how to modify the skill for your specific needs.

---

## Example Output

This repository includes example research reports:

- [**example-company-research-substack-notes.md**](https://github.com/priankr/claude-skill-company-research/blob/main/example-company-research-substack-notes.md) - Complete 10-section company research report for Substack Notes
- [**example-product-deep-dive-substack-notes.md**](https://github.com/priankr/claude-skill-company-research/blob/main/example-product-deep-dive-substack-notes.md) - Comprehensive 17-section product analysis

These examples demonstrate the quality, depth, and format of the skill's output.

## License

This skill is provided under the MIT License.

## Acknowledgments

- Developed and tested with Claude (Anthropic)
- Based on real-world company research workflows

## Related Resources

- [Anthropic Claude Skills Announcement](https://www.anthropic.com/news/claude-skills)
- [Claude Documentation](https://docs.anthropic.com/)
- [Skill Creation Guide](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)

---
