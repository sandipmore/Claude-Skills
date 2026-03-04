---
name: business-plan
description: "Create professional, investor-ready business plan documents (.docx). Use this skill whenever the user asks for a business plan, startup plan, venture plan, go-to-market strategy document, pitch document, or any comprehensive business planning document. Also trigger when the user mentions 'business model canvas as a doc', 'funding proposal', 'investor document', or wants to formalize a business idea into a structured plan. This skill produces polished Word documents with proper formatting, tables, and a table of contents. Even if the user only says 'help me plan my business' or 'I have a startup idea', consider using this skill to give them a tangible deliverable."
---

# Business Plan Creator

Generate professional, well-structured business plan documents in .docx format using the docx skill's capabilities.

## When to Use

- User wants a business plan, startup plan, or venture proposal
- User asks for a go-to-market strategy document or funding proposal
- User wants to formalize a business idea into a structured document
- User needs an investor-ready business plan

## Workflow

### Step 1: Gather Information

Before generating anything, collect key details from the user. Ask only what's missing — don't re-ask things already mentioned in conversation. Key information to gather:

**Must-haves (ask if not provided):**
- Business name and one-line description
- Industry / sector
- Core product or service offering
- Target customer / market

**Nice-to-haves (use defaults or skip if not provided):**
- Revenue model / pricing strategy
- Key competitors
- Founding team background
- Current stage (idea, MVP, revenue-generating, etc.)
- Funding needs and use of funds
- Financial projections or assumptions
- Unique value proposition / competitive advantage
- Timeline / milestones

Use sensible defaults and placeholder language (clearly marked as `[TO BE COMPLETED]`) for anything the user hasn't provided, so they get a complete document they can fill in later.

### Step 2: Read the docx Skill

Before writing any code, read `/mnt/skills/public/docx/SKILL.md` to follow the latest best practices for creating .docx files. This is critical — the docx skill has specific rules about formatting, tables, lists, and validation that must be followed.

### Step 3: Generate the Document

Create the business plan as a .docx file using `docx-js` (via `npm install -g docx`). The document should be polished, professional, and ready to share with investors or stakeholders.

#### Document Structure

Use this standard business plan structure. Adapt section depth and detail based on what the user has provided — skip or slim down sections where there's no information, rather than filling them with generic filler.

```
Cover Page
  - Business name (large, centered)
  - Tagline / one-liner
  - Date
  - "Confidential" notice (optional)

Table of Contents

1. Executive Summary
   - Business overview (2-3 paragraphs)
   - Mission statement
   - Key highlights (revenue model, market size, funding ask)

2. Company Description
   - Legal structure and founding date
   - Location
   - Vision and mission
   - Current stage and milestones achieved

3. Products & Services
   - Core offering description
   - Value proposition
   - Product roadmap / future plans

4. Market Analysis
   - Industry overview and trends
   - Target market and customer segments
   - Total Addressable Market (TAM), Serviceable Addressable Market (SAM), Serviceable Obtainable Market (SOM)
   - Customer personas (if provided)

5. Competitive Analysis
   - Direct and indirect competitors
   - Competitive advantage / differentiation
   - Competitor comparison table

6. Marketing & Sales Strategy
   - Go-to-market approach
   - Customer acquisition channels
   - Sales process
   - Pricing strategy

7. Operations Plan
   - Key activities and processes
   - Technology and infrastructure
   - Key partnerships and suppliers

8. Management Team
   - Founder(s) and key team members
   - Roles and relevant experience
   - Advisory board (if any)
   - Hiring plan

9. Financial Plan
   - Revenue model details
   - Financial projections (3-5 year summary table)
   - Key assumptions
   - Break-even analysis
   - Funding requirements and use of funds

10. Appendix (optional)
    - Supporting data, charts, or references
```

#### Formatting Guidelines

Follow these formatting rules for a professional appearance:

**Page setup:**
- US Letter size (12240 x 15840 DXA)
- 1-inch margins all around (1440 DXA)

**Typography:**
- Default font: Arial, 12pt (size: 24 in docx-js half-points)
- Headings: Arial Bold — H1 at 16pt, H2 at 14pt, H3 at 12pt bold
- Line spacing: 1.15 or 1.5 for readability

**Color scheme** (professional blue theme):
- Primary accent: `#1B4F72` (dark blue) — use for heading text
- Secondary accent: `#2E86C1` (medium blue) — use for table headers
- Table header background: `#D4E6F1` (light blue)
- Table border: `#BDC3C7` (light gray)
- Body text: `#2C3E50` (dark charcoal)

**Cover page:**
- Business name in large bold text (28-32pt), centered
- Tagline below in lighter weight
- Date and confidentiality notice at bottom
- Use a page break after the cover page

**Tables:**
- Always use DXA widths (never percentages)
- Set both `columnWidths` on table AND `width` on each cell
- Use `ShadingType.CLEAR` for header row backgrounds
- Add cell margins for readability: `{ top: 80, bottom: 80, left: 120, right: 120 }`
- Light gray borders: `BorderStyle.SINGLE, size: 1, color: "BDC3C7"`

**Lists:**
- Use proper `LevelFormat.BULLET` numbering config — never unicode bullets
- Use `LevelFormat.DECIMAL` for numbered lists

**Table of Contents:**
- Include a TOC after the cover page using `TableOfContents`
- Ensure all headings use `HeadingLevel` and styles have `outlineLevel` set

**Placeholders:**
- For missing information, use clearly marked placeholders: `[TO BE COMPLETED: description of what goes here]`
- Style placeholders in italic and a muted color so they stand out

### Step 4: Validate and Deliver

After generating the .docx:

1. Run `python scripts/office/validate.py <file>` to validate
2. If validation fails, unpack, fix XML, and repack per the docx skill instructions
3. Copy to `/mnt/user-data/outputs/` and present to the user

## Tips for Quality

- Lead with the Executive Summary — it's the most-read section. Make it compelling even with limited info.
- Use concrete numbers wherever possible (market sizes, projections, timelines).
- Keep language professional but accessible — avoid jargon walls.
- The competitor comparison table is high-impact; include it even if you need to use placeholder competitors.
- Financial projections table should have clear year-over-year columns (Year 1 through Year 3 or 5).
- If the user is at the idea stage, emphasize the opportunity and vision. If they have traction, emphasize metrics and growth.

## Example Test Prompts

1. "Create a business plan for a SaaS platform that helps restaurants manage food waste. We're pre-revenue, based in Mumbai, looking to raise $500K."
2. "I need a business plan for my freelance graphic design studio. I've been operating for 2 years with $120K annual revenue."
3. "Help me write a business plan for an AI-powered tutoring app targeting K-12 students in India."
