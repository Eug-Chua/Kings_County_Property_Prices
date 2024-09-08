# Housing Prices Prediction Using Linear Regression

## Project Overview
This project aims to predict house prices using linear regression and advanced machine learning techniques like XGBoost. Accurate house price prediction is crucial for stakeholders like real estate developers, homeowners, and investors. By modeling key features like the number of rooms, living space, and quality of construction, this project provides a transparent and interpretable solution for estimating housing prices in a data-driven manner.

## Key Features
    - Data Preprocessing: Efficient handling of missing data, outliers, and data normalization techniques ensures model robustness.
    - Feature Engineering: Creation of interaction terms, polynomial features, and exploration of the most influential predictors to improve model accuracy.
    - Modeling Techniques: Linear regression was initially used for simplicity and interpretability, while more sophisticated models like XGBoost were applied to handle non-linearity and improve prediction accuracy.
    - Model Evaluation: Metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared are used to assess model performance and generalizability.

## Technologies Used
- Programming Language: Python
- Libraries:
    - Pandas and NumPy for data manipulation.
    - Matplotlib and Seaborn for data visualization.
    - Scikit-learn for regression modeling.
    - XGBoost for boosted decision tree modeling.

## Project Workflow
1. Data Loading and Exploration:
    - Load the housing dataset and explore its structure to gain initial insights on distributions and missing values.

2. Data Preprocessing:
    - Imputed missing values using mean-based strategies for numerical data and mode-based strategies for categorical data.
    - Addressed outliers by applying logarithmic transformation to skewed variables.
    - Normalized features like sqft_living to improve linear model performance.

3. Feature Selection and Engineering:
    - Conducted feature importance analysis using XGBoost to identify key variables.
    - Created interaction terms between variables such as `sqft_living` and grade to capture non-linear relationships.

4. Model Development:
    - Implemented and fine-tuned both linear regression and XGBoost models.
    - Used GridSearchCV for hyperparameter tuning in the XGBoost model to optimize learning rate, depth, and other key parameters.
5. Model Evaluation:
    - The models were evaluated using cross-validation and metrics like MAE, MSE, and R-squared to assess predictive accuracy and model generalizability.
    - A comparison was made between linear regression and XGBoost, showing a clear improvement in prediction performance with the latter.

## Results
- The XGBoost Regressor, after tuning, achieved an R² score of 70.24%, an improvement over the untuned score of 69.46%.
- The Mean Absolute Error (MAE) and Mean Squared Error (MSE) also demonstrated improvements, showing that the model generalizes well to unseen data:
    - Mean Absolute Error (MAE): 44,996,311,824
    - Mean Squared Error (MSE): 212,123
    - R-squared: 70.24%

Key insights from the feature importance analysis include:
- `grade` (quality of construction) was the most significant predictor, reflecting how high-quality homes command higher prices.
- `sqft_living` was another crucial feature, showing that larger homes have higher market values.
- `waterfront`, indicating proximity to water, significantly impacted price, highlighting the premium paid for waterfront properties.