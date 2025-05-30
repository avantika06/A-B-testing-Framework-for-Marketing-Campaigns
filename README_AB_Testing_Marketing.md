
# A/B Testing Framework for Marketing Campaigns

This project implements an A/B testing framework to evaluate the effectiveness of digital ad campaigns, leveraging statistical analysis and data visualization techniques to simulate real-world marketing experiments.

## 📈 Project Overview

The dataset contains user-level data divided into two groups:

- **Experimental Group**: Exposed to digital ads.
- **Control Group**: Shown a Public Service Announcement (PSA) or no ads at all.

The primary goals:

1. **Campaign Success**: Determine if the ad campaign significantly increased conversions.
2. **Attributable Impact**: Quantify how much of the observed success can be directly attributed to the ad campaign.

---

## 🔍 Dataset

The dataset includes the following features:

| Column Name         | Description                                                                          |
|---------------------|--------------------------------------------------------------------------------------|
| `id`                | User ID (unique)                                                                     |
| `test_group`        | Group assignment: "ad" (experimental) or "psa" (control)                              |
| `converted`         | Conversion status: `True` if user converted, `False` otherwise                        |
| `total_ads`         | Total number of ads seen by the user                                                 |
| `most_ads_day`      | Day of the week when the user saw the highest number of ads                           |
| `most_ads_hour`     | Hour of the day when the user saw the highest number of ads                           |

---

## ⚙️ Methods and Analysis

Key steps in the analysis:

✅ **Data Exploration & Cleaning**  
- Inspected group distributions and potential imbalances.  
- Verified data types and handled missing values.

✅ **Conversion Rate Analysis**  
- Calculated conversion rates for the `ad` group and the `psa` group.  
- Experimental group conversion rate: **2.55%**  
- Control group conversion rate: **1.79%**

✅ **Hypothesis Testing**  
- Conducted **T-tests** and **Chi-squared tests** to confirm statistical significance of the observed uplift.  
- T-statistic and p-value indicate a significant positive effect of ads on conversions.

✅ **Visualizations**  
- Created bar plots to compare conversion rates by group, day of the week, and hour of the day.  
- Developed heatmaps to visualize conversion patterns.

---

## 📊 Key Findings

- The **experimental group (ad)** showed a **2.55% conversion rate**, while the **control group (psa)** had **1.79%**, confirming a significant positive impact of ads.  
- Statistical tests provided strong evidence (p-value < 0.05) that ads significantly improve conversion rates.  
- Notable variations in conversion rates by day of the week, suggesting temporal effects in ad campaign performance.

---

## 💻 Technologies Used

- **Python**: Data analysis and statistical testing (Pandas, NumPy, Statsmodels)  
- **Matplotlib / Seaborn**: Visualizations  
- **Jupyter Notebook**: Interactive data exploration and documentation

---

## 📁 How to Use

1. Clone this repository:  
   ```bash
   git clone https://github.com/avantika06/A-B-testing-Framework-for-Marketing-Campaigns.git
   cd ab-testing-marketing
   ```

2. Launch Jupyter Notebook:  
   ```bash
   jupyter notebook
   ```

3. Open the `ABtesting-Marketing.ipynb` notebook to view the step-by-step analysis and visualizations.

---

## 🚀 Future Work

- Incorporate more granular user-level data (demographics, past purchases) for deeper insights.  
- Explore uplift modeling and Bayesian methods for robust causal inference.  
- Test different ad variations and personalization strategies.

---
