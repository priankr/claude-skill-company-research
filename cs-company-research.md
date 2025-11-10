# Company Research Skill Instructions

 **Note:** This file contains the instructions that Claude follows when using the cs-company-research skill. It's included in the repository for transparency and to help users understand how the skill works.
 
**For general usage instructions, see [README.md]()**

---


---
name: cs-company-research
description: Structured workflow for researching companies and products for competitive analysis or job search preparation. Use when the user requests company research, competitive research, product analysis, or preparation for job applications. Triggers include requests like "research [company]", "help me prepare for interview at [company]", "competitive analysis of [companies]", or when provided with company URLs to analyze. Generates individual research reports for each company with focus on mission, values, products, market position, and actionable insights for job seekers.
---

# Company & Product Research

## Overview

This skill provides a structured, two-step workflow for conducting thorough company and product research. It's designed for competitive analysis, market research, and job search preparation.

**Key capabilities:**
- Research multiple companies/products in a single request
- Generate individual markdown files for each company
- Focus on product-specific information when URLs are provided
- Provide actionable insights for job applicants
- Maintain high research quality with verified sources

## Research Workflow

When the user requests company research, follow this two-step process:

### Step 1: Company Research
Create a comprehensive company research document covering: mission, values, key facts, products, market position, customers, and insights for applicants.

### Step 2: Product Deep Dive (Optional)
If the company has significant products or the user requests deeper product analysis, create a separate detailed document focused on product features, functionality, and user experience.

**File naming conventions:**
- Company research: `[Company-Name]-Research.md` (use hyphens, no spaces)
- Product deep dive: `[Product-Name]-Features-and-Functionality.md` (use hyphens, no spaces)

**Examples:**
- `Substack-Research.md`
- `Notion-Research.md`
- `Sublime-App-Features-and-Functionality.md`

**Important:** Always use hyphens (-) instead of spaces in filenames to avoid file system errors.

## Processing Multiple Companies

When the user provides multiple companies:

1. **Acknowledge the request** - Confirm which companies will be researched
2. **Research sequentially** - Complete both steps for Company A, then move to Company B
3. **Use 10-15 tool calls per company** - Thorough research requires multiple web_search and web_fetch calls
4. **Create separate files** - Each company gets its own markdown document(s)
5. **Summarize completion** - After all companies, provide a brief summary with links to all generated files

**Example user request:**
> "Help me research Company A (https://companya.com/product), Company B (https://companyb.com), and Company C (https://companyc.com/about) using the cs-company-research skill"

## Step 1: Company Research

Generate a comprehensive research report with the following structure and guidelines:

### Research Approach

**Source priority:**
1. Official company pages (About, Careers, Products, Press, Investor Relations)
2. Reputable external sources (major news outlets, analyst reports, app stores)
3. Supplemental sources only when primary sources lack information

**Research depth:**
- Use 8-15 tool calls (web_search and web_fetch) per company
- Verify key facts across multiple sources
- Focus on the specific product if a product URL is provided
- Consult `references/research-guidelines.md` for detailed quality standards

### Document Structure

Create a markdown document with these sections:

#### 1. Company Mission
- Extract the official mission or vision statement verbatim if available
- Include source citation immediately after the statement
- Add a one-sentence summary of its core intent
- If not explicitly stated, note: "Official mission statement not publicly available"

#### 2. Company Values
- List explicitly stated values with citations
- Include cultural principles or behavioral norms found on careers/about pages
- Note inferred values only if they appear consistently across multiple sources
- Format as a bulleted list with brief explanations if needed

#### 3. Key Facts
Provide 5-7 concise, well-sourced facts covering:
- **Founded:** Year and circumstances
- **Headquarters:** Location(s)
- **Scale:** Employee count, revenue range (if disclosed), or funding raised
- **Leadership:** CEO, founders, or key executives
- **Milestones:** Notable achievements, awards, acquisitions, or recognitions

