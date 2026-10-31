# Data Analysis on Solid Waste Management (Pune Case Study)

An exploratory data analysis (EDA) project evaluating ward-level solid waste generation, household distributions, and per-capita burdens across Pune using Python.

---

## 📌 Project Overview
Managing municipal solid waste effectively requires understanding not just aggregate waste volumes, but also how waste generation correlates with population density and household distributions at the ward level. This project analyzes municipal waste data for Pune to uncover key distributional insights, identify high-burden outlier wards, and categorize wards into actionable operational quadrants.

---

## 📊 Dataset Description
The analysis is based on municipal ward data (`PUNE-SW.csv`) containing the following key attributes:
* **City Name:** Municipal jurisdiction (`Pune`)
* **Zone Name:** Administrative zone classification
* **Ward Name:** Specific administrative ward identifier
* **Number of HH:** Total count of households in the ward
* **Waste Quantity (Tonnes Per Day):** Total waste generated daily
* **No. of Households with Waste Segregation:** Count of households practicing waste segregation

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 
* **Environment:** Jupyter Notebook (`conda env:base`)
* **Core Libraries:**
  * `pandas` (Data loading, aggregation, and cleaning)
  * `numpy` (Numerical operations and statistical metrics)

---

## 📈 Key Analysis & Steps Performed

1. **Data Inspection & Cleaning:**
   * Loaded and verified the dataset (`42` rows, `6` columns).
   * Inspected summary statistics (mean total waste $\approx 37.92$ tonnes/day; mean households $\approx 102,243$).
   * Checked for missing values and formatted numerical features.

2. **Feature Engineering & Normalization:**
   * Calculated normalized metrics such as **Waste per Household (kg/day)** to evaluate per-capita burden independently of total ward population size.

3. **Exploratory Data Analysis (EDA) & Correlations:**
   * **Correlation Insights:** Uncovered a weak linear correlation between household count and total waste ($r \approx 0.043$), and a negative correlation between household count and waste-per-household ($r \approx -0.693$).
   * **Outlier Detection:** Identified high-value outliers using IQR metrics, highlighting wards with disproportionately high per-household waste burdens (e.g., *Kondhwa Khurd-Mittha Nagar*, *Janta Vasahat-Duttawadi*, and *Warje-Malwadi*).
   * **Ward Categorization Matrix:** Segmented the 42 wards across quadrants comparing total waste volume against per-household waste intensity.

---

## 💡 Key Findings
* **Volume vs. Density Mismatch:** Wards with massive populations do not automatically generate proportional waste increases, proving that consumption behaviors and commercial density play major roles.
* **Outlier Identification:** Specific wards experience heavy per-household waste generation, pointing toward localized operational challenges that require targeted policy interventions.

---

## 🚀 Getting Started & Replication

To run this notebook locally on your machine:

1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
   ```
2. Navigate to the project directory and open JupyterLab:

```Bash
jupyter lab
```
3. Open
   `Data Analysis on Solid Waste Management.ipynb` and run the cells. (Note: Ensure your dataset path points correctly to your local PUNE-SW.csv file).
