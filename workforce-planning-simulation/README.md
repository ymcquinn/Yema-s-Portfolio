# 🎯 From KPIs to Action: Workforce Planning for Professional Services Firms
### A 12-Month Time-Series Analysis of Advisor Performance

## 📋 Project Overview
This project simulates workforce analytics for a boutique HR and Health & Safety consulting firm serving medium to large businesses across Canada. Using synthetic employee data spanning 12 months (2024), I analyze key performance indicators (KPIs) to identify trends, optimize resource allocation, and provide actionable recommendations for improving advisor performance and client outcomes.

## 🏢 Business Context
The firm delivers services through two primary channels:
- **Phone Support Advisors**: Handle on-demand client calls (higher volume, lower resolution rates)
- **In-Person Advisors**: Conduct onsite client visits (lower volume, higher quality metrics)

## 📊 Dataset: 12-Month Time Series

| Dimension | Details |
|-----------|---------|
| **Employees** | 500 advisors across Canada |
| **Time Period** | 12 months (January-December 2024) |
| **Total Records** | 6,000 employee-month observations |
| **Regions** | West, Central, East, Atlantic |
| **Teams** | Phone Support, In-Person Advisory |

### 👤 Employee Attributes (Static)
| Field | Description |
|-------|-------------|
| `employee_id` | Unique identifier (500 employees) |
| `region` | West, Central, East, Atlantic |
| `province` | All 10 Canadian provinces |
| `team` | Phone Support or In-Person Advisory |
| `hire_date` | Original hire date |
| `status` | Active, Probation, Training |

### 📅 Monthly Metrics (Time-Varying)
| Field | Description | Range/Notes |
|-------|-------------|-------------|
| `month` | YYYY-MM format | 2024-01 to 2024-12 |
| `tenure_years` | Calculated from hire date | Changes monthly |
| `calls_handled` | Monthly call volume | Varies by team/region |
| `avg_handle_time_minutes` | Average call duration | Target: ≤10 mins |
| `first_call_resolution_rate` | % resolved without transfer | Target: ≥80% |
| `transfer_rate` | % of calls requiring transfer | Target: ≤10% |
| `csat` | Customer satisfaction (1-5) | Target: ≥4.0 |
| `schedule_adherence` | % of scheduled time logged in | Target: ≥90% |
| `overtime_hours` | Extra hours worked | 0-20 hours/month |
| `shrinkage_percent` | Time not on calls | 10-35% |

### 📊 Quarterly Metrics (Updated Every 3 Months)
| Field | Description |
|-------|-------------|
| `accounts_assigned_qtr` | Client accounts managed |
| `documentation_quality` | Audit score on case notes (0-100) |
| `training_completion` | % of required modules completed |

### 🎯 Performance Classification
| Field | Description |
|-------|-------------|
| `performance_tier` | High/Medium/Low (computed from FCR, CSAT, adherence, documentation) |

## 🔍 Built-In Analytical Patterns
The dataset intentionally includes realistic workforce dynamics:

**Regional Effects:**
- **West region** consistently outperforms others on:
  - CSAT scores
  - Documentation quality
  - Schedule adherence
  - Transfer rates
  - Handle times

**Team Differences:**
| Metric | Phone Support | In-Person Advisory |
|--------|---------------|---------------------|
| Call Volume | Higher | Lower |
| Resolution Rate | Lower | Higher |

## 🎯 Key Performance Indicators (KPIs)

| KPI | Target | Business Question |
|-----|--------|-------------------|
| Call Volume | Varies by role | Are we staffed appropriately? |
| Avg Handle Time | ≤10 mins | Are calls efficient? |
| First Call Resolution | ≥80% | Are issues resolved quickly? |
| Transfer Rate | ≤10% | Are advisors knowledgeable? |
| CSAT | ≥4.0/5 | Are clients satisfied? |
| Schedule Adherence | ≥90% | Are advisors available when scheduled? |
| Overtime Hours | Monitor | Is there burnout risk? |
| Shrinkage | Monitor | Is non-call time managed well? |

## 🔍 Analysis Objectives

1. **Regional Performance**: Why does West outperform? What can other regions learn?
2. **Team Comparison**: Phone Support vs. In-Person - different metrics, different expectations
3. **Tenure Impact**: Do longer-tenured employees perform better?
4. **Overtime Analysis**: Does overtime correlate with performance or burnout?
5. **Performance Drivers**: What predicts High vs. Low performance tier?
6. **Monthly Trends**: Seasonality patterns and forecasting

