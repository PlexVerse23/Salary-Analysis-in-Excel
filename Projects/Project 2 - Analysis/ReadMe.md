
# 📊 Data Jobs Analysis - Skills Based

## 🚀 Introduction

As someone passionate about analytics and job market trends, I wanted to explore the skills that drive higher salaries in the data domain. Using Excel as the primary tool, I analyzed real-world job data to find out what makes a data professional more valuable — by skills, role, and region.

## 🔍 Key Questions Explored

1. Do more skills lead to better pay?
2. How do salaries vary across different regions?
3. What are the top skills of data professionals?
4. Which skills are linked to the highest salaries?

## 🧰 Excel Tools Used

- 📊 PivotTables & PivotCharts  
- 🔍 Power Query  
- 💪 Power Pivot  
- 🧮 DAX (Data Analysis Expressions)  

## 📂 Dataset Overview

The dataset includes data science job postings from 2023, featuring details on:

- 👨‍💼 Job Titles  
- 💰 Average Salaries  
- 📍 Locations  
- 🛠️ Skills Required  

---

## 1️⃣ Do More Skills Mean Better Pay?

### ➡️ Power Query for ETL

#### 🗃️ Extract

- Pulled data from `data_salary_all.xlsx`, and split it into two queries:
  - `data_jobs_all`: All job data
  - `data_jobs_skills`: Skillset linked by job ID

#### 🧹 Transform

- Cleaned column names, trimmed whitespace, and removed irrelevant data.

<div align="center">
  <img src="Analysis%20of%20Data%20Jobs%20-%201/assets/2_top_paying_roles_skills.png" alt="Top Paying Roles and Skills" width="600">
</div>

#### 📥 Load

- Loaded both queries into the Excel Data Model for deeper analysis.

### 💡 Insights

- More skills = higher salary: Especially true for Senior Data Engineers and Data Scientists.
- Business Analysts, needing fewer skills, had relatively lower median pay.

---

## 2️⃣ Salaries Across Different Regions

### 📊 PivotTables + DAX

#### 🧮 DAX Measures

```DAX
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```
To analyze median salaries in the US and globally, I created a custom DAX measure.

### 💡 Insights

- Salaries are significantly higher in the US for roles like **Data Engineer** and **ML Engineer**.
- Regional differences are stark and worth considering for remote or global roles.

<div align="center">
  <img src="Analysis%20of%20Data%20Jobs%20-%201/assets/2_top_paying_roles_skills.png" alt="Salaries by Region" width="600">
</div>

---

## 3️⃣ Top Skills in Demand

### 🔗 Power Pivot for Data Modeling

- Linked `data_jobs_all` and `data_jobs_skills` via `job_id`.
- Built a clean data model for skill frequency analysis.

### 💡 Insights

- 🔝 **Top Skills**: SQL, Python, AWS, Excel, Azure
- 📉 **Less Valued**: PowerPoint, Tableau (in terms of pay correlation)

<div align="center">
  <img src="Analysis%20of%20Data%20Jobs%20-%201/assets/2_top_paying_roles_skills.png" alt="Top Skills Chart" width="600">
</div>

---

## 4️⃣ Highest Paying Skills

### 📈 Advanced PivotCharts

Created a combo chart to visualize:
- 📊 **Median Salary** (Bar)
- 📈 **Skill Likelihood %** (Line)

### 💡 Insights

- 💰 **High-paying skills**: Python, Oracle, SQL
- 🧊 **Low-paying**: General tools like MS Word or PowerPoint

<div align="center">
  <img src="Analysis%20of%20Data%20Jobs%20-%201/assets/2_top_paying_roles_skills.png" alt="Top Paying Skills Chart" width="600">
</div>

---

## ✅ Conclusion

This project gave me valuable insight into the data job market — revealing how crucial certain skills are to earning potential. Tools like **Power Query**, **PivotTables**, **DAX**, and **Power Pivot** enabled me to dig deep into the data and spot trends.

Whether you're a job seeker or a data enthusiast, I hope this analysis provides a clear direction on what skills to focus on for a high-impact data career.


