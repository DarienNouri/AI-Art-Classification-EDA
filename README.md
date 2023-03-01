# AI-Art-Classification-EDA Project
Exploratory data analysis inspecting methods of classifying Classical, Modern, and AI-Generated art


This repository contains an exploratory data analysis project focused on analyzing art preference ratings based on demographic information and energy ratings. The project aims to build a regression model to predict art preference ratings from energy ratings and examine the impact of demographic factors on art preferences.

## Dataset

The project utilizes two datasets: Art.csv and Ratings.csv. The Art dataset contains information about various artworks, including their title, artist, and type. The Ratings dataset contains information about art ratings, including ratings for factors such as energy, darkness, action, esteem, and preference.

## Analysis

The project analysis is split into four sections:

1. Relationship between Energy Ratings and Preference Ratings
2. Classical vs. Modern Art Preference Ratings
3. Art Preference Ratings by Gender
4. Art Preference Ratings by Art Background

### Relationship between Energy Ratings and Preference Ratings

The project begins with exploring the relationship between energy ratings and preference ratings. It utilizes Ordinary Least Squares (OLS) Regression to examine the relationship between the two variables. The model's performance is evaluated using validation scores such as R2 and Mean Absolute Error (MAE). Cross-validation scores showed consistent MAE, indicating a well-trained model.

### Classical vs. Modern Art Preference Ratings

The project analyzes the difference in preference ratings between classical and modern art. It uses the Mann-Whitney U test to calculate a p-value with an alpha level of .05. The results show that preference ratings for classical art are greater than modern art. Additionally, non-human art preference ratings are lower than classical and modern art. The statistical analysis with the Mann-Whitney U test reinforces the claim of a significant difference in the level and distribution of preference ratings between modern and non-human art.

### Art Preference Ratings by Gender

The project examines the difference in preference ratings between genders. The mean difference between men and women's ratings is minimal. The Mann-Whitney U test yields (P=.44), indicating a lack of difference in preference ratings between men and women.

### Art Preference Ratings by Art Background

The project explores the difference in preference ratings between users with and without art backgrounds. The average preference rating for users with some art background is 4.19, while the average preference rating for users without an art background is 4.31. The difference of 0.12 between average preference ratings of those with some art background and those with none is not significant.

## Code Summary

The code starts with importing necessary libraries such as category_encoders, seaborn, matplotlib, and plotly. It also suppresses the warnings that may arise during the execution of the code.

The code then reads two csv files into two separate data frames art and ratings. It also creates new data frames that filter the art and ratings data frames based on artwork type. It further creates other data frames that filter the ratings data frame based on different rating factors such as energy, darkness, action, and esteem. It also separates the demographic information from the ratings data frame.

The code then computes the mean ratings of the artwork and demographics data frame based on different factors such as gender, educational background, and artwork type. It then performs statistical tests such as the Mann-Whitney U test to compare the mean ratings of the data frames. It also generates a table of test results and mean ratings.

Finally, the code creates a new data frame men_women_means that calculates the mean preference ratings based on gender. It filters out the data related to gender 3 (nonhuman artwork) and counts the number of males and females.

The identified factors in the "dark personality" traits are listed in dark_questions, which includes traits such as manipulation, deceitfulness, callousness, lack of remorse, and narcissism. The model evaluated in
