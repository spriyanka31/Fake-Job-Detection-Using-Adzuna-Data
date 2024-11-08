# Fake Job Detection Using Adzuna

## Project Overview
This project aims to analyze job postings data to identify potential fake job postings and uncover trends in job posting activity over time, through data processing, filtering, and visualization, we gain insights into job posting patterns by company, seasonal hiring trends, and detect any suspicious postings.

The primary goals of the project are:
- To detect fake job postings in the dataset.
- To visualize job posting trends by company and over time.
- To explore possible factors influencing hiring patterns, such as seasonality and economic events like elections.

## Dataset Description
The dataset used contains multiple job listings, each with various attributes:
- **Company Name**: The organization posting the job.
- **Job Title**: The position being advertised.
- **Date Posted**: The date when the job was listed.
- **Job Description**: The details of the job role.
- **Fake Job Indicator**: A boolean flag indicating whether the job is suspected to be fake.

The goal of this project is to clean, analyze, and interpret this data to highlight notable patterns and detect any suspicious job postings.

## Real-Time Data Collection via Adzuna API
A key feature of this project is the integration of the Adzuna API, which provides access to real-time job posting data from multiple job boards and websites. This API continuously collects fresh data to ensure up-to-date analysis and helps in detecting fake job postings as soon as they appear.

## How the Adzuna API Works
The Adzuna API pulls job posting data from external sources and stores the information, including company name, job title, job description, and posting date. The collected data is then processed to flag any potential fake job postings using pre-defined criteria.

## Data Preprocessing
In this step, the data is cleaned and processed to prepare it for analysis:
1. **Date Conversion**: The **Date Posted** column is converted to a datetime format. This conversion enables time-series analysis of job postings over time.
2. **Fake Job Filtering**: The dataset is filtered to create separate dataframes for suspected fake jobs and legitimate jobs, based on the **Fake Job Indicator** column.

## Key Analyses and Visualizations

### 1. Job Postings by Company
This analysis visualizes the number of job postings by each company. It helps to identify the most active employers in the dataset. By analyzing the distribution of job postings across different companies, we can detect trends in employer activity and assess whether there are companies with unusually high posting volumes.

### 2. Time-Series Analysis of Job Postings
A time-series analysis is conducted to observe job posting trends over time. This analysis focuses on monthly changes, allowing us to uncover seasonal trends and patterns. We can identify peaks in job posting activity, which could be linked to certain times of the year, such as after fiscal year-end budget decisions or major events like elections.

## Results and Insights

- **Top Employers**: The analysis shows that **Experian** has a higher number of job postings than other companies, with nearly 80 listings. This suggests that Experian may be a prominent job poster, or it may indicate potential issues like data duplication.
  
- **Seasonal Trends**: There is a noticeable peak in job postings during **October**, followed by a decline in **November**. This trend could be linked to year-end budgeting cycles, where companies may hire to utilize budget allocations before the end of the fiscal year, or economic events such as elections impacting job activity.

- **Fake Job Detection**: Only **one job posting** was flagged as suspicious, indicating that most of the job listings in the dataset appear legitimate. This suggests that the dataset is mostly clean, with minimal risk of fake job postings.

## Conclusion

This analysis provides insights into job posting patterns, with a focus on:
- Identifying **top job posters** in the dataset.
- Detecting **seasonal hiring trends** over time.
- Flagging **potential fake job postings**.

The results show that the dataset is largely legitimate, with minimal instances of suspected fake job postings. The methodology used here could be expanded and applied to larger datasets to detect fake job listings at scale. Future work could include analyzing trends within specific industries or job roles to provide even deeper insights into the job market.
