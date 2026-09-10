# **🎬 Zee Recommender Systems**
Personalized Movie Recommendation Engine using Collaborative Filtering & Matrix Factorization

# **📌 Problem Statement**

Zee aims to enhance user engagement and viewing experience by providing personalized movie recommendations. This project builds a recommendation engine that suggests movies based on historical user ratings and similarity between users and items.

The solution explores multiple recommendation approaches:

- Item-Based Collaborative Filtering using Pearson Correlation
- Item-Based Collaborative Filtering using Cosine Similarity
- K-Nearest Neighbors (KNN)
- Matrix Factorization using Singular Value Decomposition (SVD)
- Embedding-Based User and Item Similarity Models

# **🎯 Business Objective**
- Improve user engagement through personalized recommendations.
- Increase content discovery and watch time.
- Recommend relevant movies based on user preferences and historical behavior.
- Leverage collaborative filtering techniques to identify hidden viewing patterns.
- Build scalable recommendation models for real-world streaming platforms.

# **📊 Dataset Overview**

The project uses the MovieLens dataset containing:

**Ratings Dataset**
1,000,209 user ratings, 6,040 users, 3,952 movies, and Ratings on a 1-5 scale

**Movies Dataset**
Movie ID, Movie Title, and Genres

**Users Dataset**
User demographics, Age, Gender, Occupation, Zip Code

Final Dataset after merging all datasets: 1,000,209 Records,	6,040 Users, and 3,883 Movies

# **🧹 Data Cleaning & Feature Engineering**
Preprocessing Steps:

- Imported and merged ratings, users, and movies datasets
- Verified data quality and consistency
- Removed duplicate records
- Checked for missing values
- Converted rating data types
- Extracted Release Year from movie titles
- Created Release Decade feature
- Generated movie-level statistics: Average Rating and Number of Ratings
- Created User-Item Interaction Matrix
- Imputed missing ratings with 0 for collaborative filtering models

# **📈 Exploratory Data Analysis (EDA)**
## **User Behavior Insights:**
- Age group 25-34 contributed the highest number of movie ratings.
- College/Graduate Students represented the most active occupation group.
- Male users accounted for the majority of ratings in the dataset.

## **Content Insights:**
- Most movies in the dataset were released during the 1990s.
- Comedy and Drama were the most common genres.
- American Beauty received the highest number of ratings.

## **Rating Insights:**
- User-item matrix exhibited approximately 95.5% sparsity, highlighting the need for dimensionality reduction and latent-factor based methods.
- Highly rated movies were not always the most popular, demonstrating the need for recommendation algorithms beyond popularity-based suggestions.

# **🤖 Recommender Systems Implemented**
# **1️⃣ Pearson Correlation Based Collaborative Filtering**
## **Approach**
- Created movie-user pivot table.
- Computed item-item Pearson Correlation matrix.
- Built recommendation engine to suggest similar movies.

## **Example Recommendation**
Input Movie: Liar Liar

Recommended Movies:
- Mrs. Doubtfire
- Dumb & Dumber
- Ace Ventura: Pet Detective

# **2️⃣ Cosine Similarity Based Collaborative Filtering**
## **Approach**
- Constructed Item Similarity Matrix
- Constructed User Similarity Matrix
- Computed cosine similarity between movies and users
- Implemented item-based recommendation engine

## **Additional Enhancement**

Implemented:

✅ K-Nearest Neighbors (KNN)

✅ Sparse CSR Matrix Representation

✅ Item-to-Item Recommendation Search

# **3️⃣ Matrix Factorization (SVD)**

Matrix Factorization was used to uncover latent interactions between users and movies.

## **Model Configuration**
Algorithm: Singular Value Decomposition (SVD)

Latent Dimensions: d = 4

Train-Test Split: 80:20

Evaluation Metrics

Metric	ScoreRMSE	0.8775

MAPE	26.74%

- The model successfully captured hidden user preferences and movie characteristics, improving recommendation quality over sparse similarity-based approaches.

# **🔍 Embedding-Based Similarity**

Using latent embeddings generated from SVD:

## **Item Embeddings**
- Generated 4-dimensional movie embeddings.
- Computed movie-to-movie similarity using embedding vectors.

## **User Embeddings**
- Generated 4-dimensional user embeddings.
- Identified highly similar users through cosine similarity.

## **Visualization**
- Trained a 2-dimensional latent space model.
- Visualized movie clusters in embedding space.
- Observed grouping of movies with similar hidden characteristics and user preferences.

# **📊 Key Insights**
**User Demographics**
- Age Group 25-34 generated the highest engagement.
- College/Graduate Students formed the largest active audience segment.
- The dataset is predominantly male, introducing potential demographic bias.

**Recommendation System Insights**
- Collaborative filtering effectively captured user preferences.
- Matrix Factorization significantly reduced sparsity challenges.
- Embedding-based similarity produced more robust recommendations compared to raw rating correlations.
- User-based recommendations become stronger when users provide more ratings, increasing similarity confidence.

# **💡 Recommendations**
- Deploy a hybrid recommendation system combining Collaborative Filtering and Matrix Factorization.
- Use embedding-based similarity for improved scalability.
- Encourage additional user ratings to reduce sparsity.
- Filter low-rated or low-interaction movies before recommendation generation.
- Continuously retrain recommendation models to adapt to changing user preferences.

# **🛠 Tech Stack**

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

SciPy

Surprise (SVD)

Jupyter Notebook

# **⚠️ Limitations**
- Cold-start problem for new users and movies.
- Recommendations rely primarily on historical ratings.
- Limited demographic features used in recommendation generation.
- Sparse interaction matrix impacts neighborhood-based methods.

# **🚀 Future Improvements**
- Implement Neural Collaborative Filtering (NCF).
- Explore Deep Learning based recommendation architectures.
- Integrate content-based filtering using movie genres and metadata.
- Develop hybrid recommendation systems.
- Deploy recommendations through an interactive web application.

# **📌 Project Outcome**

Developed an end-to-end movie recommendation engine leveraging Collaborative Filtering, KNN, Cosine Similarity, Pearson Correlation, and Matrix Factorization techniques to generate personalized recommendations and improve content discovery through latent user-item preference modeling. 🚀
