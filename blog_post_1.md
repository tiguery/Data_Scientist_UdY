# What Drives Developer Salary and Job Satisfaction Around the World?
*2025-10-25*

**Data.** I analyzed the global **Stack Overflow Developer Survey 2024** (CSV) to explore how country, experience, work mode, and employment relate to compensation and job satisfaction. I filtered to respondents with non-missing salary and satisfaction, and kept salaries between **$5,000 and $500,000** to remove obvious outliers.

**Q1 – Which countries report the highest average developer salaries?**  
A bar chart of the **Top 10 countries** shows that mature tech markets (e.g., U.S., Switzerland, Australia) tend to lead, while emerging markets lag. Country explains a large chunk of pay differences.

**Q2 – Is coding experience related to salary?**  
A scatter with a regression line shows a clear **positive trend**: more professional years usually means higher pay. There’s wide spread, indicating factors beyond experience also matter.

**Q3 – How does remote work affect satisfaction?**  
A boxplot of **JobSatisfaction** by remote status shows a **slightly higher median** for remote-heavy roles, though distributions overlap. Flexibility appears to help, but it’s not the only driver.

**Q4 – Do full-time employees earn more than contractors or self-employed developers?**  
A salary-by-employment-type boxplot shows **full-time and contractors** on top on average, with part-time and students lower.

**Q5 – Is higher salary always linked to higher job satisfaction?**  
A scatter of satisfaction vs salary suggests a **mild positive relationship**—money helps, but isn’t everything. Some highly paid devs still report middling satisfaction.

**Mini Model.** A small linear regression (using years of experience, country, employment, and remote status) achieves reasonable **R²/MAE** on a holdout. A simple scenario—**+5 years experience**—lifts the predicted salary, consistent with Q2’s trend.

**Takeaway.** Five simple visuals tell a clear story: **country, experience, and work mode** shape compensation and satisfaction—but personal fit and role context still matter.
