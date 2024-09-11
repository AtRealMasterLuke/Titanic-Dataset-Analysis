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
## Binary Analysis
The next step in the analysis was to perform a binary analysis on the target variable, `survived`, to determine how different factors might influence the survival of passengers.
 - ### Survival Analysis:
      - A count plot was created to visualize the distribution of the survived variable. It was observed that most of the passengers onboard did not survive. The results confirmed that a significant number of passengers lost their lives during the tragedy.
 - ### Impact of Being Alone:
      - The `alone` variable (a combination of sibsp and parch) was analyzed to see if being alone affected survival chances.
      - The analysis showed that passengers who were alone had a lower chance of survival compared to those who were not alone.
 - ### Effect of Being an Adult Male:
      - The `adult_male` variable was analyzed to see its impact on survival. It was found that the vast majority of adult males did not survive.
 - ### Gender Impact:
      - The analysis of the `sex` variable showed that men had a higher mortality rate, while women were more likely to survive, confirming the notion that "women and children first" was applied during the evacuation.
 - ### Embarkation Port Impact:
      - The impact of the embarkation port (embark_town) on survival was analyzed. The majority of deceased passengers boarded at Southampton, which was also the port with the highest number of boardings.
 - ### Impact of Having a Sibling/Spouse:
      - The analysis of the `sibsp` variable indicated that passengers with siblings or spouses had better survival chances compared to those without.
## Numerical Feature Analysis
 - # Age distribution:
   - Most passengers were between the ages of 25-35, with relatively few older passengers.
 - # Fare Distribution:
   - The majority of tickets were priced between 0-50. Analyzing the mode, mean, and median, it was determined that the fare data is right-skewed.
   - The fare variable has the following distribution:
      - ## Mode: $8.05
      - ## Mean: $32.20
      - ## Median: $14.45
# Feature Engineering and Multicollinearity
 - After examining the dataset, one-hot encoding was applied to categorical variables using `get_dummies`, and correlation analysis was conducted to detect multicollinearity.
 ## Correlation Matrix Heatmap:
  - It was observed that the least important variables in terms of survival were `embark_town_Queenstown`, `sibsp`, `age`, and `parch`.
 ## Multicollinearity Check:
  - Variables with high correlations were detected and dropped, such as `who_man` and `who_woman`, since sex_male already captured this information
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