Format as bullet points with inline citations. Include "As of [date]" for time-sensitive metrics.

#### 4. Products or Services
List the company's main products/services with brief descriptions:

**Format:**
- **[Product Name]** — One-sentence description of what it does
- If a product URL was provided, mark that product with **bold** emphasis

**Core Components (if applicable):**
- List key product components (e.g., web app, mobile app, browser extension, API)
- Keep this section concise - just the product catalog

#### 5. Product Deep Dive
**For the primary product (or the product specified in the URL), create detailed subsections:**

**Organize using numbered subsections (5.1, 5.2, 5.3, etc.):**

**5.1. How [Product] Works**
- Core functionality and workflow
- Key mechanisms and features (5-8 main features)
- How users interact with the product
- Technical architecture overview (if relevant)

**5.2. What Problems It Solves**
- List 3-5 primary problems addressed
- Number each problem with explanation
- Include user pain points from reviews/testimonials

**5.3. Recent Updates**
- New features or launches (with dates)
- Version releases or major changes
- Upcoming roadmap items (if publicly shared)

**Include integrations list if applicable:**
- Partner integrations
- Import/export capabilities
- API connections

**If researching a company with multiple major products but no specific product URL provided:**
Provide a balanced overview of the top 2-3 products using simplified subsections.

#### 6. Industry and Market
- **Industry:** Identify the primary sector (e.g., "Enterprise SaaS", "Consumer FinTech")
- **Market position:** Describe the company's niche, target segment, or unique positioning
- **Market context:** Summarize relevant trends, opportunities, or challenges
- **Competition:** Note key competitors if readily apparent
- Support all claims with citations

#### 7. Customers and Use Cases
- **Target audience:** B2B/B2C, specific industries, company sizes, geographic focus
- **Customer segments:** Different types of users or buyer personas
- **Notable clients:** Named customers, case studies, or testimonials (if available)
- **Use cases:** Concrete examples of how customers use the product/service
- **Customer feedback:** Include quotes from reviews, testimonials, or app stores (if available)

#### 8. Pricing Model (if publicly available)
Include pricing information if the company publicly shares it:

**Format:**
- Tier names with pricing (e.g., "Free: [features]", "Premium: $X/month")
- What's included in each tier
- Annual vs. monthly options
- Free trial or freemium availability
- Enterprise/custom options
- Company's pricing tagline or philosophy (if stated)

**If pricing is not public:** Note "Pricing not publicly disclosed" or "Contact for quote"

#### 9. Insights for Applicants
Provide 3-5 specific, actionable insights that help a job applicant prepare:

**Format each insight as a numbered list with bold title:**

1. **[Insight Title]:**
   - Supporting details and evidence
   - How to apply it in interviews or cover letters
   - Specific examples when possible

**Example:**
1. **Emphasize Values Over Features:**
   - Demonstrate alignment with "[specific company values from Section 2]"
   - Show you understand the cultural mission beyond just the product
   - In interviews, discuss how your experience reflects these values

**Good insight topics:**
- Skills or experiences to emphasize based on company needs
- Values alignment strategies from Section 2
- Product knowledge to demonstrate from Section 5
- Industry trends to discuss from Section 6
- Company challenges to address from market analysis
- Cultural fit indicators from mission/values
- Long-term thinking if founder emphasizes patience/craft

#### 10. Complete Source List
Provide a numbered list of all sources used:

**Format:**
```
1. [Website Name | Page Title](url)
2. [Website Name | Page Title](url)
3. [Website Name | Page Title](url)
...
```

**Requirements:**
- Include every source cited throughout the document
- Maintain consistent formatting
- Number sequentially
- Do not include sources not actually cited in the document

### Document Structure Summary

The final company research document should have exactly 10 sections:
1. Company Mission
2. Company Values
3. Key Facts
4. Products or Services
5. Product Deep Dive (with numbered subsections)
6. Industry and Market
7. Customers and Use Cases
8. Pricing Model
9. Insights for Applicants
10. Complete Source List

