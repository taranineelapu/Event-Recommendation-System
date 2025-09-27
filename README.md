# Event Recommendation System

# Overview
This project develops a hybrid Event Recommendation System using collaborative filtering and content-based filtering techniques. By analyzing user-event interactions and event attributes, the system generates personalized event recommendations. This methodology is used for solving challenges like sparse data, lack of diversity, and low accuracy in traditional recommender systems.

# Objectives
* Deliver personalized event recommendations aligned with user preferences.
* Combine collaborative and content-based filtering to enhance accuracy and diversity.
* Preprocess and feature engineering to handle sparse and missing data effectively.
* Evaluate hybrid and alternate models for improved recommendation performance.

# Datasets
* events.csv → Event attributes (110 features, 1.09 GB)
* train.csv → User-event interactions (6 features)

# Methodology
* **Data Visualization:** Identified missing values, predictive, redundant, and irrelevant features.
* **Data Preprocessing:** Dropped irrelevant or incomplete features (e.g., location details) to refine datasets.
* **Model 1: Collaborative Filtering** Applied K-Nearest Neighbors (KNN) to capture user-user similarity.
* **Model 2: Content-Based Filtering** Used Cosine Similarity to capture event-event similarity.
* **Hybrid Model:** Combined recommendations from both models for personalized results.
* **Error Analysis & Tuning:** Applied RMSE with 10-fold cross-validation to optimize k in KNN (best at k=11).
* **Alternate Model:** Due to sparse user data, the model focused on content-based similarity, which yielded higher accuracy.

# Key Insights
* Sparse user-event interactions limited the accuracy of collaborative filtering.
* Optimal k=11 in KNN minimized RMSE and improved recommendation quality.
* Content-based filtering outperformed the hybrid model in recommendation accuracy.
* Preprocessing (dropping irrelevant features) was essential to enhance system performance.
* The final model recommends top 100 most similar events per user.

# Tools and Technologies
* **Language:** Python
* **Libraries:** Pandas, NumPy, scikit-learn, Matplotlib
* **Techniques:** K-Nearest Neighbors (KNN), Cosine Similarity, Cross-validation & RMSE error analysis
