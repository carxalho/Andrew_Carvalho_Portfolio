# Sony MQM Dashboard Automation

## Objective
Automate and enhance monthly MQM scorecard reporting for Sony.

## Approach
- Built an SSIS pipeline to ingest and transform manually submitted Excel scorecards.
- Applied data type validation, deduplication, and computed column logic using CTEs in SQL.
- Created two Sisense dashboards:
  - Summary Dashboard: Aggregated metrics (e.g., total word count, average score, error types).
  - Trend Dashboard: Analysed translation KPIs across language pairs (e.g., pass/fail rates, accuracy).

## Tools Used
SSIS, SQL Server, Sisense, Excel

## Impact
Reduced manual processing time, improved data accuracy, and enabled Sony to monitor translation quality trends across languages more effectively.
