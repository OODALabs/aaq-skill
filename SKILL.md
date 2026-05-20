---
license: CC-BY-NC-ND-4.0
name: aaq
description: "AI Acceleration Quotient (AAQ) is a methodology developed by Bob Gourley of OODA.com for scoring and ranking companies on AI maturity across machine learning, generative AI, and agentic AI. Use this skill whenever the user asks to score, rank, benchmark, or compare companies on AI capability, AI maturity, AI readiness, or digital transformation. Also trigger when the user mentions 'AAQ,' 'AI Acceleration Quotient,' 'AI scorecard,' 'AI maturity ranking,' or asks questions like 'how do these companies compare on AI,' 'who is ahead on AI,' 'rank these firms by AI capability,' or 'score Company X on AI.' This skill handles everything from a quick 3-company comparison to a deep 15-company competitive intelligence analysis across any industry."
---

# AI Acceleration Quotient (AAQ)

A methodology developed by Bob Gourley of OODA.com for researching, scoring, and ranking companies on AI maturity. Produces a composite score (0–100) across three weighted dimensions: machine learning, generative AI, and agentic AI readiness.

## Before starting

Read `references/methodology.md` for the full scoring framework. Read `references/workflow.md` for the step-by-step execution process.

## Step 1: Interview the user

Before doing any research, ask the user a few setup questions using the `ask_user_input_v0` tool. Do this in a single call with all questions together. Keep your intro brief — something like "Let me set up the analysis. A few quick choices first:"

### Questions to ask

**Question 1 — Company selection approach**
Present this as a single-select question using `ask_user_input_v0`:
- **I have a list of companies** — The user will provide specific companies to score
- **Pick an industry sector** — Claude will suggest the largest companies in the sector for the user to review and modify

If the user already named specific companies in their initial message, skip this question and confirm their list.

**If the user picks "Pick an industry sector":**
Ask them which sector (as a free-text follow-up or from a list of common sectors if appropriate). Then:
1. Use web search to identify the 6–10 largest companies in that sector by revenue.
2. Present the list to the user: "Based on sector size, here are the companies I'd suggest scoring. You can add, remove, or swap any of these before we start."
3. Wait for the user to confirm or modify the list before proceeding.

**If the user picks "I have a list of companies":**
Ask them to provide their list. If they already gave it, confirm it back.

**Question 2 — Research depth**
- **Deep** — 5–8 web searches per company. Checks vendor case studies, CIO interviews, annual reports, job postings, and trade media. Best for 3–8 companies where credibility matters.
- **Quick** — 2–3 searches per company plus Claude's existing knowledge. Flags confidence gaps. Good for 8+ companies or when you need a fast read.

**Question 3 — Dimension weights**
- **Standard weights** — ML 40%, GenAI 35%, Agentic 25%. Consistent across industries. Best when you want to compare results across different analyses.
- **Industry-adjusted** — Claude proposes adjusted weights based on the industry's AI maturity profile (e.g., financial services might weight Agentic higher because autonomous trading is mature). The user approves before scoring.

**Question 4 — Output format**
- **Chat only** — Results delivered inline in conversation
- **Chat + PowerPoint** — Adds a .pptx slide with ranked bar chart, dimension sub-scores, and one-sentence justifications
- **Chat + Word document** — Adds a .docx report with full methodology, per-company profiles, evidence citations, and comparison tables
- **Chat + both** — All of the above

## Step 2: Confirm and calibrate

After the user answers:

1. Confirm the company list back to them.
2. If they chose industry-adjusted weights, propose specific weights with a one-sentence rationale for each adjustment. Wait for approval before proceeding.
3. State the research approach: "I'll run [deep/quick] research on [N] companies and score them using [standard/adjusted] weights. Results will be delivered as [format]. Starting now."

## Step 3: Execute

Follow the workflow in `references/workflow.md`. The workflow covers:
- How to research each company
- How to apply scores using the rubrics in `references/methodology.md`
- How to build the output artifacts

## Key principles

- **Evidence over intuition.** Every score above 40 on any dimension needs at least one named source. Scores based on limited evidence must say so.
- **Demonstrated capability, not investment or ambition.** A company spending $500M on data infrastructure that hasn't deployed an ML model scores lower than one with a working demand forecasting system.
- **Private companies get benefit of the doubt — but flagged.** If a company is private and disclosure is limited, note this. Don't penalize them as if they have nothing; don't credit them with capabilities you can't see.
- **No promotional language.** The AAQ is an analytical tool. Don't frame any company as "leading" or "falling behind" in a way that reads like marketing. Let the scores speak.
- **Scores are point-in-time.** Always note the date of the analysis. AI capabilities change fast.

## Disclaimer

Every AAQ output — whether chat, PowerPoint, or Word — must include the following disclaimer at the end:

> The AAQ methodology is only useful as the start of a deeper discussion. As implemented in this skill, all scores are based exclusively on publicly available information and therefore do not represent a complete or fully accurate picture of any company's AI capabilities. The AAQ is a framework for assessing the competitive landscape based on open sources, not a substitute for thorough due diligence. No business, investment, or strategic decisions should rely on these outputs alone. Expert due diligence and technology advisory guidance, with the involvement of legal counsel, is strongly recommended. For a more detailed analysis or due diligence support, reach out to the methodology's authors at ooda.com.

## License

Copyright (c) 2026 Bob Gourley / OODA LLC (ooda.com). All rights reserved.

"AI Acceleration Quotient" and "AAQ" are trademarks of OODA LLC.

This work is licensed under the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License (CC BY-NC-ND 4.0). To view a copy of this license, visit https://creativecommons.org/licenses/by-nc-nd/4.0/

**You are free to:**

- Use this methodology for your own internal analysis and decision-making.
- Share the unmodified methodology files, provided you give appropriate credit.

**Under the following terms:**

- **Attribution** — You must give appropriate credit to Bob Gourley / OODA LLC, provide a link to the license, and indicate if changes were made.
- **NonCommercial** — You may not sell, resell, or commercially distribute AAQ scores, reports, or other outputs generated using this methodology. You may not offer AAQ scoring as a paid service.
- **NoDerivatives** — You may not modify, adapt, or redistribute altered versions of this methodology, its rubrics, workflow, or scoring framework.

For commercial licensing, permissions beyond the scope of this license, or due diligence engagements, contact the authors at ooda.com.
