# 📊 IT Incident Management Dashboard  
### **A Business Analyst Case Study | Power BI | SLA Performance & Operational Efficiency**

---

## 🧩 **Case Study Overview**

IT service desks handle hundreds of incidents every week — across regions, severities, and support teams. Leaders often struggle to answer critical operational questions:

- Are we meeting our SLA targets  
- Which teams or regions are causing SLA breaches  
- Where are the bottlenecks in our incident lifecycle  

This project simulates a real-world consulting engagement where the goal is to build a **Power BI dashboard** that gives IT managers a unified view of **incident volume, SLA compliance, and team performance**.

As a **Business Analyst**, this project demonstrates how you translate raw operational data into **actionable insights** that improve service delivery and reduce SLA violations.

---

## 🎯 **Business Problem**

The IT Operations team faces:

- Frequent SLA breaches for high-severity incidents  
- No centralized dashboard to track performance  
- Limited visibility into regional and team-level efficiency  
- Difficulty identifying bottlenecks in the incident lifecycle  

Leadership wants to shift from reactive firefighting to **proactive, data-driven IT operations**.

---

## 🥅 **Project Objectives**

This dashboard is designed to:

- Measure **SLA compliance** across regions, teams, and severities  
- Identify **bottlenecks** in incident resolution  
- Compare **team performance** using KPIs  
- Analyze **incident trends** over time  
- Provide **drill-down insights** for operational decision-making  

---

## 🧠 **Key Business Questions**

The dashboard answers the following:

### **SLA & Performance**
- What is the overall SLA compliance percentage  
- Which regions or teams are below SLA targets  
- How do resolution times vary by severity  

### **Volume & Workload**
- Which regions report the highest incident volume  
- Are incidents increasing or decreasing over time  
- What is the distribution by severity  

### **Operational Efficiency**
- Which teams resolve incidents faster than average  
- Where do we see consistent SLA breaches  
- Which severity levels pose the highest risk  

---

## 📂 **Dataset Description**

The dataset includes:

| Column | Description |
|--------|-------------|
| Incident_ID | Unique identifier |
| Created_Date | Incident logged date/time |
| Resolved_Date | Incident closure date/time |
| Region | North, South, East, West |
| Team | Support team handling the incident |
| Severity | Critical, High, Medium, Low |
| SLA_Target_Hours | Expected resolution time |
| SLA_Met_Flag | Yes/No |

### **Derived Metrics**
- **Resolution_Time_Hours** = Resolved_Date – Created_Date  
- **SLA_Met%** = SLA_Met / Total Incidents  
- **Avg Resolution Time** by Region, Team, Severity  

---

## 🛠️ **Tools & Technologies**

- **Power BI Desktop**  
  - Data modeling (Star schema)  
  - DAX measures for KPIs  
  - Interactive visuals & slicers  

- **Power Query**  
  - Data cleaning  
  - Date formatting  
  - Calculated columns  

- **Excel**  
  - Initial dataset preparation  

---

## 🧩 **Business Analyst Workflow (Step-by-Step)**

### **1. Requirement Gathering**
Stakeholders:  
- IT Operations Manager  
- Service Desk Lead  
- Regional Managers  

Key questions asked:  
- What SLA target do you measure against  
- Which breakdowns matter most (Region, Severity, Team)  
- What decisions will this dashboard support  

Outcome: Defined KPIs, required visuals, and drill-down needs.

---

### **2. KPI Definition**

**Primary KPIs**
- SLA Compliance %  
- Total Incidents  
- Average Resolution Time  

**Secondary KPIs**
- Critical Incident SLA %  
- Team-wise SLA %  
- Region-wise incident distribution  

---

### **3. Data Cleaning & Transformation**

Performed in **Power Query**:

- Converted date columns to Date/Time  
- Standardized Region & Severity values  
- Created `Resolution_Time_Hours`  
- Validated SLA_Met_Flag logic  
- Removed nulls and incorrect timestamps  

---

### **4. Data Modeling**

A simple **Star Schema**:

```
Fact_Incidents
│
├── Dim_Region
├── Dim_Team
├── Dim_Severity
└── Dim_Date
```

**Core DAX Measures:**
- Total Incidents  
- SLA Met Incidents  
- SLA Met %  
- Avg Resolution Time  
- Incidents by Region/Team/Severity  

---

### **5. Dashboard Design**

The dashboard is structured for top‑down decision-making.

#### **Top KPIs**
- SLA Compliance %  
- Total Incidents  
- Avg Resolution Time  

#### **Trend Analysis**
- Line chart: Incidents over time  
- Bar chart: Incidents by Severity  

#### **Regional & Team Performance**
- Map visual: Incident distribution  
- Table: Team-wise SLA %, Avg Resolution Time, Incident Count  

#### **Filters**
- Region  
- Severity  
- Team  
- Date  

---

## 📊 **Insights Generated**

Examples of insights surfaced:

- SLA compliance averaged **~80%**, with noticeable dips in certain regions  
- **South region** reported the highest incident volume  
- **Team Delta** resolved incidents **25% faster** than the overall average  
- **Critical incidents** had the longest resolution times, indicating escalation gaps  

These insights help leadership prioritize staffing, training, and process improvements.

---

## 🚀 **Future Enhancements**

Planned improvements:

- Drill-through pages for incident-level details  
- Backlog & aging analysis  
- Root cause categorization  
- Integration with ServiceNow / Jira for real-time refresh  

---

## 📁 **Repository Structure**

```
IT-incident-management-dashboard/
│
├── dashboard.pbix
├── data/
│   └── it_incidents.xlsx
├── screenshots/
│   └── dashboard.pdf
└── README.md
```
.
