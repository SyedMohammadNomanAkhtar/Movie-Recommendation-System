# Movie-Recommendation-System
[Dataset] (https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata/metadata)

##Download both the datasets Credita and Movies as both are going to be used in the system

A recommender system is a system that helps users discover movies or series they may like. It is like a salesman of a company who knows what a user might like based on their watch history and preferences. It is an application of different algorithms that combine to predicts the future preference of a set of movies for a user and provides personalized suggestions.

Types of Recommender Systems:
  1. Content Based Filtering
  2. Colabrative Filtering

### I have build Content Based Recommender System

Content-based recommendation systems work more closely with item attributes rather than user data. They predict the behavior of a user based on the items they watch to.

### Import and Load the TMDB 5000 Movie Dataset from the given link above
First you need to import the necessary packages and libraries from the Kaggle Movie Dataset
after that you need to check the columns in the dataset.
The file credits.csv contains attributes like movie_id, title, cast, and crew, and the movies.csv dataset file contains columns like genres, keywords, overview, budget etc.

### Analyzing Documents with TF-IDF

Term frequency is the relative frequency of any word in a document and is given by dividing term instances with total instances.

The other part IDF called Inverse Document Frequency is the relative count of documents containing the term and is given as a log (number of documents/documents with the term).

The overall importance of each word in the document in which they appear would be given by  TF * IDF.

This will give you a matrix where each column represents a word in the overall vocabulary (all the words that appear in at least one document)
and each row represents a movie.

TF-IDF is useful in reducing the importance of words that occur frequently in our movie description function(create_join), genre, and keyword would in turn, reduce their significance in computing the final similarity score.

### Calculating the Cosine Similarity

I have used cosine similarity to compute similarity. 
I used cosine similarity score because it is independent of magnitude and is also relatively easy and fast to calculate.

## Time to Make a Recommendation
   ### Steps
    1. Retrieve the index of the movie given its title.
    2. Compute a list of cosine similarity scores for the target movie with all movies in the dataset then convert it into a list of tuples.
    3. Sort this list of tuples based on similarity scores
    4. Get the top 10 elements(or more) of this list.
    5. Return the titles that correspond to the indices of the top elements.






























