# Project Overview: Predicting TV Show Popularity Using Machine Learning
# Research Question:
How could genres, languages, and other factors predict the popularity of TV shows?
The goal of this project was to predict TV show popularity using various features such as genres, languages, vote counts, and other relevant characteristics. By analyzing the TMDB TV Shows Dataset, which contains data for over 150,000 TV shows, the project aimed to explore the relationships between these factors and a show's popularity. The objective was to develop a system that could predict trends in TV show popularity, providing valuable insights for content creators, distributors, and streaming platforms.

# Dataset Overview:
The TMDB TV Shows Dataset 2024 is a comprehensive collection of TV show data sourced from The Movie Database (TMDB). This widely-used database contains details about TV shows, including ratings, genres, languages, release dates, and more. The dataset features data on over 150,000 TV shows, which was preprocessed and cleaned for analysis.

# Project Goals:
The primary goal was to predict the popularity of TV shows based on various features such as genres, languages, vote counts, and other characteristics. The project sought to explore the relationships between these factors and the popularity of TV shows. Success was determined by the model’s ability to predict popularity accurately, helping inform content strategy decisions for producers and distributors. Key factors influencing the model's performance included the number of seasons, vote count, genre, language, networks, and release dates.

# Data Preparation:
1.	Filtering Data: The dataset was cleaned and preprocessed by filtering the data to include only the years from January 1, 2017, to December 31, 2024, reducing the number of rows to 59,500.
2.	Uniting Tables: Data was combined and cleaned to remove unnecessary or redundant features.
3.	Cleaning Text: Irrelevant columns like 'tagline', 'created_by', etc., were dropped, while textual columns such as 'overview' were extracted and cleaned for feature engineering.
4.	Reducing Large Categories: Features such as languages, networks, and genres were converted into dummy variables.

# Exploratory Data Analysis (EDA):
EDA was performed to visually explore relationships between continuous features and categorical variables in comparison to the target variable, popularity. Various visualizations were used to identify trends and patterns in features such as genres, languages, and networks. This stage helped uncover potential relationships between features that could influence TV show popularity.

# Data Cleansing – Outliers and Missing Values:
1.	Outliers: Outliers in numerical columns, such as vote_count, number_of_seasons, and languages_count, were identified and handled appropriately. Outliers that were initially imputed as zeros were replaced using MICE (Multiple Imputation by Chained Equations).
2.	Missing Values: For missing data in categorical features, Random Forest imputation was applied after earlier attempts using KNN and MICE proved less effective.

# Feature Engineering:
To enhance model performance, new features were created:
•	Year extraction: Extracted year information from the first_air_date and last_air_date.
•	Duration calculation: Calculated the duration between these air dates.
•	Number of Seasons: Determined the number of seasons from the air dates.
•	Text Analysis: A word cloud was generated to identify the most frequent words in the name and overview features. Sentiment analysis was also performed on the overview column.

# Model Selection and Fine-Tuning:
•	Various regression models were tested, including Lasso, Random Forest Regressor, XGBoost, and Ridge. Hyperparameter optimization was performed on these models to find the best-performing one for predicting TV show popularity. The best model was selected based on performance metrics like MSE, RMSE, MAE, and RMSLE.

# Model Evaluation :
•	Various regression models, including Linear Regression, Decision Tree, Random Forest, AdaBoost, Gradient Boosting, SVM, and XGBoost, were trained to predict TV show popularity. Random Forest outperformed all other models, showing the lowest MSE, RMSE, and MAE. SVM had higher errors, and AdaBoost performed the worst.
•	Hyperparameter tuning with RandomizedSearchCV improved the Random Forest model by 6.65%. Key tuned parameters included n_estimators, max_features, and max_depth.


