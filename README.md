# Recommendations_with_IBM
## Introduction
For this project we analyzed the interactions that users have with articles on the IBM Watson Studio platform, and make recommendations to them about new articles they will like. 

## Libraries Used:
Python 3.7 and above
Pandas
Numpy
Matplotlib
pickle
RE
NLTK
Sklearn
tqdm
Jupyter

## Overview
### I. Exploratory Data Analysis
Before making recommendations of any kind, we will need to explore the data we are working with for the project. 
- What is the distribution of how many articles a user interacts with in the dataset?
- The number of unique articles that have an interaction with a user.
- The number of unique articles in the dataset (whether they have any interactions or not).
- The number of unique users in the dataset. (excluding null values)
- The number of user-article interactions in the dataset.
- The most viewed article_id

### II. Rank Based Recommendations
We don't actually have ratings for whether a user liked an article or not. We only know that a user has interacted with an article. In these cases, the popularity of an article can really only be based on how often an article was interacted with.
- Functions to return the top articles with most interactions
- Function to return the top articles IDs

### III. User-User Based Collaborative Filtering
In order to build better recommendations for the users of IBM's platform, we looked at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. This would be a step in the right direction towards more personal recommendations for the users.
- Re-formatted df to show unique users and articles
- If a user has interacted with an article at least once, the respective user-item pair is marked as 1 or marked as 0 if otherwise.
- Function to find similar users based on similarity of their interactions
- Function to return article names based on their IDs
- Function to return all articles the user interacted
- User-user collaborative Filtering function and it's improved version
- Function that sorts articles by popularity
- Function that sorts users by the number of their activity

### IV. Content Based Recommendations
Given the amount of content available for each article, there are a number of different ways in which a content based recommendation system can be implemented.
- Tokenize function to tokenize the title of each article
- Created df_to_analyze to combine all the articles available on the platform, whether or not any user interacted with the article
- Find similar articles function uses the output vector of tfidf class to determine which articles are the most similar to the article in question

V. Matrix Factorization
Finally, we will complete a machine learning approach to building recommendations. Using the user-item interactions, we will build out a matrix decomposition. Using the decomposition, we will get an idea of how well we can predict new articles an individual might interact with. We will finally discuss which methods we might use moving forward, and how we might test how well our recommendations are working for engaging users.
