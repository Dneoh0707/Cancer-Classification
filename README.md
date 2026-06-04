# Cancer Classification using Gene Expression Data

## Overview

This project aims to classify cancer and non-cancer samples using gene expression data obtained from the National Center for Biotechnology Information (NCBI) Gene Expression Omnibus (GEO).

The project was conducted as part of the *Introduction to Big Data* course at Handong Global University and combines bioinformatics with machine learning techniques to explore the feasibility of cancer detection using gene expression profiles.

---

## Problem Statement

Can gene expression data be used to distinguish cancer patients from non-cancer patients?

To investigate this question, a machine learning pipeline was developed using publicly available breast cancer gene expression datasets.

---

## Dataset

Source:

* NCBI Gene Expression Omnibus (GEO)

Characteristics:

* 60 patient samples

  * 30 Cancer (CA)
  * 30 Non-Cancer (CAP)
* 20,246 gene expression features
* FPKM-normalized expression values

---

## Data Preprocessing

### Data Wrangling

* Removed independent samples for external testing
* Transposed dataset into machine learning format
* Generated binary labels

  * CA = 1
  * CAP = 0

### Dimensionality Reduction

Principal Component Analysis (PCA) was applied to reduce more than 20,000 gene features into 10 principal components.

Benefits:

* Reduced computational complexity
* Preserved major variance in the dataset
* Improved model training efficiency

---

## Machine Learning Pipeline

### Model

Decision Tree Classifier

### Workflow

Gene Expression Data
→ Data Cleaning
→ Label Generation
→ Train/Test Split
→ PCA
→ Decision Tree Training
→ Evaluation

---

## Evaluation

### Internal Test Set

* Train/Test Split: 80/20
* Accuracy: 100%

### External Validation Set

6 samples were excluded before training and used as an independent test set.

Results:

* Accuracy: 83%
* Cancer Recall: 0.67
* Cancer Precision: 1.00
* Normal Recall: 1.00
* Normal Precision: 0.75

---

## Key Findings

* Gene expression profiles contain meaningful information for cancer classification.
* PCA successfully reduced dimensionality while preserving important biological variance.
* Model performance decreased on unseen external samples, highlighting the importance of larger datasets.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* PCA
* Decision Tree Classifier

---

## My Contributions

* Data collection from GEO database
* Data preprocessing and transformation
* PCA dimensionality reduction
* Machine learning model development
* Performance evaluation and visualization
* Result interpretation and reporting

---

## Future Improvements

* Increase dataset size
* Experiment with Random Forest and XGBoost
* Apply Deep Learning approaches
* Improve external validation performance
* Explore explainable AI techniques for biological interpretation

---
## Author

Daniel Oh

Handong Global University
Life Science Major / AI Convergence Major
