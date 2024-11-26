# Engineering Job Market Analysis Dataset

## Executive Summary

### Motivation and Potential Applications

The rapid advancement of technology has significantly increased the demand for engineering professionals, particularly in computer science and related fields. Understanding current job market trends is crucial for:

- **Job Seekers**: Aligning skills with industry demands to enhance employability and guide career planning.
- **Employers**: Developing effective recruitment strategies to attract top talent.
- **Educational Institutions**: Adjusting curricula to prepare students with in-demand skills.

This dataset project aims to bridge the gap between industry demand and workforce readiness by analyzing job descriptions from Adzuana. By extracting and analyzing common skills, job requirements, salary trends, and geographic differences, the dataset provides valuable insights into the evolving demands of the engineering workforce.

## Description of Data

The dataset comprises approximately **10,000** job descriptions focused on engineering and computer science roles. Each entry includes:

### Positions Included in the Dataset

The dataset focuses on a wide range of engineering and computer science roles, categorized into the following five groups:

| **Group**                | **Positions Included**                                                                                     |
|--------------------------|-----------------------------------------------------------------------------------------------------------|
| **Software Development** | Software Engineer, Full Stack Developer, Front End Developer, Back End Developer, Mobile App Developer    |
| **Data Science & Analytics** | Data Scientist, Data Engineer, Machine Learning Engineer, AI Engineer, Business Intelligence Analyst       |
| **Product & Design**     | Product Manager, Business Analyst, Product Analyst, UX/UI Designer, System Analyst                       |
| **IT & Systems**         | DevOps Engineer, Cloud Engineer, Site Reliability Engineer, Security Engineer, Network Engineer           |
| **Other Tech Roles**     | Embedded Systems Engineer, Quality Assurance Engineer, Database Administrator, Solutions Architect, Blockchain Developer |

---
### Attributes of the Dataset
Each entry in the dataset contains the following attributes:
- **Job Title**: Title of the job position (e.g., Software Engineer, Data Scientist).
- **Company Name**: Name of the hiring organization.
- **Description**: Job description of responsibilities and requirements.
- **Location**: City and state where the job is located.
- **Salary Min**: Minimum salary offered.
- **Salary Max**: Maximum salary offered.
- **Date Posted**: Date when the job was posted.
- **URL**: Link to the original job posting.

### Link of Dataset
The dataset is publicly available on Kaggle with th MIT License:

[Kaggle Link](https://www.kaggle.com/datasets/luqing112/engineering-jobs-insight-dataset-csv)


### Data Uniqueness

This dataset offers a comprehensive and focused view of the engineering job market by:

- **Specialization**:Concentrating specifically on engineering and computer science roles. Unlike generic job market datasets such as O*NET or Kaggle's job datasets, which often provide high-level overviews across all industries, our dataset zeroes in on the technical and engineering domain. It emphasizes the most sought-after roles in the rapidly evolving fields of software development, data science, IT infrastructure, and emerging technologies.

## Power Analysis Results

To ensure the dataset is statistically robust and representative, a power analysis was conducted.

- **Objective**: Determine the minimum sample size required to achieve statistically significant results for the analysis of engineering job postings.
- **Parameters**:
  - **Confidence Level**: 95%
  - **Margin of Error**: 5%
  - **Estimated Proportion (p)**: 0.5 (maximum variability)

- **Calculation**:
  Cochran's formula for determining sample size is given by:

  n₀ = (Z² × p × (1 - p)) / e²

  Where:
  - Z = 1.96 (Z-score for 95% confidence)
  - e = 0.05 (Margin of error)
  - p = 0.5 (Proportion)

  Substitute the values into the formula:

  n₀ = (1.96² × 0.5 × (1 - 0.5)) / 0.05² = 384

The minimum sample size required is approximately **384**.

### Result

The required sample size is approximately **384**.
Therefore, the minimum sample size for a single random sample in this project is **384** job descriptions. 

For the number of subgroups, the project estimates analyzing **25 different job types**. 

The total sample size required is calculated as:

n = 384 × 25 ≈ 10,000

Thus, the project estimates it needs approximately **10,000 job descriptions**.

## Exploratory Data Analysis

An exploratory data analysis (EDA) was performed to extract insights from the dataset.

### 1. Geographical Distribution

**Objective**: Analyze the distribution of engineering job postings across different states.

**Methodology**:

- Excluded entries where the state information was missing or invalid.
- Counted the number of job postings per state.
- Visualized the top 20 states with the highest number of job postings.

**Findings**:

- **Top States**:
  - **California**: Highest number of job postings, reflecting the tech industry's concentration in Silicon Valley.
  - **Texas**, **New York**, **Washington**, and **Massachusetts** also have significant numbers of job postings.
- **Visualization**:

  ![Job Distribution Across Top 20 States](images/state_job_distribution.png)

### 2. Skills Demand Analysis

#### Overall Skills Statistics

**Objective**: Identify the most in-demand skills across all engineering job postings.

**Methodology**:

- Extracted skills from job descriptions using a predefined skills dictionary covering programming languages, web technologies, databases, cloud platforms, etc.
- Counted the frequency of each skill.

**Findings**:

- **Top 10 Most Common Skills**:
  1. **agile**
  2. **java**
  3. **aws**
  4. **leadership**
  5. **sql**
  6. **javascript**
  7. **scrum**
  8. **c++**
  9. **python**
  10. **c#**

- **Visualization**:

  ![Top 20 Most Common Skills](images/top_skills.png)

#### Skills Demand by Job Title

**Objective**: Determine the most sought-after skills for specific job titles.

**Methodology**:

- Grouped data by job title.
- For each job title, counted the frequency of skills mentioned.

**Example Findings**:

- **Software Engineer**:
  - High demand for **Java**, **C++**, **Python**, and knowledge of **Agile** methodologies.
- **Data Scientist**:
  - Emphasis on **Python**, **machine learning**, **data analysis**, and proficiency with **SQL**.

- **Visualizations**: Generated bar charts for each job title showing the top skills.

### 3. Salary Analysis

**Objective**: Explore the salary ranges and distribution for engineering roles.

**Methodology**:

- Calculated average salaries using the provided salary ranges.
- Analyzed statistical metrics such as mean, median, and percentiles.
- Visualized salary distribution using histograms and boxplots.

**Findings**:

- **Average Salary**: Approximately \$105,000.
- **Salary Range**: Most salaries range between \$80,000 and \$130,000.
- **Outliers**: Some positions offer salaries exceeding \$150,000, indicating roles requiring specialized expertise or senior positions.

- **Visualization**:

  - **Histogram**:

    ![Salary Distribution Histogram](images/salary_histogram.png)

  - **Boxplot**:

    ![Salary Distribution Boxplot](images/salary_boxplot.png)

### 4. Company Analysis

#### Companies with the Most Job Postings

**Objective**: Identify which companies are actively hiring for engineering positions.

**Methodology**:

- Counted the number of job postings per company.
- Listed and visualized the top 20 companies.

**Findings**:

- **Top Hiring Companies**:
  - **Amazon**
  - **Microsoft**
  - **Google**
  - **IBM**
  - **Apple**

- **Visualization**:

  ![Top 20 Companies by Job Postings](images/top_companies.png)

#### Company-Specific Trends

**Objective**: Analyze salary offerings and skill demands for top companies.

**Methodology**:

- For each of the top companies, calculated the average salary offered.
- Identified the most demanded skills per company.

**Findings**:

- **Amazon** offers competitive salaries with a focus on skills like **AWS**, **Java**, and **Leadership**.
- **Google** emphasizes skills in **Python**, **Machine Learning**, and **Agile** methodologies.

### 5. Word Cloud of Job Descriptions

**Objective**: Visualize the most frequent words used in job descriptions to identify common themes and requirements.

**Methodology**:

- Combined all job descriptions into a single text corpus.
- Processed the text by removing common stopwords and irrelevant terms.
- Generated a word cloud visualization.

**Findings**:

- Commonly emphasized terms include **development**, **team**, **management**, **design**, **system**, and **support**.

- **Visualization**:

  ![Word Cloud of Job Descriptions](images/job_description_wordcloud.png)

## Link to Data Sourcing Code

The code used for data sourcing is publicly available on GitHub:

[GitHub Repository Link](https://github.com/ludaladila/Engineering-Job-Market-Analysis/blob/main/adzuna_jobs_fetcher.py)

## Ethics Statement

This project was conducted with careful consideration of ethical standards and legal regulations.

- **Data Privacy**:
  - No personal identifiable information of individuals was collected or stored.
  - Only publicly available job postings were used.
- **Compliance with Terms of Service**:
  - Data collection adhered to the terms and conditions of each job platform.
  - For platforms web scraping, data was accessed via official APIs.
- **Usage Intent**:
  - The dataset is intended for educational and research purposes.
  - Users are encouraged to respect copyright laws and platform policies when utilizing the data.
- **Impact Consideration**:
  - The project aims to positively impact job seekers, employers, and researchers.
  - Potential misuse of the data for discriminatory practices is strongly discouraged.

## Open Source License

This project is licensed under the **MIT License**.

[MIT License Text](https://opensource.org/licenses/MIT)

```
MIT License

Copyright (c) 2023

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction...

[Full license text in the repository]
```

---

**Note**: For the full license text, please refer to the [LICENSE](https://github.com/ludaladila/Engineering-Job-Market-Analysis/blob/main/LICENSE) file in the repository.

## Link to 3-Minute Pitch Video

[Watch the Project Presentation Video](https://www.youtube.com/watch?v=YourVideoLink)


