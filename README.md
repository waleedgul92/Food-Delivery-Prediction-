# Food-Delivery-Prediction-
This project focuses on predicting food delivery times using a boosting method.

## Project Structure:

The project is structured into several key sections:

  * **Import and Rename Data:** This section handles loading the dataset and performing any necessary column renaming for clarity and consistency.
  * **EDA (Exploratory Data Analysis):** This is a crucial phase where the dataset is explored through various visualizations:
      * **Histograms/KDE Plots:** To understand the distribution of numerical features.
      * **Scatter Plots:** To visualize relationships between numerical predictor variables and the target variable (Delivery Time).
      * **Count Plots:** To display the frequency distribution of categorical features.
      * **Box Plots:** To show the distribution of delivery times across different categories, helping to identify potential outliers and central tendencies.
      * **Line Plots:** To observe trends of average delivery time against continuous variables like distance and courier experience.
      * **Swarm Plots:** To visualize the spread of individual data points for delivery times across categorical variables, especially useful for smaller datasets or to complement box plots by showing data density.
  * **Handle Missing Data:** This section addresses missing values in the dataset using imputation techniques.
  * **Outlier Removal:** Outliers are identified and removed from the dataset to improve model performance. Several methods are explored and their impact on the dataset size is reported.
  * **Feature Scaling:** Numerical features are scaled to a common range using `MinMaxScaler` to prevent features with larger values from dominating the learning process.
  * **Feature Encoding:** Categorical features are converted into a numerical format using one-hot encoding (`pd.get_dummies`) to make them suitable for machine learning algorithms.
  * **Model Training:**
      * **Decision Tree Regressor:** A basic tree-based model is trained, and its performance is evaluated using MAE, MSE, and R-squared.
      * **Random Forest Regressor:** An ensemble learning method that builds multiple decision trees is trained, and its performance is evaluated.
      * **Gradient Boosting Regressor:** Another powerful boosting algorithm is implemented, and its performance is assessed.
      * **XGBoost Regressor:** A highly optimized gradient boosting library is used to train a model, and its performance is evaluated.
  * **Hyper-parameter Tuning:** `Optuna` is utilized for hyperparameter optimization of the `GradientBoostingRegressor` model to find the best set of parameters for improved performance. The best hyperparameters and corresponding MSE are reported.

## Setup and Usage:

1.  **Dependencies:** Ensure you have the necessary Python libraries installed. You can install them using pip:
    ```bash
    pip install numpy pandas seaborn matplotlib scikit-learn xgboost optuna
    ```
2.  **Data:** The project uses the `Food_Delivery_Times.csv` dataset. Make sure this file is present in the specified input directory or update the `pd.read_csv` path accordingly.
3.  **Run the Notebook:** Execute the `food-delivery-time-prediction-using-boosting-mehod.ipynb` notebook cell by cell.

## Analysis and Results:

The notebook systematically preprocesses the data and trains various regression models. The performance metrics (MAE, MSE, R-squared) for each model are printed, allowing for a comparison of their effectiveness in predicting food delivery times. The hyperparameter tuning section further refines the Gradient Boosting model for optimal performance.

This README provides a comprehensive overview of the project, its components, and instructions for replication.
