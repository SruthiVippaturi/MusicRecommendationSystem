## Objective 
To recommend the top 10 songs to users based on their listening history using collaborative filtering techniques.
The aim is to build a personalized music recommendation engine that improves user engagement and experience on streaming platforms.

## Data Sources
The data used in this project is retrieved from: http://millionsongdataset.com/ 
The dataset includes:

song_data.csv – contains song ID, title, artist name, and release year.

count_data.csv – contains user ID, song ID, and the play count.

## Key Findings
There are over 3,000 users, 900+ songs, and 2 million+ interactions in the dataset.

Some songs are extremely popular and heavily replayed by many users.

Songs released in recent years (2005–2010) dominate the dataset.

## Methods Used
### Popularity-Based Ranking
Recommended top songs based on global average play count—works for cold-start scenarios but lacks personalization.

### User-User Collaborative Filtering
Recommended songs based on similar users' preferences. Gave high F1 scores and personalized suggestions.

### Item-Item Collaborative Filtering
Used item-to-item similarity to recommend songs similar to those already listened to by the user.

### Matrix Factorization (SVD)
Modeled latent features to make personalized recommendations using Surprise library’s SVD algorithm.

### Hyperparameter Tuning using GridSearchCV
Tuned parameters like similarity metric and number of neighbors to improve RMSE and F1 score.

## How to Run this File 
### Clone the repository
```
git clone https://github.com/SruthiVippaturi/MusicRecommendationSystem.git
```
### Install dependencies
```
pip install -r requirements.txt
```
(Ensure to create a requirements.txt file with the necessary libraries listed.)

## Further Development 
Model Deployment: Deploy the final recommendation system using Flask or FastAPI to provide real-time song suggestions.

User Interface: Build an interactive front-end using Streamlit or Dash for users to enter their user ID and receive top recommendations.
