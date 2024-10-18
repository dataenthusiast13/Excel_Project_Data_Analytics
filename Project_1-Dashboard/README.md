# Excel Salary Dashboard

![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/bcb106f8-3e48-43d7-85ce-709cad7e3d73)


## Introduction

This data jobs salary dashboard was created to show people interested in data jobs salaries for their desired jobs and ensure they are being adequately compensated. 

The data is from data based on google, which provides a foundation in analyzing data using this Excel. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
My final dashboard is in [1_Salary_Dashboard.xlsx](1_Salary_Dashboard.xlsx).

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023. The dataset is available online on a variety of websites, which provides a foundation for analyzing data using Excel. It includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/0023c227-96b4-4bb3-8236-b1f05bb01f88)

- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart

![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/207ffe2a-412b-40ed-a54b-44bd8a3b1363)


- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/7e6c49c2-c73b-4701-bebd-969837281e86)

📉 Dashboard Implementation

![1_Salary_Dashboard_Job_Title](https://github.com/user-attachments/assets/baeaaa19-1502-40b8-9981-e7d73ee5930d)

#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

![1_Salary_Dashboard_Screenshot2](https://github.com/user-attachments/assets/31c39e73-4e4b-4ff8-b5f8-2fa375c00e5b)

📉 Dashboard Implementation:

![1_Salary_Dashboard_Type](https://github.com/user-attachments/assets/3a4bee7a-5832-46bf-b141-c9b2ef7d3dd0)

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/69255368-97a6-4c70-b71b-c9f730374581)


## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data online from a variety of websites, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries. 
