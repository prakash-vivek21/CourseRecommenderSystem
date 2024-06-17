# Course Recommendation System
This repository contains a course recommendation system that leverages user preferences and course attributes to provide personalized course recommendations. The system utilizes various machine learning techniques including collaborative filtering, content-based filtering, and hybrid approaches.

## Project Overview
The goal of this project is to build a recommendation system that suggests relevant courses to users based on their interests and past interactions with courses. The system is trained using a dataset of user-course interactions and user profiles detailing course interests.

## Datasets
* course_df
  - COURSE_ID: Unique identifier for each course.
  - TITLE: Name of the course.
  - Database to Blockchain: Columns representing different course categories or topics, with binary or integer values indicating relevance or presence in the course.
* ratings_df
  - user: User identifier who rated the courses.
  - item: Course identifier (corresponding to COURSE_ID in course_df).
  - rating: Rating given by the user to the course.
*user_profile_df
- user: Unique identifier for each user.
- Database to Blockchain: Binary indicators or levels of interest indicating user preferences across various course topics.

## Methodology
* Data Preprocessing
  - Handling Missing Values: Missing values in the datasets were handled appropriately to ensure data integrity.
  - Normalization/Standardization: Applied to scale features to a consistent range.

* Dimensionality Reduction
  - PCA (Principal Component Analysis): Used to reduce the dimensionality of the dataset while preserving 90% of the variance. The optimal number of components was found to be 9.
  - NMF (Non-Negative Matrix Factorization): Applied to extract meaningful patterns from the data, particularly useful in collaborative filtering.


* K-means Clustering: Applied to segment courses into 15 clusters, helping to identify similar courses and user groups.

* Model Training and Evaluation
  - Collaborative Filtering: Used user-item interaction data to predict user ratings for courses.
  - Content-Based Filtering: Utilized course attributes and user profiles to recommend courses matching user interests.

* Models and Results
  - Logistic Regression
  - Decision Tree
  - Linear SVC
  - Linear Regression
  - Ridge Regression
  - Lasso Regression
  - ElasticNet Regression
  - RecommenderNet (Keras)

* Evaluation Metrics
Models were evaluated using:
- Accuracy: For classification models.
- RMSE (Root Mean Squared Error): For regression models, measuring prediction error.

* Python Libraries:
  - numpy
  - pandas
  - scikit-learn
  - keras
  - matplotlib
