# Articles-Recommendation-Engine

## Questions to be Answered
With this model the following question will be answered:
Which articles should be highlighted for each user on the IBM platform?

Aim:
A purposeful recommendation with articles the person will probably be most interested in. 

## Files of this Repository
* Recommendations_with_IBM.ipnyb : A Jupyter Notebook with the recommendation engine
* README.md

## Libraries
The following libraries are used:
* numpy
* pandas
* matplotlib
* project_tests
* pickle

## The Underlying Data
The data available on the IBM Watson Studio platform. It contains articles, users and interactions. Since there are no ratings for any of the articles, we assume the articles with the most interactions are the most popular. These are then the articles we might recommend to new users.

## The model

* User-User Based Collaborative Filtering: In order to build better recommendations for the users of IBM's platform, we look at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. 
* Matrix Factorization: Finally, we complete a machine learning approach to building recommendations. Using the user-item interactions, we build out a matrix decomposition.

## Results
There is a so called cold start problem. New users haven't yet interacted with articles. Therefore we cannot search for a "neighbor", which means collaborative filtering cannot be used. A solution could be ranked-based or content-based recommenders. Here we used ranked-based recommendations.

Eventhough the accuracy increases with the number of latent features when we look at the whole data set, it's the other way around, when we look at the test data set. The reason is overfitting. To determine if these recommendations are an improvement to how users currently find articles we could apply an A/B Testing.



