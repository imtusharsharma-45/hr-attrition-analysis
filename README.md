# HR Employee Attrition — EDA & Statistical Hypothesis Testing

## Project Overview

This project analyzes employee attrition using **Python, exploratory data analysis (EDA), and statistical hypothesis testing**.

The objective is not only to identify patterns in employee turnover, but also to test whether observed relationships between workforce characteristics and attrition are statistically significant.

The analysis covers **1,470 employees across 35 attributes** and evaluates factors including overtime, monthly income, department, and job satisfaction.

---

## Business Problem

Employee attrition can increase recruitment costs, disrupt teams, and reduce organizational productivity.

Management wants to understand which workforce characteristics are associated with employee attrition and whether these relationships are statistically significant rather than simply visible patterns in the data.

### Key Questions

- Is overtime associated with employee attrition?
- Do employees who leave have different income levels?
- Is attrition associated with department?
- Do employees who leave report different job satisfaction levels?
- Which employee groups may require greater retention attention?

---

## Tools & Technologies

| Technology | Purpose |
|---|---|
| Python | Data analysis |
| Pandas | Data manipulation |
| NumPy | Numerical analysis |
| Matplotlib | Data visualization |
| Seaborn | Exploratory visualization |
| SciPy | Statistical hypothesis testing |
| Jupyter Notebook | Analysis workflow |

---

## Dataset Information

The project uses an IBM HR Analytics Employee Attrition dataset containing employee demographic, compensation, job, satisfaction, and employment-history information.

### Dataset Summary

| Metric | Value |
|---|---:|
| Employees | 1,470 |
| Features | 35 |
| Attrited Employees | 237 |
| Retained Employees | 1,233 |
| Overall Attrition Rate | 16.12% |
| Missing Values | 0 |
| Exact Duplicate Rows | 0 |

---

## Analysis Workflow

The project follows a structured analytical workflow:

1. Data loading and inspection
2. Data quality validation
3. Univariate analysis
4. Bivariate attrition analysis
5. Exploratory data visualization
6. Statistical hypothesis testing
7. Interpretation of results
8. Business recommendations

---

## Exploratory Data Analysis

EDA was performed to understand workforce patterns related to:

- Employee attrition
- Overtime
- Monthly income
- Department
- Job role
- Job satisfaction
- Employee demographics
- Workforce tenure and experience

Correlation analysis was also used to explore relationships among numerical employee characteristics.

---

# Statistical Hypothesis Testing

A significance level of **α = 0.05** was used for hypothesis testing.

## 1. Overtime vs Attrition

### Hypotheses

**H₀:** Overtime and attrition are independent.

**H₁:** Overtime and attrition are associated.

### Test

Chi-Square Test of Independence

### Result

- χ² = **87.56**
- p-value **< 0.001**

### Decision

Reject H₀.

There is a statistically significant association between overtime and employee attrition.

### Observed Attrition Rates

| Overtime | Attrition Rate |
|---|---:|
| Yes | 30.53% |
| No | 10.44% |

Employees working overtime show approximately three times the observed attrition rate of employees not working overtime.

---

## 2. Monthly Income vs Attrition

### Hypotheses

**H₀:** Mean monthly income is equal between attrited and retained employees.

**H₁:** Mean monthly income differs between the two groups.

### Test

Welch's Independent Samples t-test

### Result

- t-statistic = **-7.48**
- p-value **< 0.001**

### Decision

Reject H₀.

Monthly income differs significantly between employees who left and employees who remained.

### Income Comparison

| Employee Group | Average Monthly Income | Median Monthly Income |
|---|---:|---:|
| Attrited | 4,787 | 3,202 |
| Retained | 6,833 | 5,204 |

Employees who left had substantially lower income in this dataset.

---

## 3. Department vs Attrition

### Hypotheses

**H₀:** Department and attrition are independent.

**H₁:** Department and attrition are associated.

### Test

Chi-Square Test of Independence

### Result

- χ² = **10.80**
- p-value = **0.0045**

### Decision

Reject H₀.

Department and employee attrition are statistically associated.

### Department Attrition Rates

| Department | Attrited | Total Employees | Attrition Rate |
|---|---:|---:|---:|
| Sales | 92 | 446 | 20.63% |
| Human Resources | 12 | 63 | 19.05% |
| Research & Development | 133 | 961 | 13.84% |

Research & Development has the largest **number** of attritions because it is the largest department, while **Sales has the highest attrition rate**.

