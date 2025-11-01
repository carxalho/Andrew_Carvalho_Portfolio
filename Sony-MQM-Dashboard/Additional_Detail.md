## 🗂️ Sony MQM Dashboard Automation – Quality Monitoring at Scale

### Overview
Sony required a bespoke dashboard solution to streamline their monthly MQM (Managed Quality Metrics) scorecard review process. Previously, this was a manual, Excel-based workflow involving multiple files and manual aggregation. I led the automation and dashboard development to transform this into a scalable, repeatable BI process using SSIS, SQL Server, and Sisense.

### Business Challenge
The manual review of MQM scorecards was time-consuming, error-prone, and lacked visibility across language pairs and quality indicators. Sony needed a centralised, automated solution to ingest, transform, and visualise this data for operational and strategic insights.

### Approach & Execution

#### 🔹 Data Ingestion & Transformation
- Designed and implemented an SSIS pipeline to ingest monthly Excel scorecards delivered as individual files.
- Applied robust data validation:
  - Ensured correct data types and converted where necessary.
  - Removed duplicate records caused by manual entry.
  - Calculated derived columns required for analysis.
- Used Common Table Expressions (CTEs) to improve script readability and maintainability for future enhancements.
- Final output tables were created in SQL Server Management Studio (SSMS) and served as the data source for Sisense.

#### 🔹 Dashboard Development in Sisense
Delivered two dashboards based on Sony’s Statement of Work:

1. **Summary Dashboard**  
   - Key metrics: total word count, number of forms/projects, average words per form, average final score, precision ratio, pass/fail counts.  
   - Error analysis: count and type of quality indicators and translation types.

2. **Trend Dashboard**  
   - Comparative analysis across language pairs.  
   - KPIs: pass/fail rates, error rates, final scores by source and target language.  
   - Enabled Sony to assess translation efficiency and quality across linguistic combinations.

### Tools & Technologies
- SSIS – ETL automation for Excel ingestion
- SQL Server (SSMS) – Data transformation and modelling
- Sisense – Dashboard development and stakeholder reporting
- Excel – Source format and initial scorecard structure

### Impact
- Reduced manual processing time and eliminated repetitive data preparation tasks.
- Improved data accuracy and consistency across monthly reporting cycles.
- Enabled Sony to monitor translation quality trends and performance across language pairs.
- Provided stakeholders with actionable insights, supporting continuous improvement in localisation workflows.
