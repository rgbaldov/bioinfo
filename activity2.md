# 🏥 Activity 2: Analyzing Electronic Health Records (EHR) Using SQL and Python

## 🎯 Learning Objectives
By the end of this activity, students will be able to:
1. Design and query healthcare databases using SQL  
2. Extract clinical data into Python using `sqlite3` and `pandas`  
3. Perform basic health analytics (descriptive statistics & insights)  
4. Interpret results for healthcare decision-making

## 🧠 Scenario (Problem Context)
You are a **health data analyst** in a hospital. The administration wants insights from the **Electronic Health Records (EHR)** database to:
- Monitor patient demographics  
- Identify common diagnoses  
- Analyze hospital length of stay  
- Support data-driven healthcare planning

## 🗃️ Database Schema

### Table 1: `patients`

| Column | Type | Description |
|------|------|------------|
| patient_id | INTEGER | Unique patient ID |
| name | TEXT | Patient name |
| age | INTEGER | Age |
| gender | TEXT | M / F |
| city | TEXT | Residence |

### Table 2: `visits`

| Column | Type | Description |
|------|------|------------|
| visit_id | INTEGER | Visit ID |
| patient_id | INTEGER | Foreign key |
| diagnosis | TEXT | Primary diagnosis |
| admission_date | DATE | Date admitted |
| discharge_date | DATE | Date discharged |

## 🛠️ Part A – SQL Tasks (40%)

### Task 1: List all patients older than 60
```sql
SELECT * FROM patients
WHERE age > 60;
