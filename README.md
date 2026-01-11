{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fmodern\fcharset0 Courier;\f1\fnil\fcharset0 AppleColorEmoji;\f2\froman\fcharset0 Times-Roman;
\f3\fnil\fcharset0 Menlo-Regular;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;}
\paperw11900\paperh16840\margl1440\margr1440\vieww14780\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\partightenfactor0

\f0\fs26 \cf0 \expnd0\expndtw0\kerning0
# 
\f1 \uc0\u55357 \u56983 
\f0  Vehicle Silhouette Classification Project\
\
<p align="left"> \
<img src="https://img.shields.io/badge/Python-3.10-blue" /> \
<img src="https://img.shields.io/badge/Status-Completed-brightgreen" /> \
<img src="https://img.shields.io/badge/Model-F1%20Optimized-orange" /> \
<img src="https://img.shields.io/badge/Category-Machine%20Learning-lightgrey" /> \
</p>\
\pard\pardeftab720\partightenfactor0

\f2\fs24 \cf0 \
\pard\pardeftab720\partightenfactor0

\f0\fs26 \cf0 \
\pard\pardeftab720\partightenfactor0
\cf0 A supervised machine learning project focused on classifying vehicles based solely on geometric features extracted from their silhouettes.\
This repository contains the full workflow: data exploration, preprocessing, model training, evaluation, cross-validation, stacking, and comparative analysis across multiple algorithms. Everything is implemented inside a single, well-structured Jupyter Notebook.\
\pard\pardeftab720\partightenfactor0
\cf0 \
## 
\f1 \uc0\u55357 \u56536 
\f0  Project Description \
This project explores how geometric silhouette features can be used to classify vehicles into three categories: \
\
- **Car** \
- **Van** \
- **Bus** \
\
The dataset contains numerical descriptors extracted from the outline of each vehicle, captured from different angles. These features encode geometric properties such as compactness, circularity, aspect ratios, rectangularity, variance measures, skewness, and hollows ratio. \
\
The goal is to build a supervised machine learning model capable of predicting the correct vehicle class based solely on these silhouette\uc0\u8209 based measurements.\
\
## 
\f1 \uc0\u55356 \u57119 
\f0  Project Highlights \
- Full end\uc0\u8209 to\u8209 end supervised machine learning pipeline \
- Extensive Exploratory Data Analysis with visual and statistical insights \
- Robust preprocessing: imputation, scaling, encoding, redundancy analysis \
- Evaluation of multiple model variants (basic + regularized) \
- Ensemble methods (Random Forest, Gradient Boosting, XGBoost) among top performers \
- \outl0\strokewidth0 \strokec2 Assessment of cross\uc0\u8209 validation and stacking to determine their usefulness for this task\outl0\strokewidth0 \
- Detailed confusion matrices (3\'d73 and pairwise 2\'d72) \
- Clean, reproducible, and well\uc0\u8209 structured repository\
\
\
## 
\f1 \uc0\u55357 \u56550 
\f0  Dataset\
\
The dataset used in this project is the *Vehicle Silhouettes Dataset*, available on Kaggle:\
\

\f1 \uc0\u55357 \u56599 
\f0  https://www.kaggle.com/datasets/rajansharma780/vehicle\
\
This version includes the full feature names and matches the original dataset used in academic research.\
\
### **Target variable**\
- `class` 
\f3 \uc0\u8594 
\f0  \{car, van, bus\}\
\
### **Feature set**\
All remaining columns are numerical geometric descriptors of the silhouette, including:\
\
- compactness  \
- circularity  \
- distance_circularity  \
- radius_ratio  \
- pr.axis_aspect_ratio  \
- max.length_aspect_ratio  \
- scatter_ratio  \
- elongatedness  \
- pr.axis_rectangularity  \
- max.length_rectangularity  \
- scaled_variance  \
- scaled_radius_of_gyration  \
- skewness_about (x3)  \
- hollows_ratio\
\
## 
\f1 \uc0\u55356 \u57263 
\f0  Business Problem\
\
A chain of car repair shops, requested a model capable of identifying the type of vehicle based on its silhouette.  \
The task is framed as a **multiclass classification problem**, where the objective is to predict whether a silhouette corresponds to a car, van, or bus.\
\
This model could support automated intake systems, vehicle identification pipelines, or pre\uc0\u8209 processing stages in computer vision workflows.\
\
\pard\pardeftab720\partightenfactor0
\cf0 \outl0\strokewidth0 \strokec2 ## \uc0\u55358 \u56813  Project Workflow\
\
All steps are implemented inside a single Jupyter Notebook (vehicle_silhouette_classification.ipynb), organized into clear sections.\
\
1. Data Loading and Initial Inspection\
   - Import libraries\
   - Load dataset\
   - Inspect structure and descriptive statistics\
\
2. Data Cleaning and Preprocessing\
   - Check missing values and duplicates\
   - Compute descriptive statistics per class\
   - Median imputation (fit on training only)\
   - Standard scaling (post-split)\
   - Encode target labels\
\
3. Exploratory Data Analysis (EDA)\
   - Class distribution\
   - Histograms and boxplots\
   - Scatterplots for multivariate relationships\
   - Correlation matrix\
   - Identification of redundant features\
\
4. Feature Redundancy Analysis\
   - Test removal of highly correlated features\
   - Compare performance with/without reduction\
   - Conclude that full feature set performs best\
\
5. Train/Test Split\
   - 80/20 split\
   - Stratification to preserve class balance\
   - Same split used for all models\
\
6. Model Training\
   Models evaluated:\
   - Decision Tree (Basic / Regularized)\
   - Random Forest (Basic / Regularized)\
   - Logistic Regression (Basic / Regularized)\
   - k-Nearest Neighbors (Basic / Regularized)\
   - Support Vector Machine (Basic / Regularized)\
   - Gradient Boosting (Basic / Regularized)\
   - XGBoost (Basic / Regularized)\
\
7. Model Evaluation\
   Metrics:\
   - F1-score (primary metric)\
   - Accuracy\
   - Precision\
   - Recall\
   - ROC AUC\
   - Confusion matrices (3x3 and pairwise 2x2)\
\
8. Cross-Validation Assessment\
   - Evaluate whether cross-validation improves model reliability\
   - Compare CV results with train/test performance\
   - Assess its usefulness for this specific task\
\
9. Stacking Assessment\
   - Test a stacking classifier combining top-performing models\
   - Evaluate whether stacking provides additional robustness\
   - Compare results with individual models\
\
10. Conclusions\
   - Best models identified\
   - Business suitability assessed\
   - Recommendations provided\outl0\strokewidth0 \
\pard\pardeftab720\partightenfactor0
\cf0 \
--- \
\
\pard\pardeftab720\partightenfactor0
\cf0 \outl0\strokewidth0 \strokec2 ## \uc0\u55357 \u56522  Results Summary \
Ensemble methods such as **Random Forest**, **Gradient Boosting**, and **XGBoost** consistently achieved the highest F1\uc0\u8209 scores and ROC AUC values, demonstrating excellent generalization. \
\
Margin\uc0\u8209 based models (**SVM**, **Logistic Regression**) also performed strongly, with stable metrics across folds. \
\
Simpler models like **Decision Tree** and **kNN** showed lower test performance and a higher tendency to overfit. \
\
A **stacking ensemble** combining the strongest individual models was also evaluated. Its performance was comparable to the best single models, confirming the robustness of the overall modeling pipeline. \
\
Across all models, residual misclassifications were concentrated mainly in the **car\'96van boundary**, the most challenging separation in the dataset. \
\
--- \
\
VehicleSilhouetteClassificationProject/\
\uc0\u9500 \u9472 \u9472  README.md\
\uc0\u9500 \u9472 \u9472  requirements.txt\
\uc0\u9500 \u9472 \u9472  .gitignore\
\uc0\u9500 \u9472 \u9472  data/                     # empty, dataset excluded via .gitignore\
\uc0\u9500 \u9472 \u9472  notebooks/\
\uc0\u9474    \u9492 \u9472 \u9472  vehicle_silhouette_classification.ipynb\
\uc0\u9492 \u9472 \u9472  results/\
    \uc0\u9500 \u9472 \u9472  confusion_matrices/\
    \uc0\u9500 \u9472 \u9472  metrics_summary.csv\
    \uc0\u9492 \u9472 \u9472  plots/\
\pard\pardeftab720\partightenfactor0
\cf0 \outl0\strokewidth0 \
\
\
## 
\f1 \uc0\u55357 \u56425 \u8205 \u55357 \u56507 
\f0  About the Author \
\
This project was developed by **Maria Petralia (MaPi)** as part of her Data Science & AI training journey. With a background in Computer Science and professional experience in software and data solutions, she focuses on building clear, rigorous, and well\uc0\u8209 documented machine learning workflows. \
\
If you\'92d like to connect or explore more of her work: \
- GitHub: *https://github.com/MapiAI/MapiAI/tree/main* \
- LinkedIn: *https://www.linkedin.com/in/mariapetralia/* \
\
---\
}