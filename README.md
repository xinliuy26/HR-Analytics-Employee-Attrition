# HR-Analytics-Employee-Attrition
### 💡 Deep Dive into Compensation Features (Advanced Analytics)

A key highlight of this project is the feature engineering around employee compensation, which revealed a nuanced relationship between absolute income and internal pay equity:

1. **`Comp_vs_Role_Avg` (Engineered Feature) | Coefficient: -0.696**
   * **Definition:** The ratio of an individual's monthly income to the average income of their specific job role (a proxy for *Internal Pay Equity*).
   * **Business Insight:** The strong negative coefficient indicates that **internal equity is a powerful retention driver**. When controlling for job roles, employees who are compensated above their peer average exhibit significantly lower attrition risk. This suggests that relative fairness within a department heavily impacts morale and long-term loyalty.

2. **`MonthlyIncome` (Original Feature) | Coefficient: +1.344**
   * **Statistical Note (Addressing Multicollinearity):** While a positive coefficient for absolute income seems counterintuitive at first glance, it highlights a classic data science phenomenon. In multi-variable modeling, `MonthlyIncome` shares high multicollinearity with `JobRole` and `TotalWorkingYears` (senior leaders earn higher absolute pay but represent a smaller, highly specific subset of the workforce).
   * **Actionable Takeaway:** This tension proves that **relative pay competitiveness (`Comp_vs_Role_Avg`) is a cleaner, more predictive signal for employee retention** than absolute numbers alone. HR leaders looking to optimize retention spend should prioritize fixing internal pay gaps over implementing blanket salary increases.
