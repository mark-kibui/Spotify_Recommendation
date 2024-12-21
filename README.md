# Spotify Recommendation System using K-means
![Logo](Assets/Spotify_Logo.png)
## Project Overview
This project aims to build a recommendation system for Spotify users using the K-means clustering algorithm. The system suggests songs to users based on the audio features of songs, grouping them into clusters. By leveraging these clusters, the system can recommend songs that are similar to the ones the user is currently listening to.

### Key Features
- **K-means Clustering**: The main technique used to group similar songs together based on their audio features.
- **Personalized Recommendations**: Recommending songs from the same cluster as the user's favorite tracks.
- **Feature Engineering**: Using audio features such as tempo, energy, danceability, and loudness for clustering.

## Dataset
The dataset used in this project is the **Spotify Million Playlist Dataset**, which contains a variety of songs along with their audio features. Each song has multiple attributes, including:
- **Track Name**
- **Artist Name**
- **Genres**
- **Audio Features**: Danceability, energy, key, loudness, speechiness, acousticness, instrumentalness, liveness, valence, tempo, and others.

## Problem Statement
Music recommendation systems aim to suggest songs that users are likely to enjoy based on their listening history or preferences. By using K-means clustering, we group songs with similar audio characteristics into clusters. This allows us to recommend songs from the same cluster as a user's current favorite, creating a personalized music discovery experience.

## Methodology
1. **Data Preprocessing**:
   - The dataset was cleaned and preprocessed by encoding categorical features and scaling numerical features.
   - One-hot encoding was applied to the 'genre' column to create new features for each genre.
   - Numerical features (such as tempo, danceability, and loudness) were scaled to a uniform range to ensure they contribute equally to the clustering process.

2. **K-means Clustering**:
   - The K-means algorithm was applied to cluster songs based on their audio features.
   - The number of clusters was chosen through experimentation, balancing cluster cohesion and separation to ensure high-quality recommendations.

3. **Recommendation Generation**:
   - For each song, we determined its cluster label.
   - The system then recommended songs from the same cluster as the input song, providing a list of similar songs for the user to explore.

4. **Evaluation**:
   - The effectiveness of the clustering was evaluated using metrics such as the Silhouette Score, which measures how similar songs are within their cluster compared to other clusters.
   - While this is a simple approach, it provides a basis for more advanced recommendation techniques such as collaborative filtering or deep learning.

## Results
- **Cluster Cohesion**: The songs within each cluster were highly similar, based on their audio features.
- **User Experience**: Users were presented with songs that matched the general characteristics of the tracks they enjoyed, enhancing the discovery of new music within their preferred styles.
  
## Conclusion
This project demonstrated how K-means clustering can be used to group similar songs and recommend them to users based on their preferences. While K-means is a basic clustering algorithm, it offers a straightforward approach for music recommendations. For future improvements, more sophisticated techniques such as collaborative filtering, matrix factorization, or deep learning could be implemented to further personalize recommendations.
