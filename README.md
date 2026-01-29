# Movie-Recommendation-System
Just a hit and trial small project on pre-stored data which is taken from Kaggle.

#  Movie Recommendation System

A machine learning-based web application that recommends movies based on user interest. This project uses **Content-Based Filtering** to suggest the most similar movies to a given title.

# Features

# Search Functionality: Find your favorite movie from a vast dataset.
# Top 5 Recommendations: Get five personalized movie suggestions based on similarity.
# Poster Fetching: (Optional/If implemented) Displays movie posters using the TMDB API.
# Interactive UI: Built with Streamlit for a smooth user experience.

# Tech Stack

* Language: Python
* Libraries: Pandas, Scikit-learn, Streamlit, Pickle, Requests
* Algorithm: Cosine Similarity
* Dataset: [TMDB 5000 Movie Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata)

# Project Structure

text
├── dataset/             # Raw and processed data
├── app.py               # Main Streamlit application
├── model.ipynb          # Jupyter notebook for data analysis & model building
├── movie_dict.pkl       # Saved movie data
├── similarity.pkl       # Precomputed similarity matrix
└── requirements.txt     # Python dependencies


# How it Works

1. Data Preprocessing: We clean the TMDB dataset, merging keywords, cast, crew, and genres into a single "tags" column.
2. Vectorization: Text data is converted into vectors using `CountVectorizer` (Bag of Words).
3. Similarity: We calculate the **Cosine Similarity** between these vectors. The closer the angle, the more similar the movies.
4. Recommendation: When a user selects a movie, the system sorts the similarity scores and returns the top 5 most similar titles.

