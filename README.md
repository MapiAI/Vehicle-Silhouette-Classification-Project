# 🚗 Vehicle Silhouette Classification Project

<p align="left"> 
<img src="https://img.shields.io/badge/Python-3.10-blue" /> 
<img src="https://img.shields.io/badge/Status-Completed-brightgreen" /> 
<img src="https://img.shields.io/badge/Model-F1%20Optimized-orange" /> 
<img src="https://img.shields.io/badge/Category-Machine%20Learning-lightgrey" /> 
</p>

A supervised machine learning project focused on classifying vehicles based solely on geometric features extracted from their silhouettes.  
This repository contains the full workflow: data exploration, preprocessing, model training, evaluation, cross-validation, stacking, and comparative analysis across multiple algorithms. Everything is implemented inside a single, well-structured Jupyter Notebook.

## 📘 Project Description

This project explores how geometric silhouette features can be used to classify vehicles into three categories:

- **Car**
- **Van**
- **Bus**

The dataset contains numerical descriptors extracted from the outline of each vehicle, captured from different angles. These features encode geometric properties such as compactness, circularity, aspect ratios, rectangularity, variance measures, skewness, and hollows ratio.

The goal is to build a supervised machine learning model capable of predicting the correct vehicle class based solely on these silhouette-based measurements.

## 🌟 Project Highlights

- Full end‑to‑end supervised machine learning pipeline
- Extensive Exploratory Data Analysis with visual and statistical insights
- Robust preprocessing: imputation, scaling, encoding, redundancy analysis
- Evaluation of multiple model variants (basic + regularized)
- Ensemble methods (Random Forest, Gradient Boosting, XGBoost) among top performers
- Assessment of cross‑validation and stacking to determine their usefulness for this task
- Detailed confusion matrices (3×3 and pairwise 2×2)
- Clean, reproducible, and well‑structured repository

## 📦 Dataset

Dataset used: *Vehicle Silhouettes Dataset* (Kaggle)  
🔗 https://www.kaggle.com/datasets/rajansharma780/vehicle

### Target variable
- `class` → {car, van, bus}

### Feature set
Numerical geometric descriptors including:

compactness, circularity, distance_circularity, radius_ratio, pr.axis_aspect_ratio, max.length_aspect_ratio, scatter_ratio, elongatedness, pr.axis_rectangularity, max.length_rectangularity, scaled_variance, scaled_radius_of_gyration, skewness_about (x3), hollows_ratio.

## 🎯 Business Problem

A chain of car repair shops requested a model capable of identifying the type of vehicle based on its silhouette.  
The task is a **multiclass classification problem**: predict whether a silhouette corresponds to a car, van, or bus.

This model could support automated intake systems, vehicle identification pipelines, or pre‑processing stages in computer vision workflows.

## 🧭 Project Workflow

All steps are implemented inside a single Jupyter Notebook (`VehiclesilhouetteClassificationProject.ipynb`), organized into clear sections.

1. **Data Loading and Initial Inspection**
2. **Data Cleaning and Preprocessing**
3. **Exploratory Data Analysis (EDA)**
4. **Feature Redundancy Analysis**
5. **Train/Test Split**
6. **Model Training**
7. **Model Evaluation**
8. **Cross‑Validation Assessment**
9. **Stacking Assessment**
10. **Conclusions**

## 📊 Results Summary

Ensemble methods such as **Random Forest**, **Gradient Boosting**, and **XGBoost** consistently achieved the highest F1‑scores and ROC AUC values.  
Margin‑based models (**SVM**, **Logistic Regression**) also performed strongly.  
Simpler models like **Decision Tree** and **kNN** showed lower generalization.  

A stacking ensemble was also evaluated, achieving performance comparable to the best individual models.  
Most misclassifications occurred in the **car–van boundary**, the most challenging separation.

## 📁 Repository Structure

- README.md
- requirements.txt
- .gitignore
- data/  (empty)
- notebooks/
    - vehicle_silhouette_classification.ipynb
- results/
    - confusion_matrices/
    - metrics_summary.csv
    - plots/


## 👩‍💻 About the Author

This project was developed by **Maria Petralia (MaPi)** as part of her Data Science & AI training journey.  
With a background in Computer Science and experience in software and data solutions, she focuses on building clear, rigorous, and well‑documented machine learning workflows.

- GitHub: https://github.com/MapiAI  
- LinkedIn: https://www.linkedin.com/in/mariapetralia/
