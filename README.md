PROCEDURE:
Prepare Your Data: Ensure your dataset includes the necessary columns for movie IDs, titles, and genres. 
The dataset should be in CSV format and should include columns representing different genres as binary indicators (e.g., Action, Comedy, Drama, etc.).

Determine the Optimal Number of Clusters: Use the Elbow Method to determine the optimal number of clusters. 
This involves plotting the sum of squared errors (SSE) for a range of cluster values and identifying the "elbow point" where the SSE starts to decrease more slowly.

Cluster the Movies and Make Recommendations: Once the optimal number of clusters is determined, apply K-means clustering to assign each movie to a cluster. 
For a given movie, the system can then recommend other movies from the same cluster.

FUNCTION DESCRIPTION:
recommend_movies
Purpose: Recommends movies similar to a given movie based on cluster assignments.
Parameters:
movie_id (int): The ID of the movie for which recommendations are needed.
df (DataFrame): The DataFrame containing movie data, including cluster assignments.
num_recommendations (int, optional): The number of movie recommendations to return. Defaults to 5.
Returns: A list of movie titles recommended based on their similarity to the given movie.

ELBOW METHOD:
Purpose: Determines the optimal number of clusters for K-means clustering.
Procedure: Iteratively applies K-means clustering with different numbers of clusters, calculates the sum of squared errors (SSE) for each number of clusters, and plots these SSE values to identify the elbow point.
