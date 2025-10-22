# MOVIE-LENS
This project utilizes a multi-source movie dataset to perform Exploratory Data Analysis (EDA) and feature engineering for potential movie recommendation or rating prediction models.

# Movie Rating Data Analysis & Feature Engineering
This repository contains the code and documentation for the Exploratory Data Analysis (EDA) and Feature Engineering phase of a project analyzing user movie ratings, tags, and genres. The goal is to transform raw timestamp and text data into a robust feature set suitable for downstream applications like a movie recommender system or rating prediction model.

# 💻 Project Workflow
1. Data Acquisition and Merging
The final dataset was created by sequentially merging four separate data files: movies, links, ratings, and tags.

- Libraries Used: pandas, numpy, matplotlib, seaborn.

- Merge Keys: All datasets were combined primarily using the movieId key.

- Conflict Resolution: Suffixes ('rating', 'tag') were used to differentiate columns like userId and timestamp coming from the distinct rating and tagging datasets.

2. Data Cleaning and Preparation
The merged data was cleaned and prepared for analysis:

- Duplicate rows were removed.

- Missing values were addressed (e.g., dropped for critical columns).

- Timestamp columns were converted to datetime objects for easy feature extraction.

# ⚙️ Feature Engineering
Nine essential features were engineered to provide crucial temporal and structural context, significantly enhancing the predictive power of the dataset:

•	Movie release year from the movie title that shows the year each movie was released.
•	Year of rating from rating timestamp to Detect long-term trends 
•	Month of rating from rating timestamp to Identify monthly seasonality 
•	Day of the week of rating from rating timestamp to Identify weekly patterns
•	Year of tag from tag timestamp to Track the evolution of movie tags and their relevance.
•	Month of tag from tag timestamp to capture monthly seasonality in tagging behavior
•	Day of the week of tag from tag timestamp to capture weekly patterns in tagging behavior
•	Number of genre per movie to Measure a movie’s genre diversity 
•	Number of ratings that counts the number of ratings per movie measuring the popularity or exposure of a movie.



# 📊 Exploratory Data Analysis (EDA) Highlights
The EDA revealed compelling insights into user behavior and movie attributes:

1. Rating Sentiment & Distribution
Finding: The distribution of ratings is heavily left-skewed, with major peaks at 4.0 and 5.0.

Implication: Users tend to rate movies positively, or the dataset contains a high proportion of generally well-received films.

2. Genre Complexity (Multi-Genre Trend)
Finding: The majority of movies in the dataset are multi-genre, typically falling into 2–4 categories.

Implication: This indicates a common practice in filmmaking to blend genres to appeal to wider audiences, reinforcing the need to handle multi-label genre data in modeling.

3. Movie Quality Over Time
Finding: The average rating by release year hovers consistently between 3.8 and 4.2 from 1995 to 2017.

Implication: This suggests a stable standard of audience satisfaction, though visible peaks (e.g., 1996, 2011) suggest "golden eras" for highly-rated releases.

4. Genre & Tag Performance
Highest Rated: Genres like Crime, War, and Thriller showed the highest average ratings (near 4.0+). Tags like 'sci-fi' and 'thought-provoking' also scored highest.

Lowest Rated (Relative): Genres like Children, Fantasy, and Romance had the lowest averages (though still respectable).

5. User Activity Patterns
Finding: Rating activity peaks on Mondays and Sundays, and is lower on Saturdays.

Implication: This is a key behavioral signal: users are likely watching movies over the weekend and submitting their ratings during subsequent downtime (Sunday evening/Monday morning).

# Conclusion
The Exploratory Data Analysis (EDA) of the movie rating dataset reveals several critical insights into both the movie catalog and user behavior. The data exhibits an overall strong positive sentiment, with the vast majority of ratings clustered at 4.0 and 5.0. The analysis successfully identified structural popularity metrics, confirming that most movies are multi-genre (2-4 categories). Crucially, the highest-rated movies tend to fall into the Crime, War, and Thriller genres, and are often described by users with highly qualitative tags like 'thought-provoking' and 'sci-fi'. Finally, the feature engineering process unveiled a clear weekly activity pattern: users are most active in submitting ratings on Mondays and Sundays, suggesting a post-weekend viewing behavior. These engineered features and analytical insights provide a robust foundation for building effective predictive models.
