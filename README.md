# A/B Test – Landing Page Experiment

## Project Overview

This project analyzes the results of an **A/B test on a landing page**, comparing two versions, **A and B**, to determine whether there are meaningful differences in user behavior and business performance.

The analysis focuses on conversion rate, average spending, traffic sources, and user type. Statistical tests were applied to determine whether the observed differences are statistically significant and to support data-driven business decisions.

---

## 🎯 Project Objective

The main objective is to evaluate the performance of landing page versions **A and B** and identify which version shows better observed results under the experiment conditions.

The analysis answers the following questions:

* Is there a difference in average spending between users exposed to versions A and B?
* Is there a difference in conversion rate?
* Is conversion related to the traffic source?
* Is conversion related to user type?
* Are the observed differences statistically significant?
* What insights can be used to support business decisions?

---

## 📊 Dataset

The project uses the `landing_experiment.csv` dataset.

Main variables:

| Variable    | Description                              |
| ----------- | ---------------------------------------- |
| `region`    | User's geographic region                 |
| `device`    | Device used by the user                  |
| `source`    | Traffic source                           |
| `user_type` | New or returning user                    |
| `converted` | Whether the user converted               |
| `gasto`     | Amount spent                             |
| `landing`   | Landing page version: A or B             |
| `date`      | Date associated with the user/experiment |

---

## 🔎 Methodology

### 1. Data Exploration and Validation

The dataset was initially reviewed to:

* Check data types
* Identify missing values
* Detect potential inconsistencies
* Convert variables to appropriate data types
* Understand the distribution of the main variables

For example:

* `converted` was converted to Boolean.
* `date` was converted to datetime format.
* Missing values and potential data-quality issues were reviewed before the analysis.

### 2. Average Spending – A vs. B

The average spending of users who converted was compared between landing pages A and B.

A **Welch's independent samples t-test** was used because the groups are independent and the analysis does not assume equal variances.

**Hypotheses:**

* H₀: There is no difference in average spending between groups A and B.
* H₁: There is a difference in average spending between groups A and B.

### 3. Conversion Rate – A vs. B

Conversion rates were calculated for each landing page and compared using a **two-proportion z-test**.

Results:

* Landing A: **12.57%**
* Landing B: **15.96%**
* Difference: **3.38 percentage points**

The statistical test produced a p-value of approximately **3.76 × 10⁻²²**, providing strong statistical evidence of a difference in conversion rates between the two versions.

### 4. Traffic Source vs. Conversion

A **Chi-square test of independence** was used to evaluate whether conversion is associated with the user's traffic source.

Observed conversion rates:

| Traffic Source | Conversion Rate |
| -------------- | --------------: |
| Email          |           14.9% |
| Ads            |           14.7% |
| Referral       |           13.8% |
| Organic        |           13.7% |

The test produced a p-value of approximately **0.034**, indicating statistical evidence of an association between traffic source and conversion.

However, the difference between the highest and lowest conversion rates is relatively small, around **1.2 percentage points**.

### 5. User Type vs. Conversion

A second **Chi-square test of independence** was performed to determine whether conversion is associated with user type.

Observed conversion rates:

* New users: **14.30%**
* Returning users: **14.09%**
* Difference: **0.21 percentage points**

The p-value was approximately **0.473**.

Therefore, there is not enough statistical evidence to conclude that conversion is associated with user type in this dataset.

---

## 📈 Visualizations

Several visualizations were created to better understand the data, including:

* Converted vs. non-converted users by traffic source
* Conversion proportions by traffic source
* Conversion proportions by user type
* Comparisons between landing page versions
* Spending distributions

The visual analysis was used together with statistical testing rather than as a replacement for it.

---

## 💡 Key Findings

### Landing Page

Landing page B showed:

* Higher average spending among users who converted.
* A conversion rate of **15.96%**, compared with **12.57%** for A.
* A difference of **3.38 percentage points** in conversion rate.

The statistical tests provide evidence that the differences observed between the two landing page versions are statistically significant.

### Traffic Source

Traffic source shows a statistically significant association with conversion, although the differences in conversion rates between sources are relatively small.

This suggests that traffic volume, acquisition costs, and revenue generated by each channel should also be considered before making business decisions.

### User Type

New and returning users have very similar conversion rates. The statistical test did not provide sufficient evidence of an association between user type and conversion.

---

## 🚀 Business Recommendations

Based on the analysis, the following actions could be considered:

1. **Investigate the elements of Landing B** that may be contributing to its higher conversion rate.
2. Analyze the economic performance of each traffic source, including acquisition cost and revenue.
3. Further segment the experiment results by **device, region, and traffic source**.
4. Analyze user behavior beyond conversion to identify possible differences between segments.
5. Continue monitoring the landing page results with additional experiments before making long-term decisions.

A statistically significant result does not necessarily mean that the business impact is large. Both **effect size and economic impact** should be considered when making decisions.

---

## 🛠️ Technologies & Tools

![Python](https://img.shields.io/badge/Python-3776AB?style=flat\&logo=python\&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat\&logo=pandas\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat\&logo=numpy\&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat\&logo=scipy\&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat\&logo=jupyter\&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat\&logo=microsoftexcel\&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat\&logo=git\&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat\&logo=github\&logoColor=white)

### Main Technologies

* **Python** – Data analysis and statistical analysis
* **Pandas** – Data manipulation and exploration
* **NumPy** – Numerical operations
* **SciPy** – Statistical testing
* **Statsmodels** – Statistical analysis
* **Matplotlib & Seaborn** – Data visualization
* **Jupyter Notebook** – Data analysis workflow
* **Excel** – Data review and analysis
* **Git & GitHub** – Version control and portfolio management
* **AI tools** – Research, debugging, documentation, and analysis support

---

## 🧠 Skills Demonstrated

### Technical Skills

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Data Manipulation
* Statistical Hypothesis Testing
* A/B Testing
* Conversion Rate Analysis
* Data Visualization
* Business Analytics
* Python & Pandas
* SQL/Excel-oriented analytical thinking

### Soft Skills

* Analytical Thinking
* Problem Solving
* Critical Thinking
* Attention to Detail
* Business-Oriented Thinking
* Data-Driven Decision Making
* Communication of Technical Findings
* Translating Business Questions into Data Analysis

---

## 📁 Project Structure

```text
landing_experiment_data_analysis/
│
├── datasets/
│   └── landing_experiment.csv
│
├
├── S9 Version_Landing_Experiment.ipynb
│
├── README.md
```

---

## 📌 Conclusion

This project demonstrates how data analysis and statistical testing can be combined to evaluate an A/B experiment.

The analysis found statistically significant differences between landing page versions in terms of **conversion rate and average spending among converted users**. Traffic source also showed a statistical association with conversion, while user type did not show sufficient evidence of an association.

The project highlights the importance of combining **statistical evidence, effect size, visualization, and business context** when interpreting experimental results.

---

## 🏷️ Tags

`Python` `Pandas` `Data Analysis` `A/B Testing` `Statistics` `Data Visualization` `SciPy` `Seaborn` `Matplotlib` `Excel` `Business Analytics` `Jupyter` `GitHub` `AI`
