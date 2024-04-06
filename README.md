# Airbnb_prediction
Python project to predict Airbnb price

Step 1: Getting the Data

The dataset is loaded from a CSV file, and basic exploratory data analysis (EDA) is performed, including viewing the first few rows, checking for missing values, and summarizing the data.

Step 2: Exploratory Data Analysis (EDA)

Visualizations are created to understand the distribution of the target variable (log_price) and other features like room_type.
Correlations between features are examined using a heatmap.
Missing values in the dataset are highlighted, indicating a need for cleaning.

Step 2.1: Feature Engineering

New features are created, such as amenity_count and dummy variables for room_type.
Geospatial features (lat_bin and long_bin) and categorical encoding of review_scores_rating are introduced.
Missing values in bathrooms are filled with the median value.

Step 3: Handling Outliers

Outliers in the accommodates feature are identified and handled using capping and log transformation methods.
The impact of these methods on data distribution is visualized.

Step 4: Preparing the Data for Machine Learning Algorithms
Features are scaled using StandardScaler.

Data types are converted to reduce memory usage, and one-hot encoding is applied to categorical variables.

Step 5: Splitting the Dataset

The dataset is split into training and testing sets, and categorical columns are encoded numerically.

Step 6 & 7: Model Training and Evaluation

An XGBoost regressor is trained on the processed data.
Initially, a ValueError indicates an issue with non-numeric data types, which is addressed by dropping or transforming certain columns and filling missing values.
The model's performance is evaluated using RMSE and R² metrics. The initial evaluation yields an RMSE of 0.420 and an R² of 0.656.
Feature importance is analyzed to understand the impact of different features on predictions.

Hyperparameter Tuning

GridSearchCV is used to find the best model parameters, resulting in improved model performance.
Cross-validation is performed to assess the model's stability and generalizability.

Model Interpretation

SHAP (SHapley Additive exPlanations) is mentioned for model interpretation, though specific SHAP analysis results are not provided.
