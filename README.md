# Salary Dashboard Excel

![Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/8697990e-5ea3-415c-a595-3d7ae9d345a2)

# Introduction
This salary dashboard is designed to empower job seekers by providing insights into compensation trends for data-related roles. It enables users to explore salary ranges for their desired jobs, ensuring fair and competitive remuneration.

The data used in this project comes from an Excel course focused on foundational skills in data analysis. The dataset includes details about job roles, salaries, geographical locations, and key skills, all of which are integrated into the dashboard for easy visualization.

# Dashboard File
The final version of the dashboard is titled Salary_calculator.xlsx

# Skills Applied in Excel
The creation of this dashboard leveraged a variety of Excel features, including:

* Charts and Visualizations
* Formulas and Functions
* Data Validation Techniques

# Data Source
The dataset contains real-world information about data science jobs from 2023. It includes essential details like:

* Job Titles
* Salary Figures
* Geographic Locations
* Required Skills
This dataset was analyzed and transformed to derive actionable insights for job seekers.

# Dashboard Development Process
## Visualizations
### Bar Chart: Salary Comparisons Across Roles
![1_Salary_Dashboard_Chart1](https://github.com/user-attachments/assets/3f1ec85f-f1b7-4396-b049-4f902f5b2948)

* Excel Features Used: Horizontal bar chart with formatted salary data for clarity.
* Design Strategy: Sorted job roles by median salary in descending order to emphasize high-paying positions.
* Insights: Highlights that senior-level positions and engineering roles generally offer higher salaries compared to analyst positions.

### Map Chart: Country-wise Median Salaries
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/64ca42dd-c9f5-45d8-b329-e3934c3c717f)

* Excel Features Used: Map chart for global visualization of salary distributions.
* Design Choices: Utilized color gradients to represent varying salary levels across regions.
* Insights: Offers a clear understanding of geographic salary differences, pinpointing high and low-paying regions.

# Formulas and Functions Used
Calculating Median Salary by Role
```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))* 
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
))
```
* Purpose: This array formula calculates the median salary based on multiple filters, such as job title, country, and job type.
* Implementation: Returns specific insights for job roles across regions, considering only valid salary entries.

Background Table<br>
![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/5d486e3e-260b-44c9-9869-05afb103f141)

Dashboard Implementation
![1_Salary_Dashboard_Job_Title](https://github.com/user-attachments/assets/53c8d12f-3456-4ad8-9b00-0d713b8993fa)

Listing Unique Job Schedule Types
```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
* Purpose: Generates a list of unique job schedule types while excluding invalid entries and zero values.
* Implementation: Provides a streamlined view of schedule types for dashboard users.

Background Table<br>
![1_Salary_Dashboard_Screenshot2](https://github.com/user-attachments/assets/28549924-b397-4e71-a48a-389a42b8ff17).

Dashboard Implementation
![1_Salary_Dashboard_Type](https://github.com/user-attachments/assets/1dd65e9d-a9d8-42fe-88ed-fdd7857cf60c)

# Data Validation
* Filtered List: Applied data validation to ensure that inputs for job title, country, and schedule type align with predefined options.
## Key Benefits:
* Prevents errors or inconsistencies in data entry.
* Simplifies the user experience by limiting choices to valid inputs.
![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/0308572b-727f-4a48-80cd-21b59023269c)

# Conclusion
This dashboard serves as a comprehensive tool for exploring salary trends in the data science industry. By analyzing factors such as location, job title, and schedule type, users can gain valuable insights to guide their career decisions. The project demonstrates how Excel's powerful features can transform raw data into actionable knowledge, making it an essential resource for data job aspirants.
