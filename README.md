# HR Employee Attrition Analysis | EDA & Statistical Hypothesis Testing

## 📌 Project Overview

This project presents an end-to-end employee attrition analysis using **Python, Exploratory Data Analysis (EDA), and statistical hypothesis testing**.

The project combines data exploration with statistical validation to determine whether observed workforce patterns are statistically significant. The analysis covers **1,470 employees across 35 workforce attributes**, focusing on factors such as overtime, monthly income, department, job role, and job satisfaction.

The findings are supported by **Chi-Square Tests of Independence** and **Welch's Independent Samples t-tests**, enabling evidence-based business recommendations rather than relying solely on visual observations.

---

# 🎯 Business Problem

Employee attrition can increase recruitment costs, disrupt teams, and reduce organizational productivity.

Management wants to understand which workforce characteristics are associated with employee attrition and whether these relationships are statistically significant rather than simply visible patterns in the data.

### Business Questions

- Is overtime associated with employee attrition?
- Do employees who leave have different income levels?
- Is attrition associated with department?
- Do employees who leave report different job satisfaction levels?
- Which employee groups require greater retention attention?

---

# 🛠️ Tools & Technologies

| Technology | Purpose |
|------------|---------|
| Python | Data Analysis |
| Pandas | Data Manipulation |
| NumPy | Numerical Operations |
| Matplotlib | Data Visualization |
| Seaborn | Exploratory Data Analysis |
| SciPy | Statistical Hypothesis Testing |
| Jupyter Notebook | Analysis Workflow |
| Git & GitHub | Version Control & Documentation |

---

# 📂 Dataset Information

The project uses the **IBM HR Analytics Employee Attrition** dataset containing employee demographic, compensation, job, satisfaction, and employment-history information.

### Dataset Summary

| Metric | Value |
|---------|-------:|
| Total Employees | 1,470 |
| Total Features | 35 |
| Attrited Employees | 237 |
| Retained Employees | 1,233 |
| Overall Attrition Rate | 16.12% |
| Missing Values | 0 |
| Duplicate Records | 0 |

---

# 🔄 Analysis Workflow

The project follows a structured analytics workflow:

1. Data Loading & Inspection
2. Data Quality Validation
3. Univariate Analysis
4. Bivariate Analysis
5. Exploratory Data Visualization
6. Correlation Analysis
7. Statistical Hypothesis Testing
8. Interpretation of Results
9. Business Recommendations

---

# 📊 Exploratory Data Analysis

EDA was performed to understand workforce patterns related to employee attrition.

The analysis includes:

- Employee Attrition Distribution
- Monthly Income Distribution
- Age Distribution
- Overtime vs Attrition
- Department vs Attrition
- Job Role vs Attrition
- Job Satisfaction Analysis
- Correlation Heatmap

Correlation analysis was performed to examine relationships among numerical employee characteristics before conducting statistical hypothesis testing.

---

# 📈 Statistical Hypothesis Testing

A significance level of **α = 0.05** was used for hypothesis testing.

---

## 1. Overtime vs Attrition

### Hypotheses

**H₀:** Overtime and attrition are independent.

**H₁:** Overtime and attrition are associated.

### Statistical Test

**Chi-Square Test of Independence**

### Result

- χ² = **87.56**
- p-value **< 0.001**

### Decision

Reject **H₀**.

There is a statistically significant association between overtime and employee attrition.

### Observed Attrition Rates

| Overtime | Attrition Rate |
|----------|---------------:|
| Yes | 30.53% |
| No | 10.44% |

Employees working overtime show approximately three times the observed attrition rate of employees not working overtime.

---

## 2. Monthly Income vs Attrition

### Hypotheses

**H₀:** Mean monthly income is equal between attrited and retained employees.

**H₁:** Mean monthly income differs between the two groups.

### Statistical Test

**Welch's Independent Samples t-test**

### Result

- t-statistic = **-7.48**
- p-value **< 0.001**

### Decision

Reject **H₀**.

Monthly income differs significantly between employees who left and employees who remained.

### Income Comparison

| Employee Group | Average Monthly Income | Median Monthly Income |
|---------------|-----------------------:|----------------------:|
| Attrited | 4,787 | 3,202 |
| Retained | 6,833 | 5,204 |

Employees who left had substantially lower income in this dataset.

---

## 3. Department vs Attrition

### Hypotheses

**H₀:** Department and attrition are independent.

**H₁:** Department and attrition are associated.

### Statistical Test

**Chi-Square Test of Independence**

### Result

- χ² = **10.80**
- p-value = **0.0045**

### Decision

Reject **H₀**.

Department and employee attrition are statistically associated.

