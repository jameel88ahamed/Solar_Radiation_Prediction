# Solar_Radiation_Prediction

## Introduction
Solar energy has become one of the most essential renewable energy sources in the world today. Being abundant and environmentally friendly, it plays a crucial role in meeting global energy demands. According to the International Energy Agency (IEA), solar energy could account for up to 27% of global electricity needs by 2050.

Accurate prediction of solar radiation is vital for optimizing solar energy systems. It enhances energy output forecasting, reduces operational costs, and improves decision-making processes related to energy storage and grid integration. Solar energy is widely utilized across various sectors, including agriculture (solar-powered irrigation), smart cities (solar street lighting), and commercial industries (solar rooftops).

As the demand for sustainable and clean energy grows, the ability to predict solar radiation accurately becomes increasingly important. Such predictions assist in estimating the energy output of solar panels, improving grid stability, and ensuring more efficient energy management.

## Problem Statement
This project aims to address the challenge of accurately predicting solar radiation using machine learning techniques and historical data, which includes features such as temperature, humidity, wind speed, and pressure—factors that can fluctuate significantly over time and across different locations. By building predictive models based on these environmental variables, we seek to improve energy output forecasting for solar panels, which will enhance energy management, grid stability, and reduce costs for solar energy systems.

## Required Libraries
- Pandas : To Clean and maipulate the data.
- Matplotlib: A plotting library for creating visualizations.
- Seaborn: A data visualization library built on top of Matplotlib.
- Pickle: Library used for saving the model and use whenever required.
- Scikit-learn: A machine learning library that provides various regression and classification algorithms & Evaluation Metrices

## Workflow:
1. Data Collection & Pre-processing:
   - Collected the data from Kaggle, specifically for the last four months for which it was available.
   - Conducted data exploration using the **Pandas** library by examining the dataset's head, shape, statistical summary, feature data types, duplicate values, and unique value counts.
   - Applied preprocessing techniques such as removing null values, imputing missing data, removing duplicates and outliers, and handling outliers using the quantile method with the **cmap** function.
2. Feature Engineering:
   - Corrected the data types of the date column to the appropriate datetime format (%dd-%mm-%yyyy).
   - Created additional features such as date, month, year, hour, minute, and second to assist in predicting the target based on time series data.
3. Exploratory Data Analysis (EDA):
   - Created various plots such as scatter plots, pair plots, and histograms to visualize the distribution of data points within the dataset.
   - Plotted box plots to check quantile ranges and visualize outliers.
   - Conducted bivariate analysis to visualize the relationships between different features.
   - Plotted a correlation matrix to identify relationships between the target column and other features, drawing insights from these visualizations.
4. Model Building, Fine-tuning & Evaluation:
   - Used the **sklearn** library for model building, tuning, dataset splitting, and evaluation.
   - Splitting the dataset into target and features using the **train_test_split** function from the sklearn library.
   - Applied feature scaling using normalization techniques **(MinMaxScaler from sklearn.preprocessing)** for better results.
   - Loaded various algorithms including Linear Regression, SGD Regressor, KNeighbors Regressor, Decision Tree, and ensemble techniques like Random Forest, Gradient Boosting, and XGBoost.
   - Built a pipeline using a for loop for training models and displaying evaluation results such as MSE, MAE, RMSE, MAPE, and R² Score.
   - After evaluating all algorithms, selected the top three: Decision Tree, Random Forest, and XGBoost.
   - Performed hyperparameter tuning using **GridSearchCV** from the **sklearn.model_selection** library after handling outliers and applying feature scaling.
   - Performed **regression analysis** on predicted vs. actual values and identified the best-performing model and algorithm for the problem.
  
## Conclusion and Result
  - After comprehensive analysis and fine-tuning, the Random Forest algorithm provided the best results, making it the most suitable algorithm to solve this type of problem.
  - Insights from the visualizations can be leveraged to inform decision-making and improvements in solar energy installations.
