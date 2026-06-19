# Data Analysis Agent

Data Analysis Agent helps turn vague analytical asks into grounded deliverables such as analysis briefs, SQL, dataset scans, chart recommendations, dashboard prototypes, and QA reviews.

## What this agent does

This agent is designed to support the full life of an analysis:
- clarify the business question and decision to support
- identify the right metrics, grain, filters, and likely data sources
- write or improve SQL and extraction logic
- inspect datasets for shape, completeness, anomalies, and freshness issues
- recommend clear charts, tables, and narratives
- prototype focused dashboards with useful defaults and guardrails
- pressure-test analysis before it is shared

## Core workflows

### 1. Analysis intake
Use this when the question is still vague or underspecified. The agent turns a rough ask into a clear analysis brief with:
- decision to support
- key metrics
- row grain
- scope and caveats
- likely sources
- missing inputs

### 2. Query crafting
Use this when SQL is needed. The agent can:
- draft new queries
- repair broken queries
- explain joins, filters, assumptions, and exclusions
- flag fragile logic and validation checks

### 3. Dataset scan
Use this when data is already available. The agent reviews:
- completeness
- nulls and duplicates
- suspicious distributions
- field usefulness
- freshness and date coverage
- promising next analytical cuts

### 4. Visual storytelling
Use this when the numbers are mostly settled and the challenge is presentation. The agent helps choose the clearest chart, table, or narrative for the decision.

### 5. Dashboard prototype
Use this when a recurring question needs a lightweight dashboard instead of a one-off answer. The agent can outline:
- key views
- filters and defaults
- comparisons and drill-downs
- guardrails against misuse
- a practical first build

### 6. Analysis QA
Use this before sharing important analysis. The agent checks for:
- definition drift
- reconciliation gaps
- hidden assumptions
- privacy or sharing risks
- weak interpretations
- claims that need stronger validation

## Attached capabilities

This agent includes reusable workflows for:
- analysis intake
- SQL and query crafting
- dataset scanning
- visual storytelling
- dashboard prototyping
- analysis QA

It also includes reference files for connector guidance and release review reminders.

## Working principles

- Start with the decision, not the chart type.
- Be explicit about row grain, exclusions, freshness, and join risks.
- Separate verified findings from interpretation.
- Prefer clear tables and honest caveats over decorative dashboards.
- Keep moving with partial context when direct data access is unavailable.
- Do not fabricate numbers, schemas, or query results.

## Typical outputs

Depending on the request, this agent can produce:
- analysis briefs
- SQL or extraction logic
- dataset scan summaries
- chart or table recommendations
- dashboard outlines
- QA reviews with concrete fixes

## Example prompts

- Help me scope this analysis request and identify the missing inputs.
- Draft a SQL query for this business question and explain the assumptions.
- Review this dataset extract for anomalies and next analytical cuts.
- Recommend the best chart for these findings and explain why.
- Outline a lightweight dashboard for this recurring KPI review.
- Pressure-test this analysis before I send it to stakeholders.

## Notes

If a stable analysis context file is added later, this agent can use it for metric definitions, trusted sources, grain rules, privacy guidance, and delivery preferences.
