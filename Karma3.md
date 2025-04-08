# IMDb Movies Dataset Analysis

This project involves exploratory data analysis (EDA), feature engineering, and visualization using a dataset of IMDb movies. The goal was to better understand what makes a movie successful based on various features like rating, votes, runtime, and more.

---

## Table of Contents

- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Objectives](#objectives)
- [Steps Followed](#steps-followed)
  - [1. Data Cleaning](#1-data-cleaning)
  - [2. Data Exploration](#2-data-exploration)
  - [3. Feature Engineering](#3-feature-engineering)
  - [4. Data Visualization](#4-data-visualization)
- [Insights Gained](#insights-gained)
- [Future Scope](#future-scope)

---

## Dataset

- *Source:* Local CSV file named IMDB.csv
- *Columns:* Title, Genre, Rating, Votes, Runtime, Metascore, Likes, etc.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Objectives

- Load and clean the IMDb dataset
- Explore the data to identify patterns in votes, ratings, and genres
- Engineer new features to enrich the dataset
- Visualize findings using scatter plots and bar charts

---

## Steps Followed

### 1. Data Cleaning
- Removed rows with missing (NaN) values using df.dropna()
- Checked data types and null counts using df.info()

### 2. Data Exploration
- Top 10 most viewed videos
- Most frequent channel (most uploads)
- Most loved videos using Likes to Views ratio
- Highest-rated genres
- Relationship between rating and:
  - Votes
  - Runtime

### 3. Feature Engineering
Added new columns:
- Rating ratio = Rating / Votes * 100
- Title Length = Number of characters in the title
- Critic vs User = Root of squared difference between rating and metascore  
  (((Rating - Metascore/10)^2)^0.5)
- Went Viral = Marked a movie as "Yes" if votes > 20000, else "Moderate"

### 4. Data Visualization
- Scatter plot: Rating vs Votes
- Scatter plot: Rating vs Runtime
- Bar chart: Highest-rated genres
- Genre-wise average ratings

---

## Insights Gained

- Certain genres consistently get higher ratings.
- There's some correlation between runtime and rating.
- Most voted movies are not always the highest rated.
- Feature engineering helped identify outliers and unique patterns.

---

## Future Scope

- Train a Machine Learning model to predict IMDb rating based on engineered features.
- Classify whether a movie will go viral or not.
- Try classification and regression models like Random Forest or Linear Regression.

---

## Author

Just a guy learning Data Science one project at a time.