---

## 4. Job Satisfaction vs Attrition

### Hypotheses

**H₀:** Mean job satisfaction is equal between attrited and retained employees.

**H₁:** Mean job satisfaction differs between the two groups.

### Test

Welch's Independent Samples t-test

### Result

- t-statistic = **-3.93**
- p-value ≈ **0.0001**

### Decision

Reject H₀.

Mean job satisfaction differs significantly between employees who left and those who remained.

### Satisfaction Comparison

| Employee Group | Average Job Satisfaction |
|---|---:|
| Attrited | 2.47 |
| Retained | 2.78 |

Employees who left reported lower average job satisfaction.

---

## Statistical Results Summary

| Business Question | Statistical Test | Result | Significant? |
|---|---|---|---|
| Overtime vs Attrition | Chi-Square | χ²=87.56, p<0.001 | Yes |
| Monthly Income vs Attrition | Welch's t-test | t=-7.48, p<0.001 | Yes |
| Department vs Attrition | Chi-Square | χ²=10.80, p=0.0045 | Yes |
| Job Satisfaction vs Attrition | Welch's t-test | t=-3.93, p≈0.0001 | Yes |

All four tested relationships show statistically significant differences or associations at **α = 0.05**.

---

## Key Business Insights

### 1. Overtime is strongly associated with attrition

Employees working overtime have an observed attrition rate of approximately **30.5%**, compared with approximately **10.4%** among employees without overtime.

Overtime should therefore be investigated as an important retention indicator.

### 2. Attrited employees have lower income

Employees who left had a median monthly income of **3,202**, compared with **5,204** among retained employees.

Compensation differences should be investigated together with job level, experience, role, and tenure.

### 3. Sales has the highest departmental attrition rate

Although Research & Development has the largest raw number of attritions, **Sales has the highest attrition rate at approximately 20.6%**.

This demonstrates why normalized rates are more useful than raw counts when comparing differently sized departments.

### 4. Job satisfaction differs between groups

Employees who left reported lower average job satisfaction than employees who remained.

Employee satisfaction can therefore be considered alongside other workforce indicators when evaluating retention risk.

---

## Business Recommendations

1. **Review overtime-heavy roles**  
   Identify teams with persistent overtime and evaluate staffing, workload distribution, scheduling, and employee recovery time.

2. **Review compensation competitiveness**  
   Investigate compensation for employee groups showing higher attrition, while controlling for job level, experience, and role.

3. **Prioritize Sales retention analysis**  
   Sales has the highest departmental attrition rate and may benefit from deeper analysis of workload, incentives, management practices, and career progression.

4. **Monitor employee satisfaction**  
   Regular engagement or pulse surveys may help identify declining satisfaction before employees leave.

5. **Use multiple indicators together**  
   Attrition should not be attributed to one variable alone. Overtime, compensation, department, satisfaction, tenure, role, and career progression should be considered together.

---

## Important Statistical Note

Statistical significance indicates that the observed relationships are unlikely to be explained by random sampling variation under the null hypothesis.

However, these tests demonstrate **association or group differences — not causation**.

For example, the analysis supports an association between overtime and attrition, but it does not prove that overtime directly causes employees to leave.

---

## Project Structure

```text
hr-attrition-analysis/
│
├── data/
│   └── HR_Attrition.csv
│
├── notebooks/
│   └── eda_analysis.ipynb
│
├── outputs/
│   └── charts/
│
├── requirements.txt
│
└── README.md
```

---

## How to Reproduce

1. Clone or download this repository.
2. Install dependencies from `requirements.txt`.
3. Open `notebooks/eda_analysis.ipynb`.
4. Load the HR Attrition dataset.
5. Run the notebook cells sequentially.
6. Review the EDA visualizations.
7. Review the statistical hypothesis tests and interpretations.

---

## Skills Demonstrated

This project demonstrates practical experience with:

- Exploratory Data Analysis
- Statistical Hypothesis Testing
- Chi-Square Test of Independence
- Welch's Independent Samples t-test
- Statistical significance and p-values
- Workforce analytics
- Attrition analysis
- Pandas
- SciPy
- Matplotlib
- Seaborn
- Business insight generation
- Translating statistical evidence into recommendations

---

## Author

**Tushar Sharma**

Data Analyst | SQL | Python | Power BI | Tableau | Statistics | AWS | Snowflake

GitHub: `imtusharsharma-45`
