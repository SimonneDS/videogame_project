# Global Video Game Market Strategy: Success Pattern Analysis for Ice Store

## Executive Summary

This project was developed for the online retailer **Ice** to conduct a deep, strategic analysis of the global video game market. The primary objective was to move beyond conventional sales reporting and utilize advanced data analysis, including **statistical hypothesis testing**, to isolate the definitive factors driving game sales and platform longevity.

The resulting insights directly enable the company to:

1.  **Identify High-Potential Projects:** Accurately detect promising games and platforms for investment.
2.  **Optimize 2017 Advertising Strategy:** Develop highly localized and effective advertising campaigns, maximizing Return on Investment (ROI) based on validated market preferences.

-----

## Methodology and Statistical Validation

A robust **Exploratory Data Analysis (EDA)** was executed on historical sales data, strictly filtered to a **relevant analysis period (2013 onwards)** to prevent basing future predictions on obsolete platform cycles.

### Key Analytical Steps:

  * **Vital Platform Identification:** Determined platforms with the **longest active lifespan** and the **highest cumulative revenue volume** in the recent period, focusing investment on the most vital ecosystems.
  * **Geographic Demand Segmentation:** Identified the top five most successful genres and platforms for three major markets (**North America (NA), Europe (EU), and Japan (JP)**), which is critical for formulating localized marketing strategies tailored to unique regional preferences.
  * **Critical Data Handling:** Implemented a strategy for handling missing review scores, including **`NaN` and `'tbd'` (to be determined)** values, by converting them to nulls to ensure the integrity of subsequent mean calculations and statistical tests.

### Hypothesis Testing (Statistical Validation):

**Student's t-tests** were applied to provide empirical validation on the influence of consumer sentiment (reviews) on sales:

| Hypothesis Test | Null Hypothesis ($H_0$) | Key Finding |
| :--- | :--- | :--- |
| **User Score Impact** | User scores **do not** have a statistically significant correlation with game sales. | *Result of the t-test* |
| **Critic Score Impact** | Critic scores **do not** have a statistically significant correlation with game sales. | *Result of the t-test* |

This statistical framework provides an empirical basis for the weight to be given to user versus critic reviews in promotional efforts.

-----

## Technology Stack

| Category | Tool | Specific Use |
| :--- | :--- | :--- |
| **Language** | `Python` | Core environment for data analysis and execution. |
| **Manipulation** | `Pandas`, `NumPy` | Data wrangling, feature engineering, and high-performance matrix operations. |
| **Statistics** | `SciPy` | Application of inferential statistical techniques (Student's t-test) to validate business assumptions. |
| **Visualization** | `Matplotlib`, `Seaborn` | Creation of data distribution charts (histograms, boxplots) to support decision-making. |
| **Environment** | `Jupyter Notebook` | Documentation of the analytical workflow and presentation of findings. |

-----

## Code & Analysis Highlights

  * **Strategic Time Filtering:** The dataset was intelligently pruned to the 2013-onwards period, crucial for building a prediction model relevant to the contemporary market landscape.
  * **Robust Hypothesis Testing:** Implemented the `scipy.stats.ttest_ind` function with the parameter `equal_val=False` (unequal variances assumed) to ensure the highest possible precision in the statistical validation of score impacts on sales.
  * **Platform Lifecycle Analysis:** Detailed time-series analysis was performed to identify the platform's **"peak sales year"** and **"end-of-life"** period, providing foresight for investment timing.

-----

## How to Run the Project

1.  **Install Python dependencies:**
    ```bash
    pip install pandas numpy scipy matplotlib seaborn jupyter
    ```
2.  **Execute the Notebook:** Open and run the `video_game.ipynb` file in a Jupyter or JupyterLab environment to replicate the entire analysis and conclusions.