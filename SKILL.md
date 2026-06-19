---
name: data-analysis
description: Use this skill when the user needs help scoping an analysis, writing or repairing SQL, inspecting dataset quality, choosing charts or tables, prototyping a focused dashboard, or pressure-testing analysis before sharing.
---

# Data Analysis

## When to use this skill

Use this skill when the request is about turning a business question into a grounded analysis deliverable.

Typical triggers:
- the question is still vague and needs a clear analysis plan
- the user needs SQL or query repair
- the data has been extracted and needs inspection for shape, completeness, or anomalies
- the user wants help choosing the clearest chart, table, or narrative
- the same question needs a lightweight dashboard design
- an analysis, query, or dashboard needs a skeptical review before sharing

## Core workflow

1. Clarify the decision the analysis should support.
2. Identify the relevant metrics, row grain, time window, filters, and likely data sources.
3. Inspect available data, files, pasted results, screenshots, schema notes, or connected tools before committing to an analysis path.
4. Produce the most useful next deliverable for the request: analysis brief, SQL, dataset scan, visual recommendation, dashboard outline, or QA review.
5. Cite the source behind material findings when they rely on retrieved data, query results, dashboards, notebooks, or uploaded files.
6. Run a final skeptical check for grain errors, broken joins, freshness issues, denominator mistakes, reconciliation gaps, and interpretation risk.

## Request modes

### 1. Analysis intake

Use this path when the ask is vague, overloaded, or underspecified.

Deliver:
- the business decision to support
- the primary metrics and definitions in play
- the required row grain
- the likely data sources
- the analysis plan
- the most important missing inputs or risks

### 2. Query crafting

Use this path when the user needs SQL or extraction logic.

Requirements:
- make grain explicit
- name important joins and why they are safe or risky
- spell out filters, date logic, and exclusions
- include validation checks for common data-quality failures
- call out assumptions and fragility points

### 3. Dataset scan

Use this path when data is already available.

Check for:
- row counts and obvious completeness issues
- nulls, duplicates, and suspicious distributions
- schema shape and field usefulness
- freshness or date coverage issues
- the best next cuts or follow-up analyses

### 4. Visual storytelling

Use this path when the numbers are mostly settled and the main challenge is presentation.

Choose visuals based on the decision to support, not on novelty. Prefer clear tables and honest caveats over decorative charts. Separate observed facts from interpretation.

### 5. Dashboard prototype

Use this path when the same question needs a repeatable interactive surface.

Deliver:
- the key views
- required filters and defaults
- useful comparisons or drill-downs
- guardrails that prevent misuse
- a practical first-build outline

### 6. Analysis QA

Use this path before analysis is shared with stakeholders.

Review for:
- definition drift
- broken reconciliation
- hidden assumptions
- privacy or sharing risks
- weak interpretations
- claims that need more validation

## Working rules

- Start with the decision, not the chart type.
- Be explicit about row grain, exclusions, freshness, and identity caveats.
- Keep moving even without direct warehouse access by using pasted results, uploaded files, SQL snippets, screenshots, or schema descriptions.
- Distinguish clearly between verified findings, assumptions, and recommended follow-up work.
- If direct evidence is missing, say what is unknown instead of inventing results.
- Do not imply causation when the evidence only supports correlation or directional hypotheses.

## Output guidance

Match the response to the task.

Common outputs:
- analysis brief
- SQL or extraction logic
- dataset scan summary
- chart or table recommendation
- dashboard prototype outline
- QA review with concrete fixes

Lead with the answer or key finding when it is clear. Then show the supporting logic, caveats, and next steps as needed.

## If stable analysis context exists

If the workspace includes an analysis context file, use it for metric conventions, trusted sources, grain rules, privacy guidance, and delivery preferences. If that context is missing or incomplete, ask only for the missing details that materially improve the current task.
