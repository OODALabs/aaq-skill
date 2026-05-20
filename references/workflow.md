# AAQ Workflow Reference

## Research phase

### What to search for (per company)

Research targets by priority. In "quick" mode, cover items 1–3. In "deep" mode, cover all.

1. **Company + AI/ML/data analytics** — Gets the broadest overview of public AI initiatives
2. **Company + specific AI initiative** (if known from prior knowledge) — e.g., "Walmart Luminate platform," "Nestlé SAP Joule"
3. **Company + digital transformation OR technology strategy** — Catches ERP migrations, cloud partnerships, CTO/CIO interviews
4. **Company + SAP/ERP/cloud vendor** — Identifies enterprise platform status (SAP S/4HANA, Azure, AWS, GCP)
5. **Company + vendor case study** — SAP customer story, Microsoft customer story, Google Cloud customer story, Rockwell Automation, Palantir, etc.
6. **Company + AI job postings** — Data scientist, ML engineer, AI/ML roles signal investment intent
7. **Company + computer vision OR predictive maintenance OR demand forecasting** — Domain-specific AI capabilities
8. **Company + generative AI OR copilot OR LLM** — GenAI adoption specifics

### Source quality hierarchy

Prioritize sources in this order:

1. Vendor customer case studies (SAP, Microsoft, Google Cloud, Palantir, Rockwell) — most specific, most verifiable
2. CIO/CTO interviews in trade media (CIO.com, Diginomica, TechTarget) — provides strategic context and confirms deployments
3. Corporate annual reports and investor presentations — official, boardroom-level disclosures
4. Company press releases — self-reported but citable
5. Industry trade publications (Food Engineering, Supply Chain Dive, Modern Retail) — editorial verification
6. Job postings (LinkedIn, corporate careers) — signals investment intent but not deployed capability
7. Third-party tech databases (AppsRunTheWorld, ZoomInfo, LeadIQ) — useful for ERP/vendor identification but lower reliability
8. Independent analyst publications — useful context but may involve speculation

### Research notes

- Always check if SAP has published a customer case study for the company (search: "[company] site:sap.com customer story")
- Always check if Microsoft has a customer story (search: "[company] site:microsoft.com customer story")
- For private companies, explicitly note the disclosure limitation and flag scores as lower-confidence
- Job postings indicate intent, not deployed capability — use them for the Agentic dimension (organizational readiness) but not for ML or GenAI scoring
- If a company claims "AI-powered" anything in marketing copy without specifics, that is not evidence of ML deployment

## Scoring phase

### How to assign scores

For each company, work through each dimension independently:

1. **List the evidence.** Write down every specific AI capability you found, with sources.
2. **Match to rubric.** Compare the evidence against the scoring rubric in methodology.md. Find the tier that best matches the totality of evidence.
3. **Assign a score within the tier.** A company at the low end of a tier gets the bottom of the range; one at the high end gets the top. Example: a company with one strong ML deployment but no others might score 45 (low end of 41–60), while one with three deployments and partial quantified outcomes might score 58.
4. **Write a one-sentence justification.** State the key evidence that determined the score. This sentence will appear in the output table.
5. **Write a detailed justification.** For Word document output, provide 2–3 sentences per dimension explaining the score with source citations.

### Score cross-check

After scoring all companies, do a sanity check:
- Are the relative rankings defensible? Would a knowledgeable industry observer agree with the ordering?
- Is there a company scored higher on ML than another company that clearly has more production ML systems? Fix it.
- Are private companies systematically scored lower just because of disclosure? Adjust if needed and flag.

## Output phase

### Chat output (always produced)

