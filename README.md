# Recommendation_system

COMPANY : CODTECH IT SOLUTIONS

NAME : SHREYA YADAV

INTERN ID : CT04DG3452

DOMAIN : MACHINE LEARNING

DURATION : 4 WEEKS

MENTOR : NEELA SANTOSH

## 🎬 Recommendation System using SVD (Singular Value Decomposition)

This project focuses on building a personalized movie recommendation system using collaborative filtering techniques on the MovieLens 100K dataset. The system leverages the Surprise Python library, specifically using Singular Value Decomposition (SVD), one of the most popular matrix factorization methods for recommender systems.

📦 Dataset Overview
The MovieLens 100K dataset is a benchmark dataset for recommendation tasks, containing 100,000 movie ratings from 943 users across 1,682 movies. Each user has rated at least 20 movies, and the ratings range from 1 to 5 stars. This dataset is ideal for collaborative filtering as it includes sufficient user-item interactions for learning preferences.

The dataset is loaded using Surprise’s built-in Dataset.load_builtin('ml-100k') function, which automatically formats the data for model training.

🔧 Model Building with Surprise
The project uses Surprise, a specialized library for building and evaluating recommender systems. The key steps are:

Data Loading: The MovieLens 100K dataset is loaded in Surprise’s expected format using a built-in Reader class.
Algorithm Selection: The SVD algorithm from Surprise is used for building the model. SVD decomposes the user-item interaction matrix into latent user and item features.
Model Evaluation: The model is evaluated using 5-fold cross-validation with performance metrics including Root Mean Square Error (RMSE) and Mean Absolute Error (MAE). These metrics help in understanding how close the predicted ratings are to the actual user ratings.
🧠 How SVD Works
SVD is a matrix factorization technique that reduces the user-item interaction matrix into three lower-dimensional matrices representing:

User preferences (latent features)
Item characteristics
Interaction strength between users and items
By learning these latent representations, SVD can estimate how a user might rate a movie they haven't seen yet. This is especially effective in cases where the rating matrix is sparse.

🔍 Generating Recommendations
Once the model is trained on the full dataset, the system identifies unrated items for a given user and predicts ratings for them. Specifically:

For a given user_id, the system extracts the list of movies the user has already rated.
Then, it identifies all the other movies the user has not interacted with.
It uses the trained SVD model to predict ratings for these unseen movies.
Finally, it ranks the movies based on predicted ratings and recommends the top-rated ones to the user.
This approach allows the system to make personalized recommendations even for users it has seen during training.

📈 Evaluation & Results
Through cross-validation, the SVD model typically achieves low RMSE and MAE scores, indicating good prediction accuracy. The approach is scalable and performs well even with large and sparse datasets, making it widely used in real-world systems like Netflix and Amazon.

💡 Key Takeaways
SVD-based collaborative filtering is a powerful method for personalized recommendations.
The Surprise library simplifies model building, evaluation, and deployment.
Real-world recommendation systems rely heavily on such matrix factorization techniques.
Understanding user behavior through implicit patterns (like ratings) leads to effective personalization.
