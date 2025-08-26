## Orange Quality Classification

### Project Overview

This project aims to classify the **quality of oranges** based on various physical and chemical attributes. By analyzing features such as size, weight, sweetness (Brix), pH, softness, and visual characteristics, the goal is to develop a machine learning model that can accurately sort oranges into different quality tiers. This is a practical application for quality control in the agricultural and food industries.

-----

### Technical Highlights

  * **Dataset**: The dataset used is 'Orange Quality Data.csv', which contains information about orange quality.
  * **Size**: 241 entries, 11 columns.
  * **Key Features**:
      * **Physical**: Size (cm), Weight (g), Softness (1-5).
      * **Chemical**: Brix (Sweetness), pH (Acidity).
      * **Visual & Variety**: Color, Variety, Blemishes (Y/N).
  * **Approach**:
      * **Data Cleaning**: The dataset was clean with no missing values or duplicates.
      * **Exploratory Data Analysis**: The code checks basic statistics, unique values, and data types.
      * **Label Encoding**: Applied to categorical columns (Color, Variety, Blemishes (Y/N)). The target variable Quality (1-5) was converted to an integer type.
      * **Feature Engineering**: The numerical target variable Quality (1-5) was binned into a new discrete target y\_discrete using specified thresholds (1.5, 2.5, 3.5, 4.5). This converts the problem into a multi-class classification task.
      * **Data Standardization**: Applied StandardScaler to the features.
      * **Multi-class Classification**: The target variable has 4 discrete classes.
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * **67.3%** with Gradient Boosting and Decision Tree Classifiers.
      * **63.3%** with Logistic Regression and XGBoost Classifier.
      * The moderate accuracies suggest that while the models have some predictive power, the task is challenging, and there is room for improvement.

-----

### Purpose and Applications

  * **Automated Quality Control**: Enables the automatic sorting of oranges based on quality, improving efficiency in processing facilities.
  * **Agricultural Grading**: Assists farmers and distributors in grading their produce, ensuring consistent quality for consumers.
  * **Waste Reduction**: Helps in identifying lower-quality produce early in the supply chain, reducing waste.
  * **Food Science Research**: Provides a platform for analyzing the relationships between an orange's properties and its perceived quality.

-----

### Installation

Clone the repository and download the dataset.

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Investigating the impact of the discretization of the target variable on model performance.
  * Performing comprehensive hyperparameter tuning and cross-validation for all models.
  * Exploring more advanced feature engineering, possibly creating new features from the existing data.
  * Adding a more detailed analysis of the classification report and confusion matrices to understand the model's strengths and weaknesses for each quality class.