## 📈 Deliverables

- **Interactive Excel Dashboard**: Pivot tables, slicers, conditional formatting, sparklines
- **Performance Insights**: Top/bottom regions, advisors, and trends
- **Actionable Recommendations**: Training priorities, coaching targets, resource allocation

## 📁 Repository Structure| CSAT | ≥4.0/5 | Average customer satisfaction |
| Schedule Adherence | ≥90% | (Time logged in / Scheduled time) × 100 |
| Overtime % | ≤5% | (Overtime hours / Total hours) × 100 |
| Shrinkage | ≤20% | (Non-call time / Total paid time) × 100 |

### 🧮 Calculated Metrics (To Be Created)
- **Productivity Index**: Weighted combination of calls handled + FCR + CSAT
- **Quality Score**: Average of documentation quality + CSAT + FCR
- **Tenure**: Years since hire date
- **Performance Tier**: High/Medium/Low based on composite score
- **Composite Score**: Weighted combination of FCR + CSAT + Schedule Adherence + documentation quality 

## 🔍 Analysis Objectives

1. **Regional Performance**: Which provinces/regions outperform? Underperform?
2. **Advisor Rankings**: Top/bottom performers by key metrics
3. **Trend Analysis**: How do metrics change over 12 months?
4. **KPI Gaps**: Where are we missing targets? By how much?
5. **Team Comparison**: Phone Support vs. In-Person Advisory patterns
6. **Predictive Insights**: Which factors drive high performance?

## 📈 Deliverables

- **Interactive Excel Dashboard**: Pivot tables, slicers, charts, conditional formatting
- **Python Analysis** (Optional): Deeper statistical insights and visualizations
- **Actionable Recommendations**: Training priorities, resource reallocation, coaching opportunities

## 🛠️ Tools Used
- **Data Generation**: ChatGPT
- **Analysis**: Microsoft Excel (PivotTables, Power Query, DAX)
- **Visualization**: Excel Charts, Conditional Formatting
- **Documentation**: Markdown, GitHub

## 📁 Repository Structure workforce-planning-simulation/
├── README.md (this file)
├── data/
│ └── workforce_data_12months.csv (6,000 rows)
├── dashboard/
│ └── workforce_dashboard.xlsx (Excel file)
├── analysis/
│ └── python_analysis.ipynb (optional)
└── visuals/
└── dashboard_screenshots/

## Composite Score Explanation
- first_call_resolution_rate (30%)
- csat (30%) 
- schedule_adherence (20%)
- documentation_quality (20%)

**Why These Metrics?**
I weighted **FCR and CSAT highest** because they directly measure **client outcomes**. The other two measure **operational behaviors** that enable those outcomes.

### High Weight (30% each) - **The Customer Experience Drivers**
**First Call Resolution Rate (30%)**
- *Why*: Nothing frustrates clients more than being transferred or having to call back. Solving issues on the first call is the #1 driver of customer satisfaction in call centers.
- *Business impact*: Higher FCR = lower call volume = lower operational costs
**CSAT (30%)**
- *Why*: It's the ultimate measure of whether clients feel helped. If they're not satisfied, nothing else matters.
- *Business impact*: Directly ties to client retention and contract renewals

### Medium Weight (20% each) - **The Operational Excellence Drivers**
**Schedule Adherence (20%)**
- *Why*: An advisor can be amazing, but if they're not available when scheduled, clients wait longer and service suffers.
- *Business impact*: Impacts service levels and team workload balance
**Documentation Quality (20%)**
- *Why*: Poor notes mean dropped details, repeated questions, and legal/compliance risks. Good documentation shows professionalism and protects the firm.
- *Business impact*: Reduces errors, improves continuity of service, mitigates risk

## What About Other Metrics I Didn't Include:
| Metric | Why It's NOT in Composite |
|--------|---------------------------|
| **Calls Handled** | Volume ≠ Quality. Someone could take 200 calls but resolve nothing. |
| **Avg Handle Time** | Faster isn't better if issues aren't resolved. Quality over speed. |
| **Transfer Rate** | Already captured in FCR (low transfer = high FCR) |
| **Overtime Hours** | More about burnout risk than performance quality |
| **Accounts Assigned** | Often based on tenure/role, not performance |


## 🔒 Note
*This project uses fully synthetic data generated for portfolio purposes. Any resemblance to real persons or organizations is coincidental.*
