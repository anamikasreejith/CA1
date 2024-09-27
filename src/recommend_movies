import pandas as pd

# Example dataset of movies
movies_data = pd.DataFrame({
    'Movie_ID': [1, 2, 3, 4, 5],
    'Movie_Title': ['Movie A', 'Movie B', 'Movie C', 'Movie D', 'Movie E'],
    'Genres': ['Action|Adventure', 'Drama|Romance', 'Action|Thriller', 'Comedy', 'Adventure|Comedy'],
    'Actors': ['Actor1|Actor2', 'Actor3|Actor4', 'Actor1|Actor5', 'Actor6|Actor7', 'Actor8|Actor2']
})

# Function to recommend movies based on genres and actors
def recommend_movies(user_data, movies_data):
    watched_genres = user_data['Watched_Genres']
    favorite_actors = user_data['Favorite_Actors']
    
    # Filter movies based on genres and actors
    recommendations = movies_data[
        (movies_data['Genres'].str.contains('|'.join(watched_genres))) |
        (movies_data['Actors'].str.contains('|'.join(favorite_actors)))
    ]
    return recommendations

# Example user data
user_data = {
    'User_ID': 1,
    'Watched_Genres': ['Action', 'Adventure'],
    'Favorite_Actors': ['Actor1', 'Actor2'],
    'Ratings': 4.5
}

recommended_movies = recommend_movies(user_data, movies_data)
print(recommended_movies)