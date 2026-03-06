# Workforce Planning Simulation
Using synthetic operational data to build an executive dashboard for a fictional company. This project comparees advisor performance against KPIs such as call metrics, regional performance, and resolution rates. Below is a comprehensive list of metrics.

## 📊 Dataset Snapshot

| Attribute | Details |
|-----------|---------|
| **Employees** | 500 advisors |
| **Regions** | West, Central, East, Atlantic |
| **Provinces** | All 10 provinces |
| **Teams** | Phone Support, In-Person Advisory |
| **Date Range** | [Your hire date range] |
| **Status Distribution** | Active, Probation, Training |

## 👤 Employee/Advisor Attributes:
| Field | Example | Purpose |
| ----------- | ----------- | ----------- |
| Employee ID | EMP001-EMP500 | Unique identifier |
| Advisor Name | Fake names | For leaderboards |
| Region	West | West, Central, East, Atlantic | Regional breakdown |
| Province | BC, AB, SK, etc. | Granular geography |
| Team | Phone Support, In-Person Advisory | Granular geography |
| Hire Date | 2019-03-15 | Tenure analysis |
| Status | Active, Probation, Training | Workforce planning |

## 📞 Call/Service Metrics (Monthly):
|Metric	| Example	| KPI Target
| ----------- | ----------- | ----------- |
| Total Calls Handled	| 120 calls	| ≥100 |
| Average Handle Time (AHT)	| 8.5 mins | ≤10 mins |
| First Call | Resolution Rate |	78%	≥80% |
| Transfer Rate	| 12%	| ≤10% |
| Callback Rate |	5%	| ≤5% |
| Customer Satisfaction Score	| 4.2/5	| ≥4.0 |
| After-Call Work Time |	3.2 mins |	≤3 mins |
| Schedule Adherence	| 92% |	≥90% |

## 📋 Account/Quality Metrics:
| Metric	| Description	| Target |
| ----------- | ----------- | ----------- |
| Accounts Assigned	| Number of client accounts	| Varies by region |
| Complex Issue Rate	| % of calls needing escalation |	≤15% |
| Documentation Quality	| Audit score on case notes |	≥85% |
| Peer Review Score	| Quality check by supervisor	| ≥4/5 |
| Training Completion	| % of required modules done |	100% |

## 💼 Operational Metrics:
| Metric	| Purpose |
| ----------- | ----------- |
| Shrinkage	| Time not taking calls (breaks, training) |
| Occupancy Rate	| % of logged-in time on calls |
| Overtime Hours	| Extra hours worked |
| Absenteeism	| Unscheduled time off |
