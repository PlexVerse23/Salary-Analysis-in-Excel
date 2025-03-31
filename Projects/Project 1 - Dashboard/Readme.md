# Salary Dashboard  

## Introduction  

This Excel-based Salary Dashboard provides insights into job opportunities and median salaries for data-related roles across different regions worldwide. The goal is to help users make informed career choices by analyzing salary trends and job availability.  
Checkout the Project here - [Salary Dashboard](Salary_dashboard.xslx)

![Proj1_full](https://github.com/user-attachments/assets/659905b6-f253-42fc-a03d-8d4826dde57b)  

## Excel Features used  

This project utilizes:
- Excel **formulas & functions** for data processing.
- **Charts** & visualizations to present salary trends.
- **Data validation** to ensure consistency and accuracy.

## Dataset  

The project uses dataset as provided by Excel Instructor Luke Barousse. The raw dataset can be seen here - [Dataset](Datasets)  
It includes detailed employee records containing information on :  
- Job Titles
- Salaries
- Location
- Skills

## Dashboard Build  

### Formulas and Functions  

```
=MEDIAN(
IF((jobs[job_country]=country)*
(jobs[salary_year_avg]<>0)*
(jobs[job_title_short]=A2)*
(ISNUMBER(SEARCH(job_type,jobs[job_schedule_type]))),
jobs[salary_year_avg])
)
```
- **Multi-Criteria Filtering :** Utilised various functions like IF, ISNUMBER, SEARCH, etc. to calculate median salary based on specific conditions.
- **Key Insights :** This formula returned the median salary while ensuring the job title, location and job-type.
```
=XLOOKUP(title_ex,D2:D11,E2:E11,"No Results")
```
- Used XLOOKUP to extract relevant data from the dataset as requested by the user.
```
=FILTER(K2#,NOT(ISNUMBER(SEARCH("and",K2#)))*(K2#<>0))
```
- Used FILTER function to cleanup the job titles.

### Charts
#### Bar Chart
![image](https://github.com/user-attachments/assets/d110a007-4a51-4189-a425-bf3ab2ee0b5e)  
- **Bar Chart :** A visually capitvating Bar Chart to represent key insights clearly.
- **Design Choice :** Horizontal bars ordered from highest to lowest value for improved readibility.
- **Key Insights :** A quick identification of salary trends showing that Senior roles pay more than the Analyst roles.

#### Map Chart
![image](https://github.com/user-attachments/assets/ed753af3-1c73-4903-919f-542654503055)
- **Map Chart :** A map chart to show salary trends across the globe.
- **Design Choice :** Color coded chart to show region disparitites in median salaries in a quick look.
- **Key Insights :** Allows to quickly grasp the salary trends of data jobs across the globe highlighting the high/low paying regions.

### Data Validation  
![Proj1_dataval](https://github.com/user-attachments/assets/ff47c7ad-36ae-43e7-bc51-b24db201f8da)  

**Enhanced Data Validation :** Utilised the Data Validation feature in Excel to ensure -
- User input is pre-defined or restricted.
- Incorrect entries prevented.
- Usability of dashboard improved.

### Key Performance Indicators (KPIs)
![image](https://github.com/user-attachments/assets/bce3a422-ff0c-4650-98b6-d8345b9b88bc)  

- Utilised the function of `XLOOKUP` to create KPIs, improving the utility of the dashboard.
- The KPIs highlight the major factors -
  - Median Salary of the `Job Title` selected.
  - Major Platform used for finding it.
  - Total Job Count.

## Conclusion  
This Salary Dashboard is a powerful tool for job seekers and professionals looking to explore regional salary trends and job opportunities. By leveraging data-driven insights, users can make informed career moves and optimize their job search strategies.










