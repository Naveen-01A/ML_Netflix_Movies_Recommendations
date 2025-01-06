### ML_Netflix_Movies_Recommendations

# NEFLIX MOVIES AND TV SHOWS CLUSTERING PROJECT


### Project Summary -

Netflix, the world’s largest online streaming platform, serves over 220 million subscribers as of Q2 2022. To enhance user experience and reduce subscriber churn, it is essential to effectively cluster the shows hosted on the platform. By organizing shows into distinct groups, Netflix can offer more personalized recommendations, helping users discover content aligned with their interests.

The objective of this project is to classify Netflix shows into clusters where shows within the same cluster share similarities, while those in different clusters exhibit significant differences. This clustering will aid in content recommendation, enhancing engagement and improving customer retention.

Dataset Overview:

Rows: 7,787

Columns: 11

The data will serve as the foundation for creating meaningful clusters and analyzing patterns in the available shows.


### Problem Statement

Netflix needs to efficiently cluster its vast collection of 7,787 shows to improve content discovery and personalize recommendations for users. By grouping similar shows together, the goal is to enhance user experience, increase engagement, and reduce subscriber churn.

### Variables Description

Here's a brief description of each column:

1) type – Whether the content is a movie or TV show.

2) title – The name of the movie or TV show.

3) director – The director(s) of the content.

4) cast – List of actors featured in the content.

5) country – Country where the content was produced.

6) date_added – The date the content was added to the platform.It has to change to date type.

7) release_year – The year the content was released.It also has to change to date.

8) rating – Content rating (e.g., PG, R, etc.).

9) duration – Length of the movie or number of seasons for a TV show. It has to convert to integer.

10) listed_in – Categories or genres the content belongs to.

11) description – A short summary of the content.





##  Conclusions:

* In this project, we worked on a text clustering problem wherein we had to classify/group the Netflix shows into certain clusters such that the shows within a cluster are similar to each other and the shows in different clusters are dissimilar to each other.

* The dataset contained about 7787 records, and 12 attributes.
We began by dealing with the dataset's missing values and doing exploratory data analysis (EDA).

* It was found that Netflix hosts more movies than TV shows on its platform, and the total number of shows added on Netflix is growing exponentially. Also, majority of the shows were produced in the United States, and the majority of the shows on Netflix were created for adults and young adults age group.

* It was decided to cluster the data based on the attributes: director, cast, country, genre, and description. The values in these attributes were tokenized, preprocessed, and then vectorized using TFIDF vectorizer.

* Through TFIDF Vectorization, we created a total of 20000 attributes.

* We used Principal Component Analysis (PCA) to handle the curse of dimensionality. 4000 components were able to capture more than 80% of variance, and hence, the number of components were restricted to 4000.

* We first built clusters using the k-means clustering algorithm, and the optimal number of clusters came out to be 8. This was obtained through the elbow method and Silhouette score analysis.

* Then clusters were built using the Agglomerative clustering algorithm, and the optimal number of clusters came out to be 12. This was obtained after visualizing the dendrogram.

* A content based recommender system was built using the similarity matrix obtained after using cosine similarity. This recommender system will make 10 recommendations to the user based on the type of show they watched.
