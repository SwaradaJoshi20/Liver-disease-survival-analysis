## Overview
This project analyzes survival rates in patients with Primary Biliary Cirrhosis (PBC) using statistical and machine learning techniques. The goal is to identify key factors influencing survival and build predictive models. The analysis applies Kaplan-Meier estimation, Cox Proportional Hazards regression, and Random Forest classification to a classic dataset from the Mayo Clinic.

## Dataset
The dataset is from the Mayo Clinic PBC study. It includes 418 patients and features:
- `time`: Survival time in days.
- `status`: Event indicator (0=censored, 1=transplant, 2=dead).
- `trt`: Treatment code (1=DPCA, 2=Placebo).
- Prognostic variables: `age`, `sex`, `bili` (bilirubin), `albumin`, `protime`, `stage`, etc.

**Please see the [Data Directory README](data/README.md) for detailed instructions on obtaining the dataset.**

## Methodology
1.  **Data Preprocessing:** Handled missing values, feature engineering, outlier detection.
2.  **Statistical Analysis:**
    - **Kaplan-Meier Estimator** for overall and gender-stratified survival curves.
    - **Log-Rank Test** to compare survival between groups (p-value = 0.0026).
    - **Cox Proportional Hazards Model** (C-Index: 0.95) to identify significant predictors.
    - **Weibull Survival Model** to model the time-dependent hazard rate.
3.  **Machine Learning:** A **Random Forest Classifier** was built to predict survival status, achieving 99.24% accuracy.

## Key Results
- **Gender Imbalance:** The disease predominantly affects females (88.5% of the cohort).
- **Gender Disparity:** Female patients exhibited significantly better survival probabilities than males.
- **Key Predictors:** Bilirubin, albumin, and platelet count were among the most significant predictors of survival.
- **Treatment Ineffectiveness:** The drug D-Penicillamine showed no significant effect on bilirubin levels compared to a placebo.
- **Model Performance:** The Random Forest model outperformed Logistic Regression, handling class imbalance effectively.

| Model | Accuracy | Notes |
| :--- | :--- | :--- |
| Logistic Regression | Low | Failed to predict minority class |
| **Random Forest** | **99.24%** | **Well-balanced precision & recall** |

## 🛠️ Installation & Usage

1.  **Obtain the Data:** Follow the instructions in `data/README.md`.
2.  **Run the Analysis:** Execute the Jupyter notebooks in sequence:
    - Liver-Disease-Survival-Analysis\Notebooks\Liver Data preprocessing.ipynb
    - Liver-Disease-Survival-Analysis\Notebooks\Liver Data analysis.ipynb
    - Liver-Disease-Survival-Analysis\Notebooks\Liver Survival analysis.ipynb
    - Liver-Disease-Survival-Analysis\Notebooks\Liver ML model.ipynb

## Authors

- [Swarada Joshi](https://github.com/SwaradaJoshi20)
- [Vedant Dusing](https://github.com/VedantRD007)


- [Vedant Dusing](https://github.com/)
