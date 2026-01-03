# Employee-Performance-Dashboard-
# Employee Performance Analysis Dashboard (Power BI)

## Project Overview
This project focuses on building an interactive **Employee Performance Analysis Dashboard** using **Power BI**.  
The dashboard helps organizations analyze employee productivity, task efficiency, performance trends, and promotion eligibility using data-driven insights.

---

## Problem Statement
Many organizations, especially startups, lack structured systems to:
- Track employee task performance
- Measure individual and departmental efficiency
- Identify high, average, and low performers
- Evaluate promotion eligibility objectively
- Monitor workload and burnout risk

This dashboard addresses these challenges through visual analytics.

---

## Objectives
- Analyze employee task completion and delays
- Evaluate performance at employee and department levels
- Identify promotion-eligible employees
- Detect workload imbalance and burnout risk
- Provide executive-level insights for decision-making

---

## Tools & Technologies
- Power BI
- DAX (Data Analysis Expressions)
- Power Query
- CSV / Excel Dataset

---

## Dataset Description
The dataset is a simulated employee performance dataset used for analytical and learning purposes.

### Key Columns
- Employee_ID
- EmployeeName
- Department
- JobTitle
- Gender
- Experience (Years)
- TasksAssigned
- TasksCompleted
- TasksPending
- TasksDelayed
- PerformanceScore
- LeavesTaken
- WorkHoursPerWeek
- OvertimeHours
- EligibleForPromotion

---

## Key KPIs
- Total Employees
- Average Performance Score
- Promotion Eligible Count
- Promotion Percentage
- High Performers
- Average Performers
- Low Performers
- Employees at Burnout Risk
- Average Leaves per Employee
- Top Performance Score

---

## Dashboard Pages

### Page 1: Employee Performance Analysis
- Employee-wise task summary
- Tasks Assigned vs Completed vs Pending vs Delayed
- Performance Score ranking
- Promotion Eligibility analysis
- Workload and overtime tracking

#### Filters Used
- Department
- Job Title
- Gender
- Promotion Eligibility

  <img width="1299" height="714" alt="Screenshot 2026-01-03 121441" src="https://github.com/user-attachments/assets/2fb7c8e6-78cf-4a3d-8612-7714257a8b6c" />


---

### Page 2: Executive Overview
- High-level KPIs for leadership
- Department-wise average performance
- Task status distribution
- Salary distribution by job title
- Top performing employees
- Work hours vs performance comparison

  <img width="1276" height="707" alt="Screenshot 2026-01-03 121450" src="https://github.com/user-attachments/assets/7a078ed9-d249-4d06-aa91-59b855503583" />


---

## DAX Measures Used

### Total Employees
```DAX
Total Employees =
COUNT(Employee_Data[Employee_ID])

Promotion Eligible Count =
CALCULATE(
    COUNTROWS(Employee_Data),
    Employee_Data[EligibleForPromotion] = "Yes"
)

Promotion % =
DIVIDE(
    [Promotion Eligible Count],
    [Total Employees]
) * 100


