# Movie-Recommendation-System-
This is a project designed to provide movie recommendations based on user input. It utilizes techniques such as text similarity and cosine similarity to find similar movies and suggest them to the user. The system takes into account various features of movies, including genres, keywords, taglines, cast, and director, to determine similarity.

#1 The project requires the following dependencies:

difflib: Used to find the closest match for a given movie name entered by the user.
sklearn.feature_extraction.text.TfidfVectorizer: Converts the textual data into numerical feature vectors.
sklearn.metrics.pairwise.cosine_similarity: Calculates the similarity score between feature vectors.
numpy: Required for numerical operations.
pandas: Used for data manipulation and analysis.

#2 Data
The project uses a movie dataset stored in a CSV file ('movies.csv'). The dataset contains information about various movies, including their titles, genres, keywords, taglines, cast, director, and more. The dataset is loaded into a pandas DataFrame for further processing.


#3 Feature Selection
To determine similarity between movies, specific features are selected for consideration. The selected features are:
Genres
Keywords
Tagline
Cast
Director
These features are chosen as they provide valuable information for identifying similar movies.


#4 Data Preprocessing
Before applying similarity algorithms, the missing values in the selected features are filled with empty strings to ensure compatibility. The selected features are then combined into a single column in the DataFrame, creating a textual representation of the movie details.

# 4.1 Feature Vectorization
To perform similarity calculations, the textual data is converted into numerical feature vectors using the TfidfVectorizer from the scikit-learn library. The TfidfVectorizer converts each entity in the vector (movie details) to a numerical representation.


# 5 Similarity Calculation
Cosine similarity is applied to calculate the similarity scores between the feature vectors. Cosine similarity measures the cosine of the angle between two vectors, providing a similarity score between 0 and 1.


# 6 Finding Closest Match
To handle potential misspellings or variations in movie names entered by the user, the difflib library is used to find the closest match from the list of all movie titles in the dataset.


# 7 Movie Recommendations
Once the closest match is found, the system retrieves the index of the movie with the matching title. Using this index, the similarity scores for that movie are obtained from the similarity matrix. The movies are then sorted based on their similarity scores in descending order.


# 8The system suggests the top 10 movies with the highest similarity scores as recommendations for the user. The movie recommendations are displayed to the user along with their corresponding ranks.

# 9 Usage
To use the film recommendation system, follow these steps:
Ensure that the required dependencies are installed.
Load the movie dataset from the 'movies.csv' file.
Run the code provided, which includes functions for feature selection, data preprocessing, feature vectorization, similarity calculation, finding the closest match, and displaying movie recommendations.
When prompted, enter the name of a movie you like to receive personalized recommendations.

