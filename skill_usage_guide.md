# Usage Guide

This guide provides detailed instructions and examples for using the cs-company-research skill effectively.

**Note:** See [skill_customization_guide.md]() for instructions on how to modify the skill for your specific needs.

## Getting Started

### Prerequisites

- Claude account (Pro, or Team)
- Access to Claude Skills (available in Settings)

### Installation

1. Download `cs-company-research.skill` from the repository
2. Open Claude at https://claude.ai
3. Navigate to Settings → Skills
4. Click "Add Skill"
5. Upload the `.skill` file
6. Confirm the skill appears in your skills list

### Verification

Test that the skill is working:

```
Use cs-company-research to research Anthropic at https://anthropic.com.
```

If successful, you'll receive a markdown file named `Anthropic-Research.md`.

## Basic Usage

### Syntax

```
Use cs-company-research to research [Company Name] at [URL]
```

### Single Company

**Example 1: Technology Company**
```
Use cs-company-research to research Stripe at https://stripe.com.
```

**Output:** `Stripe-Research.md` containing:
- 10 comprehensive sections
- ~3,000-5,000 words
- 8-15+ cited sources
- Pricing information
- Job application insights

---

**Example 2: Consumer Product**
```
Use cs-company-research to research Notion at https://notion.so.
```

**Output:** `Notion-Research.md` with company and product analysis

---

**Example 3: Startup**
```
Use cs-company-research to research Linear at https://linear.app.
```

**Output:** `Linear-Research.md` focused on a product-first company

### Multiple Companies

Research several companies in one request:

```
Use cs-company-research to research:
- Asana at https://asana.com
- Monday.com at https://monday.com
- ClickUp at https://clickup.com
```

**Output:**
- `Asana-Research.md`
- `Monday-Com-Research.md`
- `ClickUp-Research.md`

**Note:** Companies are researched sequentially. Expect ~5-10 minutes per company.

### Product-Focused Research

When you provide a specific product URL:

```
Use cs-company-research to research Figma at https://figma.com/design.
```

The skill will:
1. Research the company (Figma)
2. Focus Section 5 (Product Deep Dive) on the Design product specifically
3. List other products briefly in Section 4

### With Product Deep Dive

Request both company research AND comprehensive product analysis:

```
Use cs-company-research to research Sublime at https://sublime.app 
and create a detailed product deep dive
```

**Output:**
- `Sublime-Research.md` (10-section company report)
- `Sublime-App-Features-and-Functionality.md` (17-section product analysis)

**When to use:**
- Complex products needing detailed feature analysis
- Technical evaluation for integration decisions
- Comprehensive competitive product comparison
- Product management research

## Advanced Usage

### Job Interview Preparation

**Scenario:** You have an interview coming up

```
I'm interviewing at [Company] for a [Role] position next week. 
Use cs-company-research to help me prepare.
```

**Example:**
```
I'm interviewing at Stripe for a Product Manager position. 
Use cs-company-research to help me prepare.
```

**What happens:**
- Standard 10-section research
- Section 9 (Insights) tailored to the Product Manager role
- Emphasis on product strategy, the payments industry, and Stripe's culture
- Specific talking points for interviews

---

### Competitive Analysis

**Scenario:** Comparing competitors in a market

```
Use cs-company-research to research these project management tools:
- Asana at https://asana.com
- Linear at https://linear.app
- Jira at https://atlassian.com/software/jira

Focus on pricing models and target customer segments.
```

**What happens:**
- Three separate research reports
- Special attention to pricing (Section 8) and customers (Section 7)
- Can manually compare across reports
- Each report is self-contained

---

### Market Research

**Scenario:** Understanding an industry space

```
Use cs-company-research to research these AI companies:
- OpenAI at https://openai.com
- Anthropic at https://anthropic.com
- Cohere at https://cohere.com

I'm interested in their business models and target markets.
```

**What happens:**
- Three detailed reports
- Emphasis on business model (Section 8 pricing)
- Target market analysis (Section 7)
- Industry positioning (Section 6)

---

### Investment Due Diligence

**Scenario:** Evaluating a potential investment

```
Use cs-company-research to research [Startup] at [URL] 
and create a detailed product deep dive. 
I'm evaluating this company for a Series A investment.
```

**What happens:**
- Comprehensive company research (funding, team, market)
- Detailed product analysis (competitive moats, technical capabilities)
- Market opportunity assessment
- Customer validation signals

---

### Partnership Evaluation

**Scenario:** Assessing potential partners

```
Use cs-company-research to research [Company] at [URL]. 
Focus on their values, culture, and customer base as we're 
evaluating a strategic partnership.
```

**What happens:**
- Standard research with emphasis on Sections 2, 6, 7
- Values alignment insights
- Customer overlap analysis
- Partnership compatibility signals

## Understanding the Output

### Company Research Report Structure

```markdown
# [Company-Name] Company Research Report

## 1. Company Mission
- Official mission statement (verbatim)
- One-sentence summary
- Source citations

## 2. Company Values
- Explicit values from official sources
- Cultural principles
- Behavioral norms

## 3. Key Facts
- Founded: Year
- Headquarters: Location
- Team Size: Number
- Funding: Amount and investors
- Leadership: CEO and key executives
- Milestones: Major achievements

## 4. Products or Services
- Product catalog with brief descriptions
- Core components (if applicable)

## 5. Product Deep Dive
### 5.1. How [Product] Works
- Core functionality
- Key features
- User interaction

### 5.2. What Problems It Solves
1. Problem 1 with explanation
2. Problem 2 with explanation
...

### 5.3. Recent Updates
- New features
- Launch dates
- Roadmap items

**Integrations:**
- Listed integrations

## 6. Industry and Market
- Primary industry/sector
- Market position
- Trends and opportunities
- Key competitors

## 7. Customers and Use Cases
- Target audience (B2B/B2C)
- Customer segments
- Notable clients
- Use cases
- Customer feedback quotes

## 8. Pricing Model
- Free tier (if applicable)
- Paid tiers with pricing
- Enterprise options
- Pricing philosophy

## 9. Insights for Applicants
1. **Insight Title:**
   - Supporting details
   - How to apply

2. **Insight Title:**
   - Supporting details
   - How to apply
...

## 10. Complete Source List
1. [Website | Page](url)
2. [Website | Page](url)
...
```

### Product Deep Dive Structure

See `example-product-deep-dive-substack-notes.fofor complete example.

## Best Practices

### 1. Provide Specific URLs

**Good:**
```
Use cs-company-research to research Notion at https://notion.so/product
```

**Better:**
```
Use cs-company-research to research Notion's AI features at https://notion.so/product/ai
```

**Why:** Specific URLs help the skill focus on the exact product/feature you care about.

---

### 2. Clarify Your Use Case

**Basic:**
```
Use cs-company-research to research Stripe at https://stripe.com
```

**Better:**
```
I'm preparing for a Product Manager interview at Stripe. 
Use cs-company-research to research Stripe at https://stripe.com
```

**Why:** Context helps the skill tailor insights (Section 9) to your needs.

---

### 3. Request Product Deep Dives When Needed

**When to request:**
- ✅ Complex products (SaaS platforms, developer tools)
- ✅ Technical evaluation needed
- ✅ Competitive feature comparison required
- ✅ Product management research

**When to skip:**
- ❌ Simple products (basic research sufficient)
- ❌ Time constraints (deep dives take 10-15 minutes)
- ❌ Company-level focus (not product-specific)

---

### 4. Research Sequentially for Multiple Companies

If researching many companies (5+), break into batches:

**Instead of:**
```
Research 10 companies at once
```

**Do this:**
```
Batch 1: Research companies 1-3
[Wait for completion]
Batch 2: Research companies 4-6
[Wait for completion]
...
```

**Why:** Easier to review and manage, better error handling

---


### 5. Verify Critical Information

The skill prioritizes verified sources, but always:
- Cross-check critical data points (funding, revenue, size)
- Visit official company pages for the latest information
- Note the research date in your records

---

### 6. Update Research Periodically

Companies change. Re-research every:
- **3 months:** Fast-growing startups
- **6 months:** Mid-stage companies
- **12 months:** Established companies

## Troubleshooting

### Issue: "File not found" Error

**Symptoms:** Error message about file not being found in outputs directory

**Cause:** Rare file system issue with Claude

**Solution:**
```
Please try saving the file again.
```

Or specify a simple filename:
```
Use cs-company-research to research [Company] and save as company-research.md
```

---

### Issue: Missing Information in Sections

**Symptoms:** Sections say "Information not publicly available"

**Causes:**
- Private company with limited public information
- Stealth mode startup
- Information genuinely not public

**Solutions:**
- Accept the limitation for private information
- Try researching press releases or news coverage separately
- Focus on publicly available sections

---

### Issue: Research Takes Too Long

**Symptoms:** Research exceeding 10-15 minutes per company

**Causes:**
- Complex company with many products
- Limited information requiring extensive searching
- Multiple products requiring deep analysis

**Solutions:**
- Skip product deep dive if not essential
- Research companies with better public information

---

### Issue: Product Deep Dive Not Generated

**Symptoms:** Only company research report created

**Causes:**
- Didn't explicitly request a deep dive
- Product information is already comprehensive in Section 5
- The company offers services, not discrete products

**Solutions:**
- Explicitly request: "and create a detailed product deep dive"
- Check if Section 5 already has sufficient product detail
- Accept that not all companies need separate deep dives

---

### Issue: Sources Seem Limited

**Symptoms:** Fewer than 8 sources cited

**Causes:**
- Small or new company with limited presence
- Niche market with few sources
- Private company

**Solutions:**
- Supplement with manual research if critical
- Focus on the quality of sources over quantity

---

### Issue: Insights Not Relevant to My Use Case

**Symptoms:** Section 9 insights don't match your needs

**Causes:**
- Didn't specify use case in request
- Default insights assume a job seeker perspective

**Solutions:**
- Provide context in your request:
  ```
  I'm researching [Company] for [specific purpose]. 
  Use cs-company-research to research [Company] at [URL]
  ```
- Manually adapt insights to your use case
- Request follow-up: "Can you provide insights focused on competitive analysis?"

## Tips for Best Results

1. **Be specific** about your research purpose
2. **Provide product URLs** when focusing on specific products
3. **Request deep dives** for complex products
4. **Research sequentially** when doing multiple companies
5. **Save reports** systematically for future reference
6. **Update regularly** for fast-changing companies
7. **Cross-reference** critical data points
8. **Provide feedback** to improve the skill over time

---