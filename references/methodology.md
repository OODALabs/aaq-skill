# AAQ Methodology Reference

*Developed by Bob Gourley of OODA.com*

## What it measures

The AI Acceleration Quotient is a composite score (0–100) measuring the depth, breadth, and maturity of a company's AI capabilities. It captures not just whether a company uses AI, but how deeply AI is embedded in operational decision-making and how positioned the company is for the next wave of autonomous AI systems. As packaged in this skill, the AAQ is designed to use only publicly available information, which means scores are not a fully accurate representation of any company's actual capabilities. The AAQ is a framework for starting a discussion on the competitive landscape based on open information. No decisions should rely on these outputs alone.

## The three dimensions

### Dimension 1: Machine learning and advanced analytics (ML)

**Default weight: 40%**

What it covers: predictive models in production, computer vision systems, demand forecasting, yield/process optimization, recommendation engines, NLP, advanced analytics platforms, and any statistical or ML-based system that makes or supports operational decisions.

**Scoring rubric:**

| Score | Evidence required |
|-------|------------------|
| 0–20 | No public evidence of ML in operations. Company may reference "data" or "analytics" generically but no specific ML use cases documented. |
| 21–40 | One or two pilot ML projects or isolated analytics deployments. May have BI dashboards but not predictive/prescriptive capability. No quantified outcomes. |
| 41–60 | Active ML deployments in at least one business function with measurable impact. Examples: demand forecasting with stated accuracy improvement, predictive maintenance at select facilities, basic computer vision. Outcomes may be localized to specific plants or regions. |
| 61–80 | Scaled ML across multiple functions or geographies. Quantified business outcomes reported (e.g., "20% forecast error reduction," "54% fewer overdue orders"). Dedicated data science team or analytics center. Multiple ML models in production simultaneously. |
| 81–100 | ML is embedded in core enterprise operations at scale. Dozens or hundreds of production models. Computer vision, NLP, optimization, and forecasting all in production. Industry-recognized as an ML leader (vendor case studies, conference keynotes, awards). Continuous model improvement cycles documented. |

### Dimension 2: Generative AI (GenAI)

**Default weight: 35%**

What it covers: large language model-powered tools (copilots, chatbots, content generators), custom model fine-tuning on proprietary data, AI-assisted coding, knowledge management systems, and any application of foundation models (text, image, code, multimodal).

**Scoring rubric:**

| Score | Evidence required |
|-------|------------------|
| 0–20 | No public evidence of GenAI adoption. May have general statements about "exploring AI" but nothing specific to LLMs or foundation models. |
| 21–40 | Pilot GenAI deployment — typically a generic chatbot, limited Copilot rollout, or single-department trial. Off-the-shelf tools without customization. Early stage with "hopeful" language about future expansion. |
| 41–60 | GenAI deployed across multiple departments for productivity (email, content, analysis). May have a dedicated AI/emerging technology lead. Still primarily using vendor defaults (e.g., standard M365 Copilot) without significant customization on proprietary data. |
| 61–80 | Enterprise-wide GenAI deployment with customization. Custom-tuned models on proprietary data (e.g., Copilot Tuning, Azure AI Foundry, fine-tuned LLMs). GenAI integrated into specific business workflows (not just general productivity). Multiple GenAI applications in production. |
| 81–100 | GenAI deeply embedded in operations. Custom AI copilots/assistants for domain-specific tasks. Multiple foundation model applications (text, vision, code). Enterprise-wide governance framework for responsible AI. Recognized externally for GenAI innovation (press coverage, partnerships with AI providers). |

### Dimension 3: Agentic AI readiness

**Default weight: 25%**

What it covers: autonomous decision systems, closed-loop operations (AI takes action without human approval), digital twins that simulate AND act, AI agents executing multi-step workflows, edge computing for real-time autonomous decisions, and the data infrastructure and governance maturity required to support autonomous AI.

**Scoring rubric:**

| Score | Evidence required |
|-------|------------------|
| 0–20 | No autonomous AI systems. Data infrastructure is fragmented (multiple ERPs, spreadsheet-based planning, siloed data). Organizational readiness for autonomous AI is low. |
| 21–40 | Some automated workflows exist but are rules-based, not AI-driven. Data infrastructure modernization may be planned or in early stages. Basic IoT sensor deployment without closed-loop action. |
| 41–60 | Partial closed-loop systems in specific domains (e.g., automated quality rejection via CV, predictive maintenance triggering work orders). Cloud migration largely complete. Data platform supports ML model deployment. ERP modernization underway or recently completed. |
| 61–80 | Multiple closed-loop AI systems in production. Digital twins with simulation and optimization. Modern data platform (unified ERP, cloud-native, real-time data pipelines). Edge computing deployed for time-sensitive decisions. AI governance framework in place. Architectural readiness for full agentic AI. |
| 81–100 | Autonomous AI agents operating across enterprise functions. Real-time decision systems at scale (thousands of edge nodes, automated inventory/pricing/routing). AI systems that plan, execute, and self-correct multi-step workflows. Industry-leading data infrastructure (hybrid cloud, ML platforms, unified data fabric). |

## Calculation

```
Final AAQ = (ML score x ML weight) + (GenAI score x GenAI weight) + (Agentic score x Agentic weight)
```

Round to nearest integer.

## Industry-adjusted weights

When the user selects industry-adjusted weights, propose adjustments based on these guidelines:

| Industry characteristic | Adjustment |
|------------------------|------------|
| Industry where autonomous systems are mature (finance, logistics, energy) | Increase Agentic to 30–35%, reduce ML to 35% |
| Industry where GenAI is the primary AI application (media, marketing, legal) | Increase GenAI to 40%, reduce ML to 35% |
| Industry that is early in AI adoption overall (agriculture, construction, mining) | Increase ML to 45%, reduce Agentic to 20% |
| Industry with strong regulatory requirements for AI governance (healthcare, pharma) | Increase Agentic to 30% (governance maturity matters more) |
| Industry where traditional analytics dominates (manufacturing, CPG, food) | Keep standard weights — they were designed for this profile |

Always present proposed weights to the user with rationale and wait for approval.

## Score interpretation tiers

| Tier | Score | Label | Meaning |
|------|-------|-------|---------|
| 5 | 81–100 | AI-Native | AI embedded in core enterprise decision-making at scale |
| 4 | 61–80 | AI-Accelerating | Multiple scaled AI systems, expanding GenAI, early agentic |
| 3 | 41–60 | AI-Adopting | Active ML deployments, GenAI exploration, infrastructure in transition |
| 2 | 21–40 | AI-Emerging | Localized analytics, isolated pilots, foundational gaps |
| 1 | 0–20 | AI-Nascent | No publicly visible AI capabilities |

---

## License

Copyright (c) 2026 Bob Gourley / OODA LLC (ooda.com). All rights reserved. "AI Acceleration Quotient" and "AAQ" are trademarks of OODA LLC. Licensed under CC BY-NC-ND 4.0 — https://creativecommons.org/licenses/by-nc-nd/4.0/