Present results in a clear conversational summary:
- Open with the key finding (who's on top, who's at the bottom, what the spread looks like)
- Show a ranked list with AAQ score, tier label, and dimension sub-scores for each company
- Include one-sentence justification per company
- Close with 2–3 cross-cutting observations (e.g., "GenAI adoption is nearly universal above the 60-point line," "Agentic AI is the clearest differentiator among the top three")
- Note the date of analysis and that scores reflect publicly visible evidence only
- End with the required disclaimer: "The AAQ methodology is only useful as the start of a deeper discussion. As implemented in this skill, all scores are based exclusively on publicly available information and therefore do not represent a complete or fully accurate picture of any company's AI capabilities. The AAQ is a framework for assessing the competitive landscape based on open sources, not a substitute for thorough due diligence. No business, investment, or strategic decisions should rely on these outputs alone. Expert due diligence and technology advisory guidance, with the involvement of legal counsel, is strongly recommended. For a more detailed analysis or due diligence support, reach out to the methodology's authors at ooda.com."

### PowerPoint output (when requested)

Generate a single slide per category (or a single slide if all companies are one category) using pptxgenjs. Read the pptx SKILL.md before generating.

**Slide layout:**
- Dark header band (navy) with title and subtitle
- Legend showing the three dimension colors
- Ranked rows with: rank number, company name, horizontal bar proportional to AAQ score, score value, dimension sub-scores, one-sentence justification
- Alternating row backgrounds for readability
- Source/disclaimer footer: must include "The AAQ methodology is only useful as the start of a deeper discussion. As implemented in this skill, all scores are based exclusively on publicly available information and therefore do not represent a complete or fully accurate picture of any company's AI capabilities. The AAQ is a framework for assessing the competitive landscape based on open sources, not a substitute for thorough due diligence. No business, investment, or strategic decisions should rely on these outputs alone. Expert due diligence and technology advisory guidance, with the involvement of legal counsel, is strongly recommended. For a more detailed analysis or due diligence support, reach out to the methodology's authors at ooda.com."

**Design specs:**
- Navy header: `1B3A5C`
- Bar color: `2E75B6`
- ML sub-score color: `2E75B6`
- GenAI sub-score color: `6B4C9A`
- Agentic sub-score color: `1A8A6A`
- Alternating row: `E8F0F8` / white
- Font: Arial throughout
- Company name: 12–13pt bold
- AAQ score: 14–16pt bold navy
- Justification: 9–10pt gray
- Footer: 8pt italic gray

### Word document output (when requested)

Generate a .docx file using the docx npm package. Read the docx SKILL.md before generating.

**Document structure:**
1. Title page with analysis title, date, industry/context, and source note
2. Methodology section — brief (one page) summary of the AAQ framework, three dimensions, and weights used
3. Company profiles — one section per company with: company overview (2–3 sentences), dimension-by-dimension scoring with evidence and sources, technology stack summary where known
4. Ranked comparison table — all companies with AAQ, dimension scores, tier label
5. Cross-cutting observations — 3–5 themes observed across the analysis
6. Methodology notes — limitations, source categories, date of analysis
7. Disclaimer — must include: "The AAQ methodology is only useful as the start of a deeper discussion. As implemented in this skill, all scores are based exclusively on publicly available information and therefore do not represent a complete or fully accurate picture of any company's AI capabilities. The AAQ is a framework for assessing the competitive landscape based on open sources, not a substitute for thorough due diligence. No business, investment, or strategic decisions should rely on these outputs alone. Expert due diligence and technology advisory guidance, with the involvement of legal counsel, is strongly recommended. For a more detailed analysis or due diligence support, reach out to the methodology's authors at ooda.com."

**Design specs:**
- Navy headings: `1B3A5C`
- Accent headings: `2E75B6`
- Source lines: gray italic, 9pt
- Alternating table rows: `E8F0F8` / white
- Header row: navy background, white text
- Font: Arial throughout
- Body: 11pt, headings: 16pt/13pt/11pt

---

## License

Copyright (c) 2026 Bob Gourley / OODA LLC (ooda.com). All rights reserved. "AI Acceleration Quotient" and "AAQ" are trademarks of OODA LLC. Licensed under CC BY-NC-ND 4.0 — https://creativecommons.org/licenses/by-nc-nd/4.0/