### Formatting Guidelines

- **Headers:** Use clear, sentence-case section headers (##, ###)
- **Citations:** Cite sources inline using format: [Website Name | Page Title](url)
- **Bullets:** Use bulleted lists for values, facts, and features
- **Emphasis:** Bold key terms and company/product names for scannability
- **Conciseness:** Use short sentences and clear paragraphs
- **Factual tone:** Professional, objective, and verifiable

### Quality Checks

Before finalizing the document:
- ✓ All major sections have content (or explicitly note if info unavailable)
- ✓ Every claim is cited with a reputable source
- ✓ Product focus aligns with provided URL (if applicable)
- ✓ Insights are specific and actionable, not generic
- ✓ Source list is complete and properly formatted
- ✓ No speculation or unverified claims

## Step 2: Product Deep Dive

**When to create this document:**
- User explicitly requests deeper product analysis
- The product is complex with many features
- The company research document's Product Deep Dive section is limited
- The product is the main focus of the user's interest

**When to skip this document:**
- Product information is comprehensive in Step 1
- Company offers services rather than discrete products
- User indicates they only need company-level information

### Document Structure

Create a separate markdown document titled: `[Product-Name]-Features-and-Functionality.md` (use hyphens, no spaces)

**Example:** `Sublime-App-Features-and-Functionality.md`

#### Document Metadata
Include at the top:
- **Document Version:** (e.g., 1.0)
- **Last Updated:** [Date]

#### Executive Summary
Start with a 2-3 paragraph executive summary covering:
- What the product is and its core purpose
- Target audience and use case
- How it differs from competitors

**Key Differentiators** subsection (bulleted list of 4-6 unique aspects)

---

#### Target Audience
Product teams, product managers, stakeholders, and anyone needing detailed understanding of product capabilities.

#### Content Sections

**1. Core Architecture / Product Overview**
- Platform components (web, mobile, desktop, API)
- Data model or content structure
- Technical infrastructure overview
- Deployment options

**2. Content Capture / Core Features** (Adapt section title to product)
Organize by feature category with numbered subsections (2.1, 2.2, etc.):
- **2.1. [Feature Category Name]**
  - How it works
  - Key capabilities
  - User workflows
- **2.2. [Feature Category Name]**
  - Continue pattern

For each major feature:
- **Feature name:** Brief description
- **Functionality:** How it works
- **User benefit:** Why it matters
- **Availability:** (If applicable) Plan tier, platform, or prerequisites

**3. AI/Automation Features** (if applicable)
- How AI is integrated
- Automation capabilities
- Intelligence features
- Design philosophy around AI

**4. Visual Workspace / Creation Tools** (if applicable)
- Canvas, editor, or creation environment
- Supported elements and capabilities
- Use cases for the tool
- Limitations (if known)

**5. Collaboration & Sharing** (if applicable)
- Privacy model and settings
- Sharing capabilities
- Team features
- Permissions and access control

**6. Integrations & Extensions**
- Third-party integrations
- API availability
- Import/export capabilities
- Plugin ecosystem

**7. Pricing & Plans**
- Pricing tiers with features
- Free trial or freemium model
- Annual vs. monthly options
- Enterprise offerings
- Business model insights

**8. User Experience & Interface**
- Interface design approach
- Ease of use and learning curve
- Accessibility features
- Performance characteristics
- Mobile vs. desktop experience

**9. User Workflows** (Optional but recommended)
Create a table showing common use cases and workflows:

| Use Case | Workflow Steps |
|----------|----------------|
| Writer's Research | 1. Step one<br>2. Step two<br>3. Step three |
| Designer's Process | 1. Step one<br>2. Step two |

**10. Competitive Positioning** (Optional but valuable)
Create comparison table vs. key competitors:

| vs. Competitor A | vs. Competitor B | vs. Competitor C |
|-----------------|------------------|------------------|
| • Differentiator 1<br>• Differentiator 2 | • Differentiator 1<br>• Differentiator 2 | • Differentiator 1<br>• Differentiator 2 |

**11. Target User Profile** (Optional)
- Ideal user characteristics
- User persona description
- Pain points addressed
- Current tool alternatives

**12. Product Metrics & KPIs** (Optional - if inferrable)
Potential engagement, retention, or conversion metrics based on product type

**13. Product Roadmap Insights** (Optional)
- Known limitations
- Potential future features (clearly mark as inferred)
- Product philosophy and direction

**14. Technical Implementation** (Optional - for technical products)
- Architecture estimates
- Technology stack (if known)
- Data model approach

**15. User Feedback & Sentiment** (if available)
- Quotes from reviews
- Common praise themes
- Common criticism themes
- Feature highlights from users

**16. Conclusion**
- Summary of key capabilities
- Primary differentiators
- Best suited for [user type]
- Key takeaways (3-5 bullets)

**17. Sources**
Complete numbered list of all sources used

### Flexibility Note
Not every product will need all 17 sections. Adapt the structure based on:
- Product complexity
- Available information
- User's needs
- Time constraints

**Minimum sections:** 1-8 plus Sources (core product information)
**Recommended:** Sections 1-11 plus Sources (comprehensive understanding)
**Optional additions:** Sections 12-16 for extra depth

### Research Strategy for Product Deep Dive

Use these sources for comprehensive product information:

1. **Product landing page** - Core features and value prop
2. **Product documentation** - Detailed functionality
3. **Help center/Knowledge base** - User workflows and how-tos
4. **App store listings** - Features, screenshots, user reviews
5. **Product demo videos** - Visual walkthrough of capabilities
6. **Release notes/Changelog** - Recent updates and version history
7. **Pricing page** - Plans and feature availability
8. **User reviews** (G2, Capterra, app stores) - Real-world usage and pain points
9. **Product comparison sites** - How it stacks up to alternatives
10. **Company blog** - Product announcements and thought leadership

Aim for 10-15 tool calls to gather comprehensive product information.

## Best Practices

### Before Starting Research
- Clarify how many companies to research if ambiguous
- Confirm if both Step 1 and Step 2 are needed
- Note any specific areas of focus the user mentions

### During Research
- **Use web_fetch extensively** - Don't rely only on search snippets; fetch full pages for complete information
- **Verify facts** - Cross-reference key data points across multiple sources
- **Stay focused** - If a product URL is provided, prioritize that product in the research
- **Note gaps** - If information isn't available, explicitly state this rather than guessing
- **Track sources** - Keep organized notes of all sources for the final source list

### After Completing Each Company
- Review the document for completeness
- Verify all citations are properly formatted
- Check that insights are specific, not generic
- Ensure markdown formatting is consistent

### When Researching Multiple Companies
- Complete one company fully before starting the next
- Keep consistent formatting and depth across all companies
- At the end, create a brief summary comparing key findings

## Common Pitfalls to Avoid

❌ **Insufficient research depth** - Using only 2-3 sources or relying on search snippets
❌ **Missing citations** - Making claims without source attribution
❌ **Generic insights** - Advice that could apply to any company
❌ **Speculation** - Inferring facts not supported by sources
❌ **Inconsistent formatting** - Different structures across company reports
❌ **Product confusion** - Mixing up different products from the same company
❌ **Ignoring URL context** - Not focusing on the specific product in a provided URL
❌ **Poor source quality** - Using unverified blogs or AI summaries

## Reference Materials

For detailed guidance on research quality, source evaluation, and section-specific best practices, consult:

**`references/research-guidelines.md`** - Comprehensive guide covering:
- Source quality standards (what to use, what to avoid)
- Citation formatting and best practices
- Research process recommendations
- Handling missing information
- Section-specific guidelines for each report component
