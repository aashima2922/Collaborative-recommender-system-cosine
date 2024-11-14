# Collaborative-recommender-system-cosine
Collaborative Recommender System using Cosine similarity

Item-Based Collaborative Filtering Recommendation System
This project builds an item-based collaborative filtering recommendation system that recommends items similar to those a user has interacted with. It uses cosine similarity to measure similarity between items and identify items that users may like based on their past interactions.

How It Works
Data Loading:

The system reads three main files:
items.csv: Information about each item (e.g., ID, category).
users.csv: Information about each user (e.g., ID, country).
events.csv: User interactions with items, with timestamps.
Training - Calculating Item Similarity:

The system creates a user-item interaction matrix that shows which users interacted with which items.
Cosine similarity is then used to calculate similarity between items. Items with high similarity scores are likely to be recommended together.
Session Analysis:

User events are grouped into sessions if there is an 8-hour gap between events.
Duplicate item visits within a session are removed, and sessions with only one event are excluded.
The system calculates statistics like the number of sessions, average events per session, and bounce rates.
Generating Recommendations:

For a given session, the system finds similar items based on items in the session history.
It recommends the top 5 items that are most similar to those in the current session.
Evaluation:

The system is evaluated by checking if the recommended items include a target item, calculating the accuracy of recommendations.
Usage
Set Up Files: Ensure items.csv, users.csv, and events.csv are in the same directory as the code.

Output:
The program prints session statistics, recommended items, and evaluation results showing recommendation accuracy.
