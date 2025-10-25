# What Drives Developer Salary and Job Satisfaction Around the World?
*2025-10-25*

**Data.** I analyzed the global **Stack Overflow Developer Survey 2025** (CSV) to explore how country, experience, work mode, and employment relate to compensation and job satisfaction. I filtered to respondents with non-missing salary and satisfaction, and kept salaries between **$5,000 and $260,000** to remove obvious outliers.

**Q1 – Which countries report the highest average developer salaries?**  
A bar chart of the **Top 10 countries** shows that the 3 mature tech markets: U.S., Switzerland, and Israel take the lead while emerging markets lag. Country explains a large chunk of pay differences. However, the highest salaries are reserved for nomadic developers, those who work remotely anywhere in the world without a fixed country.

<img width="884" height="484" alt="image" src="https://github.com/user-attachments/assets/d8761c88-001e-4226-8bdc-ff4c1ea42e21" />

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>SalaryUSD</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Nomadic</td>
      <td>150788.571429</td>
    </tr>
    <tr>
      <th>1</th>
      <td>United States of America</td>
      <td>145991.694460</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Switzerland</td>
      <td>137687.328947</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Israel</td>
      <td>128875.542857</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Mauritania</td>
      <td>121570.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Ireland</td>
      <td>119229.873950</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Singapore</td>
      <td>112083.130435</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Luxembourg</td>
      <td>111683.466667</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Australia</td>
      <td>103770.644592</td>
    </tr>
    <tr>
      <th>9</th>
      <td>United Kingdom of Great Britain and Northern I...</td>
      <td>103741.316949</td>
    </tr>
  </tbody>
</table>
</div>

**Q2 – Is coding experience related to salary?**  
A scatter with a regression line shows a clear **positive trend**: more professional years usually means higher pay. There’s wide spread, indicating factors beyond experience also matter.

<img width="784" height="484" alt="image" src="https://github.com/user-attachments/assets/e3201b95-b086-4940-8a09-053bc15acc3b" />

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>YearsCodePro</th>
      <th>SalaryUSD</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>YearsCodePro</th>
      <td>1.000000</td>
      <td>0.365133</td>
    </tr>
    <tr>
      <th>SalaryUSD</th>
      <td>0.365133</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>

**Q3 – How does remote work affect satisfaction?**  
A boxplot of **JobSatisfaction** by remote status shows a **slightly higher median** for remote-heavy roles, though distributions overlap. Flexibility appears to help, but it’s not the only driver.

<img width="883" height="484" alt="image" src="https://github.com/user-attachments/assets/35ce8866-e0ae-4975-9e57-04f8f47a1a06" />

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>median</th>
    </tr>
    <tr>
      <th>RemoteWork</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Hybrid (some in-person, leans heavy to flexibility)</th>
      <td>3007</td>
      <td>7.186232</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>Hybrid (some remote, leans heavy to in-person)</th>
      <td>3111</td>
      <td>7.041787</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>In-person</th>
      <td>2030</td>
      <td>6.916749</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>Remote</th>
      <td>5579</td>
      <td>7.302384</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>Your choice (very flexible, you can come in when you want or just as needed)</th>
      <td>2077</td>
      <td>7.408281</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>nan</th>
      <td>1870</td>
      <td>7.266845</td>
      <td>8.0</td>
    </tr>
  </tbody>
</table>
</div>

**Q4 – Do full-time employees earn more than contractors or self-employed developers?**  
A salary-by-employment-type boxplot shows **full-time and contractors** on top on average, with part-time and students lower.

<img width="981" height="484" alt="image" src="https://github.com/user-attachments/assets/06626849-3f4d-4ada-b876-ebc141d21f16" />

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
      <th>median</th>
      <th>mean</th>
    </tr>
    <tr>
      <th>Employment</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Employed</th>
      <td>14913</td>
      <td>81210.0</td>
      <td>89844.974117</td>
    </tr>
    <tr>
      <th>Independent contractor, freelancer, or self-employed</th>
      <td>2231</td>
      <td>81210.0</td>
      <td>89860.974003</td>
    </tr>
    <tr>
      <th>Not employed</th>
      <td>278</td>
      <td>75410.0</td>
      <td>88675.629496</td>
    </tr>
    <tr>
      <th>Student</th>
      <td>209</td>
      <td>20883.0</td>
      <td>31745.665072</td>
    </tr>
  </tbody>
