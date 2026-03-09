---
name: founder-finance-plan
description: >
  Create interactive, personalised personal financial plans for Indian startup founders,
  AI/SaaS founders, and early-stage entrepreneurs. Trigger for any Indian founder asking
  about personal finances, financial planning, retirement, personal runway, wealth building,
  or liquidity. Also trigger for: "founder salary", "paying myself", "MRR salary", "PPF",
  "NPS", "ELSS", "old vs new tax regime", "80C", "advance tax", "ITR filing", "ESOP
  taxation", "USD revenue", "FEMA", "cloud costs", "ARR multiples", "SaaS equity", "net
  worth", or "founder financial health". Even casual questions like "how do I manage money
  as a founder?" should trigger this. Starts with a structured interview, gives live
  suggestions with options, ends with an Excel workbook and/or Word (.docx) plan.
---

# Indian Founder Personal Finance Planning Skill — Interactive Edition

## Overview & Flow

This skill runs in **4 sequential phases**. Do NOT skip phases or jump to the document.

```
PHASE 1 → Warm intake interview (3 focused questions at a time)
PHASE 2 → Live diagnostic: show financial health scores + immediate flags
PHASE 3 → Present personalised options menu — let founder choose focus areas
PHASE 4 → Generate outputs: Excel workbook and/or Word (.docx) plan
```

The goal: feel like a knowledgeable friend who happens to be a CA + financial advisor,
not a form or a chatbot.

---

## PHASE 1: Intake Interview

### How to Run the Interview

- Ask in **batches of 2–3 questions** maximum per message. Never fire 8 questions at once.
- Use **plain conversational language** — not jargon. Say "your monthly rent + food + EMIs"
  not "monthly personal expenditure."
