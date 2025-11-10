# Customization Guide

This guide shows you how to modify the cs-company-research skill to meet your specific needs.

**Note:** See [skill_usage_guide.md](https://github.com/priankr/claude-skill-company-research/blob/main/skill_usage_guide.md) for instructions how to use the skill.

## Why Customize?

The default skill is designed for general company research, but you might want to:

- Add industry-specific sections (SaaS metrics, e-commerce performance, etc.)
- Focus on specific aspects (technical details, sustainability, diversity)
- Adjust research depth (faster/lighter or deeper/comprehensive)
- Change output format (different section order, additional summaries)
- Target different audiences (investors vs. job seekers vs. competitors)

## Customization Methods

### Method 1: Use Claude to Modify (Recommended)

The easiest way to customize the skill is to ask Claude to modify it for you.

**Basic template:**
```
I want to modify the cs-company-research skill to [your modification]. 
Can you help me update the SKILL.md file?
```

**Claude will:**
1. Read the current SKILL.md
2. Make your requested changes
3. Show you the modifications
4. Create an updated .skill file

**Example:**
```
I want to modify the cs-company-research skill to add a "Team & Leadership" 
section that analyzes the founding team's background, advisory board, and 
key executive experience. Can you add this as Section 4, and shift the 
current sections down?
```

---

### Method 2: Manual Editing

For hands-on customization:

1. **Extract contents:**
   ```bash
   # Rename to .zip
   mv cs-company-research.skill cs-company-research.zip
   
   # Unzip
   unzip cs-company-research.zip -d cs-company-research-custom
   ```

2. **Edit files:**
   - `SKILL.md` - Main instructions
   - `research-guidelines.md` - Quality standards (optional)

3. **Repackage:**
   ```bash
   # Zip the folder
   cd cs-company-research-custom
   zip -r ../cs-company-research-custom.skill *
   ```

4. **Upload to Claude:**
   - Settings → Skills → Add Skill
   - Upload your custom .skill file

## Common Customizations

### 1. Add Industry-Specific Sections

#### For SaaS Companies

**Request to Claude:**
```
Modify cs-company-research to add a "SaaS Metrics & Business Model" section 
after the Pricing Model section. It should analyze:
- Revenue model (subscription, usage-based, hybrid)
- Contract structure (monthly, annual, multi-year)
- Estimated ARR/MRR (if disclosed)
- Customer acquisition strategy
- Churn indicators
- Expansion revenue approach
```

**Result:** New Section 9 focused on SaaS-specific metrics

---

#### For FinTech Companies

**Request to Claude:**
```
Add a "Regulatory & Compliance" section to the skill that analyzes:
- Licenses and regulatory approvals
- Compliance frameworks (KYC, AML, etc.)
- Data security standards
- Banking partnerships
- Geographic regulatory status
```

---

### 2. Adjust Research Depth

#### Lighter, Faster Research

**Request to Claude:**
```
Modify cs-company-research to do lighter research:
- Reduce to 5-8 tool calls per company (from 8-15)
- Focus on official company sources only
- Reduce Company Research to 8 sections (remove Pricing Model)
- Skip customer feedback collection
```

**Use case:** Quick overviews, time-sensitive research

---

#### Deeper, Comprehensive Research

**Request to Claude:**
```
Modify cs-company-research to do deeper research:
- Increase to 15-20 tool calls per company
- Add more subsections to Product Deep Dive (5.4, 5.5, 5.6)
- Require verification of key facts across 3+ sources
- Add "Recent News & Announcements" section
```

**Use case:** Due diligence, major decisions

---

### 3. Change Target Audience

#### For Investors/VCs

**Request to Claude:**
```
Modify Section 9 "Insights for Applicants" to "Investment Considerations" 
that analyzes:
- Market size and growth potential
- Competitive moats and defensibility
- Revenue model sustainability
- Team strength and track record
- Capital efficiency indicators
- Risk factors and challenges
- Exit potential
```

---

#### For Sales Teams

**Request to Claude:**
```
Modify Section 9 to "Sales Intelligence" that provides:
- Ideal customer profile
- Key pain points and buying triggers
- Decision-maker information
- Budget indicators
- Competitive positioning angles
- Objection handling insights
```

---

### 4. Add Specific Analysis Sections

#### Sustainability & ESG

**Request to Claude:**
```
Add a "Sustainability & ESG Practices" section after Section 7 that covers:
- Environmental commitments and initiatives
- Social impact programs
- Governance structure
- Diversity and inclusion data
- Sustainability reporting
- Carbon footprint disclosures
```

---

#### Technology Stack

**Request to Claude:**
```
Add a "Technology & Infrastructure" section to Product Deep Dive that analyzes:
- Core technology stack (if known)
- Cloud infrastructure provider
- Development frameworks
- API architecture
- Security infrastructure
- Technical team size and expertise
```

---

### 5. Modify Output Format

#### Add Executive Summary

**Request to Claude:**
```
Modify the Company Research report to add an "Executive Summary" as the 
very first section (before Section 1). It should be 2-3 paragraphs covering:
- What the company does
- Key differentiators
- Market position
- Most relevant finding for the user
```

---

#### Change Section Order

**Request to Claude:**
```
Reorder the Company Research sections to put:
- Products or Services as Section 2 (after Mission)
- Company Values as Section 3
- Key Facts as Section 4
This front-loads the most important product information.
```

---

#### Add Comparison Tables

**Request to Claude:**
```
When researching multiple companies, automatically generate a comparison 
table at the end summarizing:
- Founded year
- Size (employees)
- Funding
- Primary product
- Pricing model
- Target market
```

---

### 6. Change Citation Style

#### Numbered Footnotes

**Request to Claude:**
```
Change the citation format from inline [Website | Page](url) to numbered 
footnotes [1] with references at the end of each section.
```

---

#### APA Style

**Request to Claude:**
```
Modify citations to use APA format:
(Author, Year) inline with full references at the end.
```

## Step-by-Step Example

**Goal:** Customize for SaaS company analysis

**Step 1: Request comprehensive SaaS modifications**
```
I want to create a SaaS-focused version of cs-company-research. Please modify:

1. Add "SaaS Metrics & KPIs" section covering:
   - Pricing model type
   - Contract terms
   - Estimated MRR/ARR
   - Customer acquisition approach
   - Churn indicators

2. Enhance Product Deep Dive to add:
   - API and developer experience
   - Integration marketplace
   - Uptime and reliability data
   - Feature release cadence

3. Update "Customers and Use Cases" to analyze:
   - Customer segmentation by size (SMB/Mid-Market/Enterprise)
   - Vertical specialization
   - Self-serve vs. sales-led 

4. Add section on "Product-Led Growth Indicators"

Please create this as a new skill file called "cs-company-research-saas"
```

**Step 2: Save as a separate skill**
Name it `cs-company-research-saas.skill` for SaaS-specific research.

**Step 3: Test on SaaS companies**
```
Use cs-company-research-saas to research Notion at https://notion.so.
```

---

## Best Practices

1. **Keep the YAML frontmatter intact** - The `name` and `description` fields are critical.
2. **Test after modifications** - Research a test company to ensure changes work
3. **Maintain citation requirements** - Don't remove source verification.
4. **Keep sections focused** - Each section should have a clear purpose.
5. **Update examples** - If you change the structure, update the example outputs
6. **Save versions** - Keep the original skill file before making major changes.

### Getting Help with Modifications

If you're unsure how to modify the skill:

1. **Describe your use case** to Claude in detail.
2. **Ask Claude to review** the current [SKILL.md](http://skill.md/) structure
3. **Request specific changes** you want to make
4. **Test the modified version** on a real company.
5. **Iterate** based on results

Claude can read, modify, and repackage skills efficiently!
---
