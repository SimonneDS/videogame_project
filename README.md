# Analysis of Success Patterns in the Global Video Game Market

## Business Objective

This project was developed for the online store **Ice** to conduct a strategic analysis of the global video game market.

The main goal is to **identify key success patterns** (platform, genre, region, score) that will allow the company to:

1.  **Detect promising projects** with high sales potential.
2.  **Plan and optimize advertising campaigns** for 2017, maximizing Return on Investment (ROI).

## ✨ Key Results and Impact

A **robust Exploratory Data Analysis (EDA)** was executed, focusing on the current period, and statistical techniques were applied to validate critical market hypotheses:

* **Identification of Vital Platforms:** Platforms with the **longest lifespan** and the **highest revenue volume** in the recent period (starting from 2013) were determined, enabling the company to focus advertising investment on the ecosystems with the most traction.
* **Geographic Segmentation:** The **top five most popular genres and platforms per region (NA, EU, JP)** were identified, revealing unique preferences for a localized marketing strategy.
* **Statistical Validation (Hypothesis Testing):** **Student's t-tests** were applied to confirm whether user and critic scores had a significantly different impact on sales, providing an empirical basis for the weight to be given to reviews in advertising campaigns.

## 🛠️ Technologies and Stack

| Category | Tool | Specific Use |
| :--- | :--- | :--- |
| **Language** | `Python` | Data analysis, cleaning, and modeling. |
| **Manipulation** | `Pandas`, `NumPy` | Preprocessing, handling missing values, and matrix calculations. |
| **Visualization** | `Matplotlib` | Creation of data distribution charts (histograms, boxplots) for decision-making. |
| **Statistics** | `SciPy` | Application of statistical hypothesis testing (Student's t-test) to validate assumptions. |
| **Environment** | `Jupyter Notebook` | Documentation of the workflow and presentation of results. |

## 💡 Code Highlights

* **Critical Missing Data Handling:** A strategy was implemented for handling `NaN` values and the string `'tbd'` (to be determined) in user scores, converting them to null values to allow for the calculation of means and the application of statistical analysis without bias.
* **Strategic Time Filtering:** The dataset was defined and filtered to a **relevant analysis period** (starting from 2013), which is crucial for not basing 2017 predictions on outdated platform data.
* **Solid Hypothesis Testing:** The `scipy.stats.ttest_ind` function was implemented with the parameter `equal_val=False` (unequal variances) to perform hypothesis tests with greater precision, a key technique for the robustness of the analysis.