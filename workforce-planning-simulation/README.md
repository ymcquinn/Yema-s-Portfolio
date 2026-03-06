# 🎯 From KPIs to Action: Workforce Planning for Professional Services Firms
### A 12-Month Time-Series Analysis of Advisor Performance

## 📋 Project Overview
This project simulates workforce analytics for a boutique HR and Health & Safety consulting firm serving medium to large businesses across Canada. Using synthetic employee data spanning 12 months, I analyze key performance indicators (KPIs) to identify trends, optimize resource allocation, and provide actionable recommendations for improving advisor performance and client outcomes.

## 🏢 Business Context
The firm delivers services through two primary channels:
- **Phone Support Advisors**: Handle on-demand client calls, providing immediate HR and H&S guidance
- **In-Person Advisors**: Conduct onsite client visits for deeper consultations and relationship management

Management needed visibility into:
- Regional performance variations
- Individual advisor effectiveness
- Progress toward KPI targets
- Resource allocation across provinces

## 📊 Dataset: 12-Month Time Series

| Dimension | Details |
|-----------|---------|
| **Employees** | 500 advisors across Canada |
| **Time Period** | 12 consecutive months |
| **Total Records** | 6,000 employee-month observations |
| **Regions** | West, Central, East, Atlantic |
| **Teams** | Phone Support, In-Person Advisory |

### 👤 Employee Attributes (Static)
- `employee_id`: Unique identifier
- `region`: Geographic region
- `province`: Specific province
- `team`: Phone Support or In-Person Advisory
- `hire_date`: Original hire date
- `status`: Active, Probation, Training

### 📅 Monthly Metrics (Time-Varying)
- `calls_handled`: Monthly call volume
- `avg_handle_time_minutes`: Average call duration
- `first_call_resolution_rate`: % resolved without transfer
- `transfer_rate`: % of calls requiring transfer
- `csat`: Customer satisfaction score (1-5)
- `schedule_adherence`: % of scheduled time logged in
- `overtime_hours`: Extra hours worked
- `shrinkage_percent`: Time not on calls (breaks, training)

### 📊 Quarterly Metrics (Updated Every 3 Months)
- `accounts_assigned`: Client accounts managed
- `documentation_quality`: Audit score on case notes (0-100)
- `training_completion`: % of required modules completed

## 🎯 Key Performance Indicators (KPIs)

| KPI | Target | Formula/Description |
|-----|--------|---------------------|
| Call Volume | ≥100/month | Total calls handled |
| Avg Handle Time | ≤10 mins | Average call duration |
| First Call Resolution | ≥80% | (Calls resolved / Total calls) × 100 |
| Transfer Rate | ≤10% | (Calls transferred / Total calls) × 100 |
| CSAT | ≥4.0/5 | Average customer satisfaction |
| Schedule Adherence | ≥90% | (Time logged in / Scheduled time) × 100 |
| Overtime % | ≤5% | (Overtime hours / Total hours) × 100 |
| Shrinkage | ≤20% | (Non-call time / Total paid time) × 100 |

### 🧮 Calculated Metrics (To Be Created)
- **Productivity Index**: Weighted combination of calls handled + FCR + CSAT
- **Quality Score**: Average of documentation quality + CSAT + FCR
- **Tenure**: Years since hire date
- **Performance Tier**: High/Medium/Low based on composite score

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

## 📁 Repository Structureworkforce-planning-simulation/
├── README.md (this file)
├── data/
│ └── workforce_data_12months.csv (6,000 rows)
├── dashboard/
│ └── workforce_dashboard.xlsx (Excel file)
├── analysis/
│ └── python_analysis.ipynb (optional)
└── visuals/
└── dashboard_screenshots/


## 🔒 Note
*This project uses fully synthetic data generated for portfolio purposes. Any resemblance to real persons or organizations is coincidental.*