### Department Attrition Rates

| Department | Attrited | Total Employees | Attrition Rate |
|------------|---------:|----------------:|---------------:|
| Sales | 92 | 446 | 20.63% |
| Human Resources | 12 | 63 | 19.05% |
| Research & Development | 133 | 961 | 13.84% |

Although Research & Development records the highest number of attritions, **Sales has the highest attrition rate**.

---

## 4. Job Satisfaction vs Attrition

### Hypotheses

**H₀:** Mean job satisfaction is equal between attrited and retained employees.

**H₁:** Mean job satisfaction differs between the two groups.

### Statistical Test

**Welch's Independent Samples t-test**

### Result

- t-statistic = **-3.93**
- p-value ≈ **0.0001**

### Decision

Reject **H₀**.

Average job satisfaction differs significantly between employees who left and those who remained.

### Satisfaction Comparison

| Employee Group | Average Job Satisfaction |
|---------------|-------------------------:|
| Attrited | 2.47 |
| Retained | 2.78 |

Employees who left reported lower average job satisfaction.

---

# 📋 Statistical Results Summary

| Business Question | Statistical Test | Result | Significant? |
|-------------------|------------------|--------|--------------|
| Overtime vs Attrition | Chi-Square Test | χ² = 87.56, p < 0.001 | ✅ Yes |
| Monthly Income vs Attrition | Welch's t-test | t = -7.48, p < 0.001 | ✅ Yes |
| Department vs Attrition | Chi-Square Test | χ² = 10.80, p = 0.0045 | ✅ Yes |
| Job Satisfaction vs Attrition | Welch's t-test | t = -3.93, p ≈ 0.0001 | ✅ Yes |

These statistical findings provide quantitative evidence supporting the patterns observed during exploratory data analysis.

---

# 💡 Key Findings

### Overtime

Employees working overtime exhibit significantly higher attrition than employees who do not work overtime.

### Monthly Income

Employees who left the organization have considerably lower average and median monthly income.

### Department

Sales records the highest attrition rate, while Research & Development records the largest number of attritions due to its larger workforce.

### Job Satisfaction

Employees who left the organization report lower average job satisfaction than retained employees.

---

# 📋 Business Recommendations

1. **Review overtime-heavy roles** to improve work-life balance and reduce burnout.

2. **Evaluate compensation competitiveness** for employee groups experiencing higher attrition.

3. **Prioritize retention strategies within the Sales department**, where the attrition rate is highest.

4. **Monitor employee satisfaction regularly** through engagement surveys and feedback programs.

5. **Consider multiple workforce indicators together**, including overtime, income, department, job satisfaction, tenure, and job role when developing retention strategies.

---

# 📖 Important Statistical Note

Statistical significance indicates that the observed relationships are unlikely to be explained by random sampling variation under the null hypothesis.

However, these analyses demonstrate **association or group differences—not causation**.

For example, the results support a statistically significant association between overtime and employee attrition, but they do not prove that overtime directly causes employees to leave.

---

# ⭐ Project Features

- End-to-End Exploratory Data Analysis (EDA)
- Statistical Hypothesis Testing
- Chi-Square Test of Independence
- Welch's Independent Samples t-test
- Correlation Analysis
- Business Interpretation of Statistical Results
- Workforce Analytics
- Employee Attrition Analysis
- Data-Driven Business Recommendations

---

# 📁 Project Structure

```text
HR-Employee-Attrition-Analysis/
│
├── Data/
│   └── HR_Attrition.csv
│
├── Notebooks/
│   └── eda_analysis.ipynb
│
├── Reports/
│   └── Visualizations/
│
├── requirements.txt
│
└── README.md
```

---

# ▶️ How to Run the Project

1. Clone this repository.
2. Install the required Python libraries from `requirements.txt`.
3. Open `eda_analysis.ipynb` in Jupyter Notebook.
4. Load the dataset from the `Data` folder.
5. Run the notebook cells sequentially.
6. Review the EDA visualizations.
7. Interpret the statistical hypothesis testing results and business recommendations.

---

# 💼 Skills Demonstrated

- Data Cleaning & Validation
- Exploratory Data Analysis (EDA)
- Statistical Hypothesis Testing
- Chi-Square Test of Independence
- Welch's Independent Samples t-test
- Correlation Analysis
- Statistical Interpretation
- Workforce Analytics
- Employee Attrition Analysis
- Pandas
- NumPy
- SciPy
- Matplotlib
- Seaborn
- Business Insight Generation
- Data-Driven Decision Making

---

# 👨‍💻 Author

**Tushar Sharma**

**Aspiring Data Analyst**

**GitHub:** `imtusharsharma-45`
