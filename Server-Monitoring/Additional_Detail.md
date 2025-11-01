## 🖥️ Server Monitoring & Job Analytics – Proactive Infrastructure Intelligence

### Overview
As the primary data infrastructure relied on an on-premises physical server, I identified a critical need for visibility into server health, database growth, and ETL job performance. I designed and implemented a comprehensive monitoring solution using SQL Server metadata views, star-schema modelling, and automated alerting to prevent outages and improve operational reliability.

### Business Challenge
The server hosted multiple databases supporting ETL pipelines and reporting layers. However, there was no existing solution to monitor:
- Database size and growth trends
- Table and column counts
- Job execution schedules, durations, and failures

This lack of visibility posed risks of server crashes, delayed reporting, and inefficient resource usage.

### Approach & Execution

#### 🔹 Metadata Extraction & Modelling
- Leveraged INFORMATION_SCHEMA and INFORMATION_DATABASE views in SSMS to extract metadata.
- Created five analytics tables using a star-schema architecture:
  - One fact table containing database identifiers and quantitative metrics.
  - Three dimension tables for row counts, column counts, and size in GB.
  - Two additional dimension tables for job history and most recent job sync.
- Used Windows Functions (e.g. DENSE_RANK) to isolate the latest sync data and avoid duplication.

#### 🔹 Dashboard Development
- Built a server monitoring dashboard to track:
  - Row/column counts
  - Database size distribution
  - Growth trends and threshold alerts

- Developed a job analytics dashboard to report:
  - Job schedules, execution counts, failure rates
  - Duration comparisons across daily, weekly, monthly, and all-time averages
  - Highlighted longest-running and most frequently failed jobs (30–90 day windows)

#### 🔹 Alerting & Automation
- Implemented triggers to notify when:
  - Server capacity exceeded 90% (by size, row, or column count)
  - Jobs failed or exceeded 200% of their average run time

### Tools & Technologies
- SQL Server (SSMS) – Metadata extraction and modelling
- T-SQL – Star-schema design and logic
- Windows Functions – Ranking and filtering
- Sisense – Dashboard development and alerting

### Impact
- Prevented server crashes by proactively identifying capacity risks.
- Reduced job failures and improved response times to incidents.
- Increased accountability among job owners through transparent reporting.
- Enhanced overall server performance and reliability, supporting uninterrupted data operations.
