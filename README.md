# Content-Based Movie Recommendation

The Content-Based Movie Recommendation system is a project that suggests movies to users based on the similarity of movie features. It utilizes the content or attributes of movies such as genres, keywords, cast, crew, and overview to generate recommendations.

## Description

The project involves the following steps:

1. Data Preparation:
   - The movie data is loaded from the "tmdb_5000_movies.csv" file, which contains information about various movies.
   - The movie credits data is loaded from the "tmdb_5000_credits.csv" file, which includes details about the cast and crew of movies.
   - The two datasets are merged based on the movie title to create a consolidated movie dataset.

2. Data Preprocessing:
   - The necessary columns for training the model are selected from the dataset.
   - Null values are dropped from the dataset.
   - The genres and keywords columns are converted from string format to lists using the `ast.literal_eval()` function.
   - The cast column is filtered to retrieve the three most known cast names.
   - The crew column is processed to extract the director's name.
   - The overview column is split into a list of words.
   - All the extracted features are combined into a new column called "tags".

3. Data Vectorization:
   - The tags column is converted into vectors using the `CountVectorizer` from the scikit-learn library.
   - Cosine similarity is calculated between each vector to determine the similarity between movies.

4. Movie Recommendation:
   - The system takes a user-selected movie as input.
   - Based on the similarity scores, the top 5 most similar movies are recommended.
   - The recommended movies are displayed to the user.

## Technologies Used

The Movie Recommendation system is developed using the following technologies and libraries:

- Python: Programming language used for the project implementation.
- pandas: Library for data manipulation and analysis.
- NumPy: Library for mathematical operations on arrays and matrices.
- scikit-learn: Library for machine learning tasks such as data preprocessing and similarity calculations.
- Streamlit: Framework for building interactive web applications.
- pickle: Library for serialization and deserialization of Python objects.

## Usage

To use the Content-Based Movie Recommendation system:

1. Install the required dependencies by running:
   ```
   pip install pandas numpy scikit-learn streamlit
   ```

2. Clone the project repository:
   ```
   git clone https://github.com/your-username/content-based-movie-recommendation.git
   ```

3. Navigate to the project directory:
   ```
   cd content-based-movie-recommendation
   ```

4. Run the Streamlit application:
   ```
   streamlit run app.py
   ```
   
5. Select a movie from the dropdown list and click the "recommend" button to get the recommended movies.

## Dataset

The movie dataset used in this project is obtained from the TMDB (The Movie Database) website. It includes information about movies such as titles, genres, keywords, cast, crew, and overview.

