## 🧩 Sisense Governance Dashboards – BI Estate Visibility & Optimisation

### Overview
Upon assuming ownership of our core BI platform, Sisense, I identified a critical gap in estate visibility. There was no existing mechanism to audit dashboard usage, data model activity, or user engagement. To address this, I led the development of a custom governance framework using Jupyter notebooks, Sisense APIs, and SQL-based reporting.

### Business Challenge
The BI estate lacked transparency, making it difficult to:
- Identify unused or duplicated dashboards and data models.
- Monitor user activity and access patterns.
- Prioritise change requests based on actual usage and impact.

This hindered platform efficiency and limited the ability to scale BI operations effectively.

### Approach & Execution

#### 🔹 Data Extraction via Sisense API
- Partnered with Sisense’s Technical Account Executive to access backend metadata via API endpoints.
- Developed 11 Jupyter notebooks, each targeting a specific KPI:
  - Dashboard inventory and sharing details
  - Data model metadata and size (GB)
  - Access groups and user roles
  - Build schedules and software tenants
  - User activity and group membership
- Used Python libraries: os, json, requests, and pandas to extract and transform data.

#### 🔹 Data Modelling & Integration
- Transformed raw API data into structured tables.
- Linked datasets using SQL joins (LEFT JOINs, UNIONs) to create a unified governance model.
- Imported the final tables into Sisense as data sources.

#### 🔹 Dashboard Development
Created three governance dashboards:

1. **Dashboard Analytics**
   - Total dashboards, usage metrics (clicks, engagement), sharing access paths.

2. **Data Model Insights**
   - Active/inactive models, size distribution, build schedule trends.

3. **User Overview**
   - Active vs inactive users, role distribution, group membership, usage frequency.

### Tools & Technologies
- Python (Jupyter) – API integration and data transformation
- Sisense API – Metadata extraction
- SQL (SSMS) – Data modelling and joins
- Sisense – Dashboard creation and reporting

### Impact
- Enabled full visibility into the BI estate, supporting data-driven governance.
- Facilitated the removal of inactive dashboards, models, and users.
- Prioritised change requests based on actual usage and impact.
- Improved platform performance, reduced clutter, and increased stakeholder confidence in BI operations.
