# Titanic-Dataset-Analysis
 This project involves an exploratory data analysis (EDA) of the famous Titanic dataset provided by Seaborn. The objective is to estimate what kind of passengers were more likely to survive the Titanic disaster and compare it with the actual survivors. The primary modeling technique used in this project is Logistic Regression.
# Introduction
The Titanic dataset is one of the most well-known datasets in data science. It provides data on the passengers aboard the Titanic, including their demographic information and whether they survived the disaster. This project aims to explore this data and perform various analyses to understand the factors influencing survival rates, using Logistic Regression as the main algorithm for prediction.
# Exploratory Data Analysis
## Missing Values
The dataset initially had missing values in the `age`, `deck`, and `embark_town` columns. The `deck` variable was dropped due to excessive missing values, but before its removal, the following analysis was performed:
 ## Deck Analysis
- Visualized the distribution of passengers across different decks.
- Observed that Deck C had the most passengers, and survival rates were higher on Decks B and C, with Decks A and G being the least safe.
- After the analysis, the `deck` column was dropped
 ## Age Imputation
  The age variable had 177 missing values. Instead of dropping this important feature, the missing values were filled based on the median age within each passenger class (pclass):
  ## Age imputation strategy
  - Used a boxplot to analyze the distribution of ages across different passenger classes.
  - Filled missing ages with the median values: 38 for `pclass=1`, 29 for `pclass=2`, and 24 for `pclass=3`.
## Embark_Town Missing Values
Finally, the `embark_town` column had two missing values, which were simply dropped:
## Final Check
After these steps, no missing values remained in the dataset
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
