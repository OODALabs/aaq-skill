# AI Acceleration Quotient (AAQ)

A scoring methodology for measuring how deeply AI is embedded in an organization's operations. Developed by [Bob Gourley](https://ooda.com) at [OODA LLC](https://ooda.com).

The AAQ produces a composite score from 0 to 100 across three dimensions:

- **Machine learning and advanced analytics** (default 40%) — production ML systems, predictive models, computer vision, demand forecasting, optimization
- **Generative AI adoption** (default 35%) — LLM-powered tools, copilots, custom fine-tuning, knowledge management, AI-assisted workflows
- **Agentic AI readiness** (default 25%) — autonomous decision systems, closed-loop operations, digital twins, edge computing, data infrastructure maturity

Scores place organizations into five tiers, from AI-Nascent (0-20) through AI-Native (81-100).

## What this repo contains

```
SKILL.md                    # Claude skill definition (the main entry point)
references/methodology.md   # Full scoring rubrics and dimension definitions
references/workflow.md      # Step-by-step research and scoring process
LICENSE                     # CC BY-NC-ND 4.0
```

## Using the AAQ as a Claude skill

This repo is packaged as a [Claude Project skill](https://docs.claude.com). To use it:

1. Download this repo as a ZIP (Code > Download ZIP) or clone it
2. In Claude, open a Project and go to Project Knowledge
3. Upload all four files (`SKILL.md`, `LICENSE`, `references/methodology.md`, `references/workflow.md`)
4. Start a conversation and ask Claude to score companies on AI maturity

Example prompts:
- "Score the top 8 defense contractors on AI maturity"
- "Run an AAQ analysis on Walmart, Target, and Costco"
- "Pick the largest companies in the pharmaceutical sector and benchmark them on AI"

The skill walks you through setup choices (research depth, weighting, output format) and then runs the analysis using web search to gather current public evidence.

## What the AAQ is for

The AAQ is a starting point for competitive intelligence, not a final verdict. It works from publicly available information only, which means it can't capture everything a company is doing internally. It's useful for:

- Getting a structured read on where companies stand relative to each other
- Identifying which dimension of AI (ML, GenAI, Agentic) differentiates leaders from laggards in a given industry
- Framing due diligence conversations with concrete, scored evidence
- Tracking how an industry's AI maturity shifts over time

It is not a substitute for deep due diligence. See the full disclaimer in `SKILL.md`.

## Methodology overview

Each dimension has a five-tier rubric (0-20, 21-40, 41-60, 61-80, 81-100) with specific evidence requirements at each level. Scores above 40 on any dimension need at least one named source. The methodology rewards demonstrated, deployed capability over investment announcements or aspirational statements.

Weights can be adjusted by industry. Financial services might weight Agentic higher because autonomous trading systems are mature. Media companies might weight GenAI higher. The standard weights work well for manufacturing, CPG, and most industrial sectors.

Full rubrics and scoring guidance are in [`references/methodology.md`](references/methodology.md). The research and scoring workflow is in [`references/workflow.md`](references/workflow.md).

## License

Copyright (c) 2026 Bob Gourley / OODA LLC. All rights reserved.

"AI Acceleration Quotient" and "AAQ" are trademarks of OODA LLC.

Licensed under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/). You can use this methodology for your own internal analysis and share the unmodified files with credit. You cannot sell AAQ outputs as a service or redistribute modified versions. See [`LICENSE`](LICENSE) for full terms.

For commercial licensing or due diligence engagements, contact the authors at [ooda.com](https://ooda.com).
