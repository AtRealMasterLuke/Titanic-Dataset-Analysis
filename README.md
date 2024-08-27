# Titanic-Dataset-Analysis
 This project involves an exploratory data analysis (EDA) of the famous Titanic dataset provided by Seaborn. The objective is to estimate what kind of passengers were more likely to survive the Titanic disaster and compare it with the actual survivors. The primary modeling technique used in this project is Logistic Regression.
# Introduction
The Titanic dataset is one of the most well-known datasets in data science. It provides data on the passengers aboard the Titanic, including their demographic information and whether they survived the disaster. This project aims to explore this data and perform various analyses to understand the factors influencing survival rates, using Logistic Regression as the main algorithm for prediction.
# Exploratory Data Analysis
The current EDA includes:
- Missing Values Analysis: We analyzed the missing values in the dataset and found that the `deck` column has too many NaNs, leading to its potential exclusion from the analysis.
- Feature Dropping: Columns that provide similar information, such as `alive`, `class`, and `embarked`, were removed to avoid redundancy.
More analysis is ongoing, including visualizations and statistical summaries, to identify patterns and correlations.
# Modeling with Logistic Regression
Logistic Regression is used as the primary machine learning algorithm to predict the likelihood of passenger survival based on the available features. This choice was made due to its effectiveness in binary classification problems, such as survival prediction.
Future sections will include details on how the model was trained, evaluated, and the insights gained from it.
# Future Work
- Visualization: Create plots to visualize the distribution of passengers based on survival, age, fare, and class.
- Feature Engineering: Handle missing values, particularly in columns like `age` and `embark_town`.
- Modeling: Continue refining the Logistic Regression model and explore other potential algorithms for comparison.
# Contributing
Contributions are welcome! If you have suggestions or want to improve this analysis, feel free to submit a pull request.
# License
This project is licensed under the MIT License.
