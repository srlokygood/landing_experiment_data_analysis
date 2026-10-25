# Landing Page B Lifts Conversion by 3.4 Points in an A/B Test

An A/B test compared two landing page versions on conversion rate, spending, traffic source, and user type. Landing B converted at **15.96%** versus **12.57%** for Landing A, a **3.38 percentage point** lift that is statistically significant (p ≈ 3.76 × 10⁻²²).

![Main dashboard](images/dashboard.png)

## Business Question

Which landing page version performs better, and do traffic source or user type influence conversion? The answer determines which version to keep and where to focus further optimization.

## Data

- **Source:** `landing_experiment.csv` (number of records and date range not stated).
- **Files:** `datasets/landing_experiment.csv`, `S9 Version_Landing_Experiment.ipynb`.
- **Variables:**

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

## Process

- **Cleaning and transformation (pandas):** checked data types and missing values, converted `converted` to Boolean and `date` to datetime, and reviewed the distributions of the main variables.
- **Data model:** a single flat table (no star schema).
- **Statistical tests:**
  - Welch's t-test for average spending among converted users (A vs. B).
  - Two-proportion z-test for conversion rate (A vs. B).
  - Chi-square test of independence for traffic source vs. conversion.
  - Chi-square test of independence for user type vs. conversion.
- **Visualizations:** conversion by traffic source and user type, A vs. B comparisons, and spending distributions.

## Findings

1. Landing B converted at **15.96%** versus **12.57%** for A, a difference of **3.38 percentage points** (p ≈ 3.76 × 10⁻²²).
2. Traffic source is associated with conversion (p ≈ 0.034), but the gap between Email (14.9%) and Organic (13.7%) is only about **1.2 percentage points**.
3. User type is not associated with conversion: New 14.30% vs. Returning 14.09% (**0.21 pp** difference, p ≈ 0.473).

## Recommendations

- Investigate which elements of Landing B drive its higher conversion.
- Compare traffic sources by acquisition cost and revenue, not just conversion rate.
- Segment results by device, region, and traffic source.
- Run additional experiments before making long-term decisions.

## Limitations

- A statistically significant result does not mean the business impact is large. Effect size and economic impact must also be considered.
- The data has no acquisition cost or revenue per channel, so channel profitability cannot be concluded.
- Device and region effects were not analyzed.
- Experiment design details (randomization, duration, sample sizes) are not documented.

## How to Open It

- Install the dependencies from `requirements.txt`.
- Open `S9 Version_Landing_Experiment.ipynb` in Jupyter Notebook.
- The dataset is in `datasets/landing_experiment.csv`.

## Tools

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

Python (pandas, NumPy, SciPy, Statsmodels), Matplotlib, Seaborn, Jupyter Notebook, Excel, Git & GitHub

## Tags

`Python` `Pandas` `Data Analysis` `A/B Testing` `Statistics` `Data Visualization` `SciPy` `Seaborn` `Matplotlib` `Excel` `Business Analytics` `Jupyter` `GitHub` `AI`
