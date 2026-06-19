# Analysis Lanes

The skills in this plugin refer to analysis lanes instead of naming one required stack.

## Lane mapping

| Lane | Placeholder | Included defaults | Other options | Use it for |
| --- | --- | --- | --- | --- |
| Structured records | `[[structured_data]]` | Airtable | Snowflake, BigQuery, Databricks, Redshift, PostgreSQL, MySQL | Querying tables, exploring schemas, and producing result sets |
| Notebook lab | `[[notebook_lab]]` | Hex | Jupyter, Deepnote, Observable | Iteration, reusable code, and richer exploratory work |
| Behavior signals | `[[behavior_signals]]` | Amplitude | Mixpanel, Heap | Product event trends and funnel questions |
| Sheet workspace | `[[spreadsheet_workspace]]` | — | Google Drive, Excel | Small exports, manual QA, and stakeholder-friendly tables |
| Presentation surface | `[[presentation_surface]]` | — | Google Drive, Looker, Tableau | Final charts, dashboards, and share-ready narratives |
| Planning tracker | `[[planning_tracker]]` | Atlassian, Linear, Asana | Jira | Analysis requests, owners, deadlines, and dependencies |
| Data operations | `[[operations_logs]]` | — | Airflow, Dagster, Prefect, dbt | Data pipeline freshness, model ownership, lineage, and data outage context |

## Usage rules

- Do not assume warehouse access. Skills must work from pasted query results and uploaded files.
- Ask for the row grain when it matters; many analysis mistakes are really grain mistakes.
- When freshness is uncertain, check `[[operations_logs]]` or state the uncertainty clearly.
- The goal is trustworthy analysis, not maximal tooling.
