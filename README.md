# ML_FinalProject_MovieRecommender

## Introduction

In a world that has become dominated by social media, targeted suggestions and/or targeted advertisement  has proven to be effective means of outreaching. Instead of presenting consumers with random advertisements, companies can place targeted advertisements based on one's recent behavior. Many have encountered situations where a simple Google search results in weeks of advertisement about the searched product or products in the same category. Targeted suggestions extend beyond advertisement. For example, shopping sites, such as Amazon, use consumer behavior metrics to suggest items that are frequently purchased together. Another great example is Netflix. The application has the ability to suggest Movie/Show are based on viewing history. Targeted suggestions are a result of a predictive algorithm known as recommender systems,a machine learning application. This project explores a simple movie recommender system.

## Objective
This project explores a simple movie cluster recommender system. The system is to recommend similarly rated movies based on an input of a movie title enjoyed by the user.

## Dataset

The dataset was obtained from MovieLens, a movie recommendation service. The dataset is composed of 27,753,444 ratings across 58,098 movies with 1,108,997 tag applications from 283,228 users. The data was collected between January 9, 1995 and September 26, 2018.

## Inputs

The features of this dataset include:
1. userId
2. movieId
3. rating
4. Timestamp
5. movieId
6. title
7. genres

## Data Preparation

Checked for Null values
Null values were not found in any rows or columns


## Merged data sets
Combined the movies and rating data frames using the movie id as the key


## Dataset description
Checked column data types 
Used the describe function to check data frame statistics


## Feature engineering
Created a dataframe for each movie and the number of ratings in order to calculate the correlation 

## Modelling


Used seaborn plot to validate if the average rating is higher if the number of ratings is higher. From the seaborn plot below, a positive correlation can be observed between the two.


A movie rating matrix was created logging users against the movie titles using the pandas pivot table functions.


Searched for movie of interest. In our case, we chose Pulp Fiction. 

Using the Corrwith() function, we looked for a correlation between Pulp Fiction ratings and the rating of the other movies in the dataset


From the results, it was hard to derive whether movies with a high correlation rate (1.0) to Pulp Fiction were necessarily as good as there were no other variables involved. Created a data frame to look at the correlation rate and number of ratings for each movie. It was found that movies with high correlation rate (1.0) also may have a low number of ratings. 


Created a dataframe to look at movies that were correlated to Pulp Fiction but also had more than 300 ratings. It was found that there were more popular movies returned in the result.

## Conclusion

In conclusion, this movie recommender system is very simple. There are additional features that could be leveraged for a more complex recommendation such as gender, demographic and age. Other approaches that could be used to solve for this are content-based filtering and collaborative filtering. 

## References

[1] Creating a Simple Recommender System in Python Using Pandas
Usman Malik - https://stackabuse.com/creating-a-simple-recommender-system-in-python-using-pandas/

[2] Python: Pandas Dataframe.corrwith()
Shubham- Ranjan - https://www.geeksforgeeks.org/python-pandas-dataframe-corrwith/




