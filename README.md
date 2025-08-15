# Stars, Galaxies, and Quasars Classification Model

## Overview

This project implements a machine learning model to classify astronomical objects — **Stars**, **Galaxies**, and **Quasars** — based on observational data from the **Sloan Digital Sky Survey (SDSS)**. The dataset contains **10,000 observations**, each described by **17 feature columns** and a target class.

The primary goal is to build a predictive model that can accurately distinguish between different types of celestial objects using photometric and positional data.

---

## Dataset

* **Source:** [Sloan Digital Sky Survey (SDSS) — Kaggle Dataset](https://www.kaggle.com/datasets/lucidlenn/sloan-digital-sky-survey)
* **Size:** 10,000 samples
* **Split:** 70% training, 30% testing
* **Features:**

  * `ra`, `dec` — Right Ascension and Declination
  * `u`, `g`, `r`, `i`, `z` — Photometric system magnitudes
  * `run`, `rerun`, `camcol`, `field` — Image field descriptors
  * `redshift` — Wavelength shift due to motion
  * `plate` — Plate number
  * `mjd` — Modified Julian Date
  * `fiberid` — Optical fiber ID

**Preprocessing:**

* Dropped non-informative ID columns
* Verified no missing data
* Encoded target classes numerically

---

## Methodology

1. **Data Preprocessing**

   * Removed unused identifier columns (`objid`, etc.)
   * Normalized features where required
   * Converted categorical labels to numeric form

2. **Model Training**

   * Implemented multiple classifiers:

     * Decision Tree Classifier
     * Logistic Regression
     * K-Nearest Neighbors (KNN)
   * Tuned hyperparameters for optimal accuracy

3. **Evaluation Metrics**

   * Accuracy Score
   * Recall
   * Precision
   * F1 Score

---

## Results

| Classifier          | Accuracy | Recall (Macro) | F1 Score (Macro) | F1 Score (Weighted) |
| ------------------- | -------- | -------------- | ---------------- | ------------------- |
| Decision Tree       | 0.990000 | 0.975708       | 0.980987         | 0.989932            |
| Logistic Regression | 0.976000 | 0.968090       | 0.971192         | 0.975966            |
| Nearest Neighbor    | 0.907333 | 0.898056       | 0.911480         | 0.907247            |
| SVM                 | 0.953333 | 0.945222       | 0.953278         | 0.953326            |


---

## References

* Sloan Digital Sky Survey (SDSS) — [https://www.sdss.org](https://www.sdss.org)
* Kaggle Dataset — [Sloan Digital Sky Survey Dataset](https://www.kaggle.com/datasets/lucidlenn/sloan-digital-sky-survey)