</table>
</div>

**Q5 – Is higher salary always linked to higher job satisfaction?**  
A scatter of satisfaction vs salary suggests a **mild positive relationship**—money helps, but isn’t everything. Some highly paid devs still report middling satisfaction especially starting around the $150K mark.

<img width="784" height="484" alt="image" src="https://github.com/user-attachments/assets/0ad515be-5e9c-48e2-b744-928737be6919" />

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>SalaryUSD</th>
      <th>JobSatisfaction</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>SalaryUSD</th>
      <td>1.000000</td>
      <td>0.081623</td>
    </tr>
    <tr>
      <th>JobSatisfaction</th>
      <td>0.081623</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>

**Predictive Model.** A linear regression (using years of experience, country, employment, and remote status) 
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>SalaryUSD</th>
      <th>YearsCodePro</th>
      <th>RemoteWork_Hybrid (some remote, leans heavy to in-person)</th>
      <th>RemoteWork_In-person</th>
      <th>RemoteWork_Remote</th>
      <th>RemoteWork_Your choice (very flexible, you can come in when you want or just as needed)</th>
      <th>RemoteWork_nan</th>
      <th>Employment_I prefer not to say</th>
      <th>Employment_Independent contractor, freelancer, or self-employed</th>
      <th>Employment_Not employed</th>
      <th>...</th>
      <th>Employment_Student</th>
      <th>Country_Canada</th>
      <th>Country_France</th>
      <th>Country_Germany</th>
      <th>Country_India</th>
      <th>Country_Italy</th>
      <th>Country_Netherlands</th>
      <th>Country_Poland</th>
      <th>Country_United Kingdom of Great Britain and Northern Ireland</th>
      <th>Country_United States of America</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>104413.0</td>
      <td>2.0</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>...</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>22</th>
      <td>87500.0</td>
      <td>7.0</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>...</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>25</th>
      <td>108913.0</td>
      <td>37.0</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>...</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
    </tr>
    <tr>
      <th>29</th>
      <td>205000.0</td>
      <td>19.0</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>...</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>31</th>
      <td>250000.0</td>
      <td>17.0</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>...</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
    </tr>
  </tbody>
</table>
</div>

achieves reasonable **R²/MAE** on a holdout.
R² Score: 0.49 or 49%
Mean Absolute Error: $31,405
<img width="584" height="584" alt="image" src="https://github.com/user-attachments/assets/2a117d7c-3d7a-4b23-b15c-dbac4d384436" />

A simple scenario—**+5 years experience**—lifts the predicted salary, consistent with Q2’s trend.
<img width="484" height="384" alt="image" src="https://github.com/user-attachments/assets/a3f69cea-d3a5-4463-a0a0-2d3a472b7cbe" />
Predicted increase: +$6,216

**Further analysis and validation**

<img width="784" height="384" alt="image" src="https://github.com/user-attachments/assets/94850644-15de-4b6e-bea7-4d90140b526c" />

Most residuals cluster near zero, though a few extreme salaries cause a long tail, that would be typical for salary data with wide income ranges.

<img width="798" height="484" alt="image" src="https://github.com/user-attachments/assets/ea5ae82e-870a-49b2-a08c-46108dd61650" />

Experience (YearsCodePro) has the largest positive effect, meaning each extra year adds roughly a few thousand dollars on average.
Some countries have positive coefficients (e.g., U.S. or Switzerland) — others slightly negative, reflecting real-world salary gaps.

<img width="878" height="384" alt="image" src="https://github.com/user-attachments/assets/28ba0388-db40-4a10-8f42-572271f7d427" />

Positive bars show countries with higher predicted salaries than the base (usually the first alphabetically, e.g., United Kingdom).
Negative ones indicate slightly lower expected pay, even after adjusting for experience.

**Takeaway.** Five simple visuals tell a clear story: **country, experience, and work mode** shape compensation and satisfaction—but personal fit and role context still matter.
