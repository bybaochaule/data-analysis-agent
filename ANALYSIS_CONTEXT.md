# Analysis Context

Use this file to capture stable business context for the Data Analysis Agent.

## Business or team name
Example: Growth Analytics Team

## Metric glossary
- Weekly Active Users (WAU): Unique users with at least one qualifying session in the last 7 days.
- Activation Rate: Percentage of new users who complete the core activation event within 14 days of signup.
- Retention D30: Percentage of new users active 30 days after signup.
- Revenue: Net recognized revenue, excluding refunds, credits, and internal test transactions.

## Trusted sources
- `analytics.events`: Canonical product event stream for usage analysis.
- `core.users`: Source of truth for user attributes and signup date.
- `finance.revenue_daily`: Source of truth for recognized revenue.
- `growth_dashboard`: Executive KPI dashboard for cross-checking top-line metrics.
- Hex notebooks in the team workspace: Preferred place for exploratory analysis and draft modeling.

## Grain and join rules
- `analytics.events` is event-level grain; aggregate before joining to user-level summaries when possible.
- `core.users` is one row per user.
- Join revenue to users by `account_id`, not by email.
- Exclude internal employees, QA accounts, and demo workspaces from stakeholder-facing reporting.
- Watch for duplicate rows when joining events to subscription or billing tables.

## Privacy and sharing
- Do not include raw email addresses, full names, or payment identifiers in broadly shared outputs.
- Suppress or aggregate results when a segment has fewer than 10 users.
- Treat finance and people data as limited-audience unless explicitly approved for wider sharing.
- Redact customer-identifiable examples before using screenshots or copied rows.

## Delivery preferences
- Prefer concise memos for business questions and SQL snippets for analyst handoff.
- Use tables for exact comparisons and line charts for time trends.
- Keep dashboards focused on 3 to 5 core views.
- Include a short caveats section for any analysis shared with leadership.
- When assumptions are material, list them explicitly near the top.
