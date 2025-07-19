# Credit Card Default Risk Prediction

This project presents a complete machine learning pipeline to predict credit card default risk. The analysis compares four classification models—Logistic Regression, Random Forest, XGBoost, and K-Nearest Neighbors (KNN)—using a real-world dataset. The pipeline includes thorough preprocessing, class balancing, feature selection, and performance evaluation with interpretability in mind.

------------------------------------------------------------------------

## Project Overview

Credit default prediction is critical for minimizing financial loss and enabling responsible lending. This study implements and evaluates four supervised learning models using a dataset of over 36,000 applicants. The task is binary classification: predicting whether an individual is at high risk of default.

**Highlights:** - Advanced preprocessing and cleaning. - Class imbalance correction using ADASYN. - Correlation-based feature selection. - 5-fold cross-validation and hyperparameter tuning. - Visualization of correlation, distributions, and model performance. - HTML report generated using Quarto.

------------------------------------------------------------------------

## Dataset

Dataset source: [Kaggle - Credit Car Prediction Dataset](https://www.kaggle.com/datasets/tanayatipre/car-price-prediction-dataset/data?select=train_data.csv)

**Attributes include:** - Demographics: age, education, employment length - Financial info: income, account age, asset ownership - Communication: phone access, internet availability

------------------------------------------------------------------------

## Setup Instructions

### Requirements

Make sure you have the following installed: - [R](https://www.r-project.org/) - [RStudio](https://posit.co/) - [Quarto](https://quarto.org/)

Install R libraries:

``` r
install.packages(c("caret", "xgboost", "randomForest", "class", 
                   "smotefamily", "ROSE", "corrplot", "pROC"))
```

------------------------------------------------------------------------

## Running the Project

1.  Open `credit_card.qmd` in RStudio.
2.  Click **Render** or run the following in the console:

``` r
quarto::quarto_render("credit_card.qmd")
```

3.  The output is an interactive HTML report that includes all plots, model outputs, and interpretations.

------------------------------------------------------------------------

## Models Compared

| Model               | Accuracy (All Features) | Accuracy (Selected Features) |
|---------------------|-------------------------|------------------------------|
| Logistic Regression | 62%                     | 62%                          |
| Random Forest       | 99%                     | 99%                          |
| XGBoost             | 93%                     | 91%                          |
| KNN                 | 98%                     | 97%                          |

Random Forest and KNN outperformed the others. Feature reduction had minimal performance impact, suggesting good variable selection.

------------------------------------------------------------------------

## Visualizations

The report includes: - Correlation heatmaps - Feature distribution plots before/after scaling - Class balance charts before/after ADAS - Model accuracy comparison bar plot

------------------------------------------------------------------------

## Limitations

-   **Small dataset** (\~36,000 samples) may not reflect all borrower behaviors.
-   **Single institutional source** restricts generalizability.
-   **Synthetic oversampling** (ADAS) might introduce unrealistic patterns.
-   **No temporal dynamics**: the data is static, limiting trend analysis.
-   **No cost-sensitive metrics**: false positives/negatives are not weighted differently.
-   **Model interpretability** is limited for ensemble methods like Random Forest and XGBoost.

------------------------------------------------------------------------

## Conclusion

This project demonstrates that tree-based and distance-based models can effectively predict credit default risk, especially with proper preprocessing and resampling. Random Forest and KNN showed excellent performance, while XGBoost offered a solid trade-off between interpretability and accuracy. Logistic Regression was less suited for this non-linear task.

These findings reinforce the importance of preprocessing, careful model selection, and balancing accuracy with explainability in real-world credit scoring systems.

------------------------------------------------------------------------

## Author

**Emad Taghiye**\
Ph.D. Student, University of Oregon\
[etaghiye\@uoregon.edu](mailto:etaghiye@uoregon.edu){.email}
