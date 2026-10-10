# Disease Prediction from Medical Data

Machine learning internship project (CodeAlpha, Task 4). The goal is to predict the possibility of disease from patient data using classification techniques.

## Datasets
- Heart Disease (UCI) - `heart.csv`
- Diabetes (Pima Indians) - `diabetes.csv`
- Breast Cancer (Wisconsin, UCI) - loaded directly from scikit-learn

## Approach
1. Loaded and cleaned each dataset (removed duplicate rows in the heart dataset; replaced invalid zero values in the diabetes data with the column median).
2. Split the data 80/20 into training and test sets and scaled the features.
3. Trained four classifiers: Logistic Regression, SVM, Random Forest, XGBoost.
4. Compared accuracy and checked precision, recall and the confusion matrix for the best model.

## Results (test accuracy)
| Model | Heart Disease | Diabetes | Breast Cancer |
|---|---|---|---|
| Logistic Regression | 0.8361 | 0.7078 | 0.9825 |
| SVM | 0.7705 | 0.7403 | 0.9825 |
| Random Forest | 0.7705 | 0.7792 | 0.9561 |
| XGBoost | 0.7049 | 0.7727 | 0.9561 |

## Findings
- No single algorithm was best on every dataset.
- The original heart dataset contained 723 duplicate rows that caused data leakage (100% accuracy); removing them gave realistic results.
- On diabetes, recall for diabetic patients was about 0.61, so some cases were missed. Class weighting or more features could improve this.

## How to run
## How to run
1. Open [Disease_Prediction.ipynb](Disease_Prediction.ipynb) in Google Colab, or click here: [Open in Colab](https://colab.research.google.com/github/rishagaur/Disease_Prediction_ml/blob/main/DiseasePrediction.ipynb)
2. Upload the datasets [HeartDiseaseTrain-Test.csv](HeartDiseaseTrain-Test.csv) and [diabetes.csv](diabetes.csv) into the Colab files area (the `content` folder).
3. Click Runtime > Run all.
## Tools
Python, pandas, scikit-learn, XGBoost, Google Colab

*Educational project only. Not intended for real medical decisions.*