- **Acknowledge each answer** before asking the next batch (e.g., "Got it — ₹80K/month in
  Mumbai is pretty typical for a funded founder. A couple more things...")
- If the user has already shared some details in their opening message, extract those first
  and only ask for what's genuinely missing.
- Make it feel like a conversation, not a KYC form.
- **Detect AI/SaaS context**: If the founder mentions SaaS, AI product, MRR, ARR, cloud
  costs, USD revenue, or API inference costs — activate the AI/SaaS overlay (see below).

### AI/SaaS Founder Detection (Check Before Round 1)

If the founder's opening message mentions ANY of these, tag them as an AI/SaaS founder
and add AI/SaaS-specific questions in Round 3 plus the SaaS module in the options menu:

- Business model keywords: SaaS, subscription, API product, usage-based, AI product, LLM app
- Revenue keywords: MRR, ARR, USD revenue, Stripe, Paddle, LemonSqueezy, international customers
- Cost keywords: AWS, GCP, Azure, OpenAI API, Anthropic API, GPU, inference cost, cloud bill
- Structure keywords: Stripe Atlas, Delaware C-Corp, Cayman, ODI (Overseas Direct Investment),
  FEMA compliance, Deel, Remote.com, global payroll, flip structure
- Valuation keywords: ARR multiple, SaaS valuation, Rule of 40, NDR, churn

### Round 1 — The Basics (Ask First)

Ask these 3 things together:

> "To build your plan, let me start with a few basics:
>
> 1. How old are you, and which city are you based in?
> 2. What's your current monthly take-home from the startup (after tax)? If you're not
>    paying yourself yet, just say ₹0.
> 3. What does your monthly personal spending look like — roughly? (rent, food, EMIs,
>    subscriptions — ballpark is fine)"

### Round 2 — Savings & Safety Net (Ask After Round 1)

> "Thanks. A few more:
>
> 4. How much do you have in savings right now — in your personal bank account, FDs,
>    or any liquid investments? (Keep startup's bank account separate from this)
> 5. Do you have any existing investments — PPF, mutual fund SIPs, EPF from a prior job,
>    NPS, or anything else? Rough numbers are fine.
> 6. Any loans or EMIs? (home loan, car loan, education loan, or credit card outstanding)"

### Round 3 — Startup & Equity Context (Ask After Round 2)

> "Almost there:
>
> 7. What stage is your startup at — bootstrapped / seed funded / Series A or beyond?
>    And roughly what % equity do you hold?
> 8. Are you on the Old Tax Regime or New Tax Regime — or not sure yet?
> 9. Do you have dependents — spouse, kids, or parents who rely on your income?"

**If AI/SaaS founder detected — add these to Round 3:**

> "A few SaaS/AI-specific questions too:
>
> 10. What's your current MRR (Monthly Recurring Revenue)? Even a rough number helps.
> 11. Is your revenue primarily in INR or USD (or mixed)? If USD, how are you receiving
>     it — via Stripe to an Indian account, or through a foreign entity?
> 12. What does your monthly cloud/infrastructure bill look like? (AWS, GCP, OpenAI API,
>     etc.) — this affects startup runway which directly affects your personal runway.
> 13. Do you have a foreign holding structure — Delaware C-Corp, Stripe Atlas, Cayman?"


### Optional Round 4 — Only if Needed for Completeness

Ask these only if the answers above leave gaps:

- "Do you have health insurance in your name right now? (Not the startup's group cover —
  a personal policy you'd keep even if the startup shut down)"
- "Do you have a term life insurance policy?"
- "Are you registered for GST or drawing income as professional fees rather than salary?"
- "Any ESOPs or stock options granted to you from the startup?"
- "What's the biggest financial worry on your mind right now?"

---

## PHASE 2: Live Diagnostic

After collecting enough information (at minimum: age, city, take-home, burn, savings),
**immediately show a financial health snapshot** — before asking for more or building
the document. This gives instant value and builds trust.

### Diagnostic Format

Present this as a clean scorecard in the chat (use a table or clear structure):

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  📊 YOUR FINANCIAL HEALTH SNAPSHOT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Monthly Take-home     ₹[X]
  Monthly Burn          ₹[Y]
  Monthly Surplus       ₹[X-Y]   [🔴 Deficit / 🟡 Tight / ✅ Positive]

  Personal Runway       [N] months   [🔴 <6 / 🟡 6-12 / ✅ >12]
  Savings Rate          [Z]%         [🔴 <10% / 🟡 10-20% / ✅ >20%]
  Emergency Fund        ₹[savings] vs ₹[burn×6] target  [🔴/🟡/✅]
  EMI-to-Income         [EMI/income]%  [🔴 >40% / 🟡 25-40% / ✅ <25%]

  Tax Regime            Old / New / Unknown
  Insurance Gap         Health: [✅ Covered / 🔴 Gap] | Term: [✅/🔴]
  Retirement Savings    [✅ Active / 🟡 Stalled / 🔴 None]

  ⚡ TOP 3 IMMEDIATE FLAGS:
  1. [Most urgent issue — e.g., "Emergency fund covers only 3 months — critical gap"]
  2. [Second — e.g., "No health insurance post leaving corporate job"]
  3. [Third — e.g., "80CCD(1B) NPS benefit of ₹50,000 deduction unused"]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

After showing the diagnostic, make one brief observation in plain English:
> "Your runway is solid at 18 months, which gives you breathing room — but the bigger
> issue is that your retirement savings are completely stalled and every month of delay
> is expensive given compounding. Let's fix that."

Then move to Phase 3.

---

## PHASE 3: Options Menu — Let Founder Choose

After the diagnostic, present a **personalised options menu**. The founder picks what
they want to go deep on. This makes the plan feel built FOR them, not generic.

### Options Menu Format

```
Based on your situation, here's what I can help you with. Tell me which areas matter
most to you right now — pick 1, a few, or all of them:

  A) 💰 Cash Flow Fix
     Optimise your monthly cash flow, extend personal runway,
     and figure out the right founder salary to draw.

  B) 🧾 Tax Planning
     Old vs New regime decision (with your actual numbers),
     which deductions to claim, and advance tax calendar.

  C) 🛡️ Insurance Audit
     Check your health + term cover gaps and what to buy first.

  D) 📈 Investment Roadmap
     Where to invest your surplus — PPF, NPS, ELSS, SIPs —
     in priority order for your specific situation.

  E) 🏦 Retirement Planning
     How much corpus you'll need, where you stand today,
     and a step-by-step catch-up plan.

  F) 📊 ESOP / Equity Planning
     How to think about your startup equity, ESOP tax
     implications, and what to do on a liquidity event.

  G) 🤖 AI/SaaS Finance Module  [shown only for AI/SaaS founders]
     MRR-to-salary optimisation, USD revenue & FEMA rules, cloud
     cost volatility impact on personal runway, ARR-multiple equity
     valuation, and global payroll tax implications.

  H) 📊 Interactive Excel Workbook
     Generate a live, formula-driven Excel file you can update
     yourself — 9 sheets: Dashboard, Inputs, Cash Flow, Tax Planner,
     Investment Tracker, Retirement Planner, ESOP Modeller,
     Insurance Audit, and 90-Day Action Plan.

  I) 📄 Full Financial Plan (Word Document)
     Generate a complete, structured personal finance document
     covering everything above — ready to share with your CA.

  J) 📦 Both — Excel + Word Document
```

Wait for the founder's response. Then:
- **If they pick 1–2 areas**: Go deep on those in the conversation with specific numbers,
  options, and trade-offs. Then offer to generate the full document.
- **If they pick G or "all"**: Go directly to Phase 4 (document generation).
- **If they seem unsure**: Recommend starting with their top 2 flagged issues from Phase 2.

---

## PHASE 3B: Deep-Dive Modules (Conversational Suggestions)

When a founder picks an area, go deep with **specific options and trade-offs** — not
generic advice. Use the frameworks below for each module.

---

### Module A: Cash Flow Fix

Show the monthly cash flow table with their numbers. Then:

1. **Calculate and name the problem precisely:**
   - "You have a ₹23,000/month deficit. At current pace, your personal savings run out
     in 14 months. Here's how you could fix it:"

2. **Present concrete options** (always give multiple paths):

   > **Option 1 — Increase Founder Salary**
   > Draw ₹[burn + 20% buffer] instead of current ₹[X].
   > Impact: Deficit eliminated. Risk: Startup cash burn increases by ₹[difference]/month.
   > Feasible if: Company has 12+ months of runway.
   >
   > **Option 2 — Expense Reduction**
   > Largest reducible expenses from your profile: [list top 2-3 with specific ₹ amounts]
   > E.g., "Moving from Bandra to Andheri saves ₹15,000–20,000/month in rent alone."
   >
   > **Option 3 — Part-time Consulting Income**
   > 2 days/month consulting at your prior seniority level = ₹30,000–80,000/month additional
   > (many founders do this without conflict — check your SHA/SHA for IP restrictions).
   >
   > **Option 4 — Emergency Fund Extension Strategy**
   > Move current savings from savings account (3.5%) to liquid MF (6.5–7%).
   > On ₹[savings], this saves ₹[difference] per year — ₹[amount]/month effectively.

3. Ask: "Which of these feels most doable? I'll run the specific numbers for your choice."

---

### Module B: Tax Planning

Do the actual Old vs New Regime calculation with THEIR numbers:

```
YOUR PERSONALISED TAX COMPARISON (FY 2024-25)

Gross Annual Income: ₹[X]

OLD REGIME                          NEW REGIME
─────────────────────────────       ─────────────────────────────
Gross Income         ₹[X]           Gross Income         ₹[X]
Standard Deduction   -₹50,000       Standard Deduction   -₹75,000
HRA Exemption        -₹[Y]          (No other deductions)
80C (PPF + ELSS)    -₹1,50,000
80D (Health ins.)   -₹[Z]
NPS 80CCD(1B)       -₹50,000
Home Loan Interest  -₹[W]
─────────────────────────────       ─────────────────────────────
Taxable Income       ₹[A]           Taxable Income       ₹[B]
Tax Payable          ₹[T1]          Tax Payable          ₹[T2]
─────────────────────────────       ─────────────────────────────
VERDICT: [Old/New] saves ₹[difference] this year → Recommend [Old/New]
```

Then flag specific deduction opportunities they may be missing:
- "You mentioned you have parents — are they over 60? If yes, their health insurance
  premium gives you ₹50,000 in 80D deduction instead of ₹25,000. That's ₹7,500–15,600
  extra tax saved depending on your bracket."
- "You haven't started NPS yet. ₹50,000/year in NPS Tier 1 saves you ₹15,600 in tax
  (if in 30% bracket) and builds retirement corpus simultaneously."

Present the advance tax calendar with THEIR estimated numbers:

> "Based on estimated annual tax of ₹[T], here are your advance tax installments:
> - By 15 June: ₹[15% of T]
> - By 15 Sep: ₹[30% more = 45% cumulative]
> - By 15 Dec: ₹[30% more = 75% cumulative]
> - By 15 Mar: ₹[25% remaining]
> Mark these in your calendar NOW — 234B/234C interest applies if you miss them."

---

### Module C: Insurance Audit

Run through their current coverage and flag gaps:

```
YOUR INSURANCE AUDIT

Health Insurance
  Required:  ₹[10-25L based on city and family size]
  Current:   [What they mentioned / "Unknown"]
  Gap:       [Yes/No — specific amount]
  Action:    [Buy X from Y, costs ~₹Z/yr, deductible under 80D]

Term Life Insurance
  Required:  ₹[10-15× annual income or ₹1Cr min if dependents]
  Current:   [What they mentioned]
  Gap:       [Yes/No]
  Action:    [Buy X online, costs ~₹Y/yr at age Z]

Personal Accident / Critical Illness
  Status:    [Usually missing for founders]
  Recommend: [Yes/No based on dependents and risk profile]
```

Give specific product names and estimated premiums. Always recommend online direct purchase.

Explain the corporate cover trap:
> "If you were covered under your previous employer's group health plan, that cover
> lapsed the day you quit. Any pre-existing conditions you develop NOW won't be covered
> by a new individual policy for 2–4 years (waiting period). Buy individual cover today
> while you're healthy — not after you need it."

---

### Module D: Investment Roadmap

Show the Indian Founder Financial Stack with THEIR specific numbers plugged in:

```
YOUR PERSONALISED INVESTMENT STACK

You have ₹[surplus]/month to invest. Here's the priority order:

🔴 STEP 1 — EMERGENCY FUND (Complete First)
   Target:  ₹[burn × 6] = ₹[X]
   Current: ₹[Y]
   Gap:     ₹[X-Y]
   Action:  Put ₹[monthly amount] into [liquid MF name] until gap is closed
   Time:    ~[N] months at current surplus

🟡 STEP 2 — TAX SHIELD (Once Step 1 is done)
   PPF:     ₹[12,500/month or ₹1.5L/yr lump sum before 5 April]
             → Saves ₹[tax saved] in tax + builds ₹[FV at maturity] by age [X]
   NPS:     ₹[4,167/month = ₹50,000/yr]
             → Extra ₹[15,600 at 30% bracket] tax saved; can't touch until 60
   ELSS:    ₹[remaining 80C room ÷ 12]/month SIP
             → 3-year lock-in, ~12-14% historical CAGR

🟢 STEP 3 — WEALTH BUILDING (Once Step 2 is running)
   Nifty 50 Index SIP: ₹[X]/month (UTI or Nippon, direct plan, ~0.1% expense)
   Flexicap SIP:       ₹[Y]/month (Parag Parikh, direct plan)
   Suggested split: 60% index / 40% flexicap

   Projection at [X]% monthly for [N] years: ₹[FV]
```

For each instrument, offer to explain more:
> "Want me to walk through how to actually open a PPF account online in 10 minutes?
> Or should I show you the SIP compounding math for your specific numbers?"

---

### Module E: Retirement Planning

Run the retirement gap analysis with their numbers:

```
YOUR RETIREMENT SNAPSHOT

Age today:          [X]
Target retirement:  [60 or stated preference]
Years to retire:    [N]

Monthly lifestyle today:     ₹[burn]
Inflation-adjusted at 60:    ₹[burn × (1.06)^N] (assuming 6% inflation)
Required monthly withdrawal: ₹[above]
Target corpus (25× rule):    ₹[above × 12 × 25]

CURRENT TRAJECTORY
─────────────────────────────────────
Existing corpus:             ₹[investments today]
At 7% real return for [N]yr: ₹[FV of existing]
Monthly SIP needed to fill gap: ₹[PMT calculation]

VERDICT: You need ₹[X]/month in long-term investments to retire comfortably.
         You are currently investing ₹[Y]/month → Gap of ₹[X-Y]/month.
```

Then offer 3 paths:
> **Path 1 (Conservative)**: Increase monthly SIP by ₹[gap amount] immediately
> **Path 2 (Balanced)**: Increase salary, invest incremental amount
> **Path 3 (Equity Bet)**: Model what startup equity needs to be worth to cover gap

---

### Module F: ESOP / Equity Planning

Show the ESOP tax walkthrough if applicable:

```
YOUR ESOP SNAPSHOT

Grant: [X shares at ₹[strike price] — vesting over [N] years]
Current FMV (if known): ₹[Y] per share
Potential perquisite tax at exercise: (₹Y - ₹strike) × shares × [tax rate]%

EXERCISE TIMING OPTIONS:
Option 1 — Exercise now:
  Perquisite tax today: ₹[calculated]
  Holding period starts now; LTCG rate (unlisted, >24 months) = 20% with indexation

Option 2 — Wait until pre-IPO/secondary:
  Higher FMV → higher perquisite tax; but timing may align with liquidity
  Risk: Startup fails, options worthless

Option 3 — Exercise + immediate sell (if secondary market open):
  Perquisite tax + STCG at slab rate if held < 24 months
  But de-risks equity concentration
```

Always add:
> "Equity planning has significant tax implications — loop in a CA before exercising.
> A good CA can save you lakhs by timing the exercise correctly."

Show exit scenario table:
| Company Valuation | Your Stake (X%) | After Further Dilution | Pre-tax | Post-tax (LTCG 20%) |
|------------------|----------------|----------------------|---------|---------------------|
| ₹10 Cr | ₹Xcr | ₹Xcr | ₹Xcr | ₹Xcr |
| ₹50 Cr | ... | ... | ... | ... |
| ₹200 Cr | ... | ... | ... | ... |
| ₹0 (failure) | ₹0 | ₹0 | ₹0 | ₹0 |

---

---

### Module G: AI/SaaS Finance Module [Only for AI/SaaS Founders]

This module addresses the 6 financial patterns unique to Indian AI/SaaS founders.

---

#### G1. MRR-Based Personal Salary Optimisation

SaaS founders have a unique salary lever: MRR. Show the relationship clearly:

```
YOUR MRR → SALARY FRAMEWORK

Current MRR:           ₹[X] / $[Y]
Company Burn Rate:      ₹[Z]/month (infra + team + tools)
Startup Cash Runway:    [N] months

Recommended Founder Salary Bands:
─────────────────────────────────────────────────────────
MRR Stage          Safe Founder Salary      Rationale
─────────────────────────────────────────────────────────
MRR = ₹0           ₹0 – ₹30,000            Survival mode; use savings
MRR = ₹1–5L        ₹30,000 – ₹60,000       Cover personal burn only
MRR = ₹5–15L       ₹60,000 – ₹1,20,000     Can afford to pay yourself properly
MRR > ₹15L         Market rate (₹1.5L+)    Now build personal wealth aggressively
─────────────────────────────────────────────────────────

Rule: Founder salary should not exceed 25–30% of MRR until you reach
default alive (MRR > total monthly burn including your salary).
```

Key question to always ask: "Are you default alive?" (MRR > total monthly costs including your salary)
→ If yes: personal finances can stabilise. If no: personal burn reduction is priority.

---

#### G2. USD Revenue & FEMA / RBI Compliance

For Indian founders receiving USD revenue — this is often mishandled. Cover clearly:

**If selling to international customers from an Indian entity (LLP/Pvt Ltd):**
- Foreign remittances must come in via FIRC (Foreign Inward Remittance Certificate)
- Must be received within 9 months of export of services (FEMA guidelines)
- File softex / EDPMS returns if applicable (for software exports > $25,000)
- GST: Export of services is zero-rated (0% GST), claim refund of input GST credit
- Tax: Revenue taxed in India as normal business income; no special treatment for USD

**If using a foreign holdco (Delaware / Cayman / Singapore) with Indian subsidiary:**
- Personal salary can come from either entity — tax implications differ significantly
- Dividends from foreign holdco to Indian resident: taxed at 20% + surcharge (no indexation)
- Need CA + Company Secretary familiar with FEMA, ODI (Overseas Direct Investment) rules
- Transfer pricing documentation mandatory if transacting between related entities

**If using Stripe Atlas / foreign-only entity (no Indian entity yet):**
- All income received in India is taxable in India regardless of where earned
- FEMA violation risk if not structured properly — get a CA immediately
- LRS (Liberalised Remittance Scheme) allows Indians to invest $250,000/year abroad

**Practical USD Cash Flow Tip:**
> Keep a USD account (Federal Bank, ICICI, HDFC offer EEFC accounts for exporters).
> Convert only what you need for INR expenses — avoids repeated conversion charges (~0.5–1%).
> Monitor USD/INR monthly — a 5% INR depreciation = 5% windfall on existing USD holdings.

---

#### G3. Cloud Cost Volatility & Personal Runway Impact

AI founders have a unique risk: cloud bills can spike 5–10× overnight (viral moment,
bad query, inference cost scaling). This creates personal runway risk.

Show this framework:

```
CLOUD COST RISK TO PERSONAL RUNWAY

Average Monthly Cloud Bill:        ₹[X]
Worst-case Spike (3× average):     ₹[3X]
Startup Cash Reserves:             ₹[Y]
Months until forced salary cut:    ₹[Y] ÷ (Burn + ₹[3X] - MRR) = [N] months

PERSONAL IMPACT:
If startup cuts founder salary to ₹0, personal runway = ₹[savings] ÷ ₹[burn] = [M] months

RECOMMENDATIONS:
1. Set cloud billing alerts at 120% of average monthly spend (AWS/GCP both support this)
2. Implement rate limiting / request throttling for AI inference endpoints
3. Keep 3 months of peak cloud costs in startup's FD — ring-fenced from operating cash
4. Personally: maintain 6-month emergency fund independent of startup's health
```

Specific cost optimisation tips for AI founders (mention these):
- Use spot/preemptible instances for batch inference (60–80% cheaper)
- Cache common LLM responses — reduces OpenAI/Anthropic API calls by 20–40%
- AWS/GCP startup credits: apply for $100K–$200K in credits (Y Combinator, AWS Activate, GCP for Startups)
- Model distillation / smaller models for routine tasks vs frontier models for complex ones

---

#### G4. SaaS/AI Equity Valuation (ARR Multiples)

Generic exit modelling doesn't capture SaaS valuation. Use ARR multiples:

```
YOUR SAAS EQUITY VALUATION MODEL

Current ARR:          ₹[MRR × 12] = ₹[X]
YoY Growth Rate:      [G]%
Net Dollar Retention: [NDR]% (revenue retained + expanded from existing customers)

VALUATION RANGE (ARR Multiples — Indian/Global SaaS, 2024-25):
─────────────────────────────────────────────────────────────────
Scenario          ARR Multiple    Company Valuation    Your Stake ([E]%)
─────────────────────────────────────────────────────────────────
Conservative      3×              ₹[3X]                ₹[3X×E]
Base Case         6×              ₹[6X]                ₹[6X×E]
Optimistic        10×             ₹[10X]               ₹[10X×E]
Hypergrowth       15×+            ₹[15X+]              ₹[15X+×E]
─────────────────────────────────────────────────────────────────
All pre-tax. LTCG at 20% (unlisted, held >24 months) applies at exit.

RULE OF 40 CHECK (Growth Rate % + Profit Margin % should be ≥ 40 for premium valuation):
  Your Growth Rate:   [G]%
  Your Profit Margin: [P]%
  Rule of 40 Score:   [G+P] → [<40: below premium / ≥40: premium multiples apply]
```

Note: Indian SaaS companies selling to US/global markets often command higher multiples
than purely domestic SaaS (larger TAM, USD revenue = dollar-denominated value).

---

#### G5. Global Payroll & Tax Complexity

Many AI/SaaS founders hire globally (contractors in US, EU, team in India).
Flag these personal finance implications:

**If you have employees/contractors outside India:**
- Indian entities can pay foreign contractors via wire transfer — no special license needed
- But if you have a foreign entity paying Indian employees: FEMA PE (Permanent Establishment)
  risk — can create unexpected Indian tax liability for the foreign entity
- Deel / Remote.com / Multiplier handle compliance but add 15–20% overhead to contractor cost

**Your own compensation if you have a foreign entity:**
- Taking salary from a Delaware C-Corp as an Indian resident: taxable in India at slab rates
- Taking dividends from foreign holdco: 20% tax in India (plus DTAA relief if applicable)
- Stock options in US entity held by Indian resident: FEMA reporting required (Form OPI/ODI)
- **Get a CA with international tax experience — this is not a DIY area**

---

#### G6. SaaS-Specific 90-Day Financial Priorities

Replace generic actions with SaaS-specific ones where applicable:

| Action | SaaS Context | Priority |
|--------|-------------|----------|
| Set cloud billing alerts | Prevents bill shock → salary cut cascade | Week 1 |
| Apply for AWS/GCP startup credits | Up to $200K — reduces burn, extends personal runway | Week 2 |
| Open EEFC account (if USD revenue) | Avoid repeated forex conversion fees | Month 1 |
| Get FEMA-compliant CA | Foreign entity + Indian residency = complexity | Month 1 |
| Model "default alive" date | MRR growth vs burn — the SaaS founder's north star | Month 1 |
| Separate company cloud costs from personal | Common mistake — leads to messy ITR | Ongoing |

---

## PHASE 4: Generate Outputs

Trigger when founder selects G / H / I from the menu, or after 2+ deep-dive modules.
Offer: "Want me to generate your plan as an Excel workbook, a Word document for your CA, or both?"

### Option G — Interactive Excel Workbook

Run the bundled generator script:
```bash
python founder-finance-plan/scripts/generate_excel.py /mnt/user-data/outputs/founder_finance_plan_india.xlsx
```
Validate with recalc.py, then share via present_files.
Tell the founder: **edit only the blue/yellow cells on the Inputs sheet — everything else updates automatically.**

The workbook has 9 interconnected sheets:

| Sheet | What it does |
|-------|-------------|
| Dashboard | Auto scorecard: runway, savings rate, investment stack status, alerts |
| Inputs | All editable inputs — one place, all other sheets update |
| Cash Flow | 12-month tracker with cumulative personal cash position |
| Tax Planner | Old vs New regime side-by-side + advance tax calendar with rupee amounts |
| Investments | Layer 1-4 stack tracker + 10-year SIP compounding projection table |
| Retirement | Corpus gap analysis, monthly SIP needed, 5-milestone projection |
| ESOP Planner | Perquisite tax at exercise + exit scenario modeller (editable valuations) |
| Insurance Audit | Coverage gap checker with product recommendations and premiums |
| 90-Day Plan | Prioritised checklist with deadlines and CA/RIA flags |

### Option H — Word Document

### Pre-Generation Checklist

Before writing the document, confirm you have:
- [ ] Age, city, family situation
- [ ] Monthly take-home and monthly burn
- [ ] Savings balance
- [ ] Existing investments (even if ₹0)
- [ ] EMIs / liabilities
- [ ] Equity stake and stage
- [ ] Tax regime (or determined via Module B)
- [ ] Insurance status
- [ ] Focus areas the founder cares about most

If any critical item is missing, ask ONE final consolidating question:
> "Before I write the document, one quick check — do you have any existing PPF, NPS,
> or mutual fund investments? And do you currently have personal health insurance?"

### Document Generation

Read `/mnt/skills/public/docx/SKILL.md` BEFORE writing any code.
Read both files in `references/` — they contain instrument details and scenario templates.

All figures in ₹. Indian numbering (lakhs, crores). All analysis uses data collected
in Phases 1–3 — this is NOT a generic template, it's specific to this founder.

### Document Structure

```
1. Cover Page
   - Title: "Personal Financial Plan — [Founder Name]"
   - Subtitle: "Indian Startup Founder Edition | [Month Year]"
   - Confidential watermark

2. Executive Summary (1 page)
   - Financial health snapshot (the Phase 2 diagnostic, formatted cleanly)
   - Top 3 priority actions (specific, numbered, actionable)
   - Summary table: Take-home | Burn | Surplus | Runway | Tax Regime

3. Section 1: Cash Flow & Liquidity
   - Monthly cash flow statement (their actual numbers)
   - Runway analysis with risk flag
   - Emergency fund gap and fix plan
   - EMI health check
   - Expense optimisation opportunities (specific, ranked by ₹ impact)
   - Advance tax calendar with their estimated installment amounts

4. Section 2: Tax Planning
   - Old vs New regime comparison (their actual numbers side by side)
   - Deductions being used vs. deductions being missed
   - ITR form recommendation (ITR-1 / ITR-3 / ITR-4)
   - Advance tax schedule
   - ESOP section (if applicable)

5. Section 3: Investment Roadmap
   - Their personalised Founder Financial Stack with ₹ amounts
   - Instrument-by-instrument breakdown (PPF, NPS, ELSS, Index MFs)
   - SIP plan: fund names, amounts, platforms
   - Compounding projection table (10yr / 20yr / 30yr)

6. Section 4: Retirement Planning
   - Retirement gap analysis with their numbers
   - Current trajectory vs. required trajectory
   - Monthly investment needed to hit target
   - Path options (conservative / balanced / equity-dependent)

7. Section 5: Insurance Audit
   - Current vs. required coverage table
   - Specific gaps flagged with urgency level
   - Recommended products with estimated premiums and 80D impact

8. Section 6: ESOP & Equity Planning (include only if ESOPs or significant equity)
   - ESOP tax walkthrough
   - Exit scenario modelling table
   - Diversification triggers

9. Section 7: 90-Day Action Plan
   - Week 1 / Month 1 / Month 2 / Month 3 priorities
   - Each item: Action | Why | Time | CA/RIA needed?

10. Appendix
    - All assumptions listed
    - Indian financial year calendar
    - Recommended platforms (Zerodha Coin, Groww, ClearTax, eNPS, etc.)
    - Disclaimer
```

### Document Tone
- Peer-to-peer, practical, India-aware
- All figures in ₹ with Indian notation (₹5,00,000 not ₹500,000; "5 lakh" in prose)
- Every recommendation has a specific rupee amount, product name, and next step
- Acknowledge Indian realities: family obligations, real estate pressure, gold, LIC from parents
- Label every assumption clearly

### Output
1. Save to `/mnt/user-data/outputs/founder-financial-plan-india.docx`
2. Use `present_files` to share
3. In closing message: mention top 2 urgent actions and offer to answer follow-up questions

---

## Key Frameworks (Reference — Used Across All Modules)

### Indian Founder Financial Stack
```
🔴 Layer 1 — SURVIVAL: Emergency fund (6×burn in liquid MF) + Health + Term insurance
🟡 Layer 2 — TAX SHIELD: PPF ₹1.5L + NPS ₹50k + 80D health premium + ELSS remainder
🟢 Layer 3 — WEALTH: Nifty 50 Index SIP + Flexicap SIP (direct plan only)
🔵 Layer 4 — EQUITY: Startup equity as lottery ticket; diversify on any liquidity event
```

### Tax Regime Heuristic
```
Total deductions > ₹3.75L → Old Regime
Total deductions < ₹3.75L → New Regime
Income ≤ ₹7L → New Regime (zero tax via 87A rebate)
```

### Advance Tax Dates
15 June (15%) → 15 Sep (45%) → 15 Dec (75%) → 15 Mar (100%)

### ESOP Tax (Unlisted)
Grant: No tax | Vesting: No tax | Exercise: Perquisite at slab rate |
Sale <24mo: STCG at slab | Sale ≥24mo: LTCG 20% with indexation

### Retirement Corpus Formula
`Monthly burn × 12 × 25 × (1.06)^years_to_retirement`

### Emergency Fund Target
`Monthly burn × 6` — in liquid MF, never in startup's current account

---

## Reference Files

- `references/india-instruments.md` — All Indian investment instruments: PPF, NPS, ELSS,
  liquid MFs, SGBs, index funds — with limits, tax status, lock-in, platforms, and traps
- `references/india-founder-scenarios.md` — Three realistic INR founder archetypes with full
  cash flow tables, tax calculations, and investment recommendations

Always read BOTH before writing the document.

---

## Disclaimer (Include in Every Document)

> *This document is prepared for informational and planning purposes only. It does not
> constitute professional financial, tax, or legal advice under Indian law. Please consult
> a SEBI-registered Investment Adviser (RIA) and/or a Chartered Accountant (CA) before
> making significant financial decisions. Tax laws referenced are as per Finance Act 2024
> (FY 2024-25) and are subject to change.*
