# HR Attrition — EDA & Hypothesis Testing

## Business Problem
Company mein employee attrition rate high hai. Kaunse factors (OverTime, Income, Department, Job Satisfaction) attrition ko significantly drive karte hain, aur HR retention strategy kaise design kare?

## Dataset
IBM HR Analytics Employee Attrition dataset — 1470 employees, 35 features.
Source: https://github.com/IBM/employee-attrition-aif360

## Approach
1. Data cleaning & overview
2. Univariate + Bivariate EDA
3. Hypothesis testing (t-test, chi-square)
4. Business insights & recommendations

## Key Findings

| # | Question | Test | Result | Significant? |
|---|---|---|---|---|
| 1 | OverTime vs Attrition | Chi-square | Chi2=87.56, p<0.0001 | ✅ Yes |
| 2 | MonthlyIncome vs Attrition | t-test | T=-7.48, p<0.0001 | ✅ Yes |
| 3 | Department vs Attrition | Chi-square | Chi2=10.80, p=0.0045 | ✅ Yes |
| 4 | JobSatisfaction vs Attrition | t-test | T=-3.93, p=0.0001 | ✅ Yes |

## Insights & Recommendations

**1. OverTime is the strongest attrition driver**
Attrition rate ~30% (OverTime) vs ~10% (No OverTime). Recommendation: workload redistribution or comp adjustment for overtime-heavy roles.

**2. Low income correlates with higher attrition**
Median income of attrited employees (₹3,202) is ~38% lower than retained employees (₹5,204). Recommendation: salary benchmarking for entry-level bands and retention bonuses.

**3. Sales department has the highest attrition**
Department significantly affects attrition (p=0.0045), with Sales showing the highest rate. Recommendation: targeted retention programs for Sales.

**4. Job satisfaction is a leading indicator**
Attrited employees report lower average satisfaction (2.47 vs 2.78 on a 1-4 scale). Recommendation: regular pulse surveys to catch early warning signs.

## Conclusion
Attrition is driven by a combination of workload, compensation, department culture, and employee engagement — not a single cause. A multi-pronged retention strategy addressing all four factors is recommended.

## Structure
```
hr-attrition-eda/
├── data/HR_Attrition.csv
├── notebooks/eda_analysis.ipynb
├── src/
├── outputs/charts/
└── requirements.txt
```

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy (stats)
