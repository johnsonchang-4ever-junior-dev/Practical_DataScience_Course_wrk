# Evaluating Recommender System Methods
*By Johnson Chang*

## Five Approaches to Rating Prediction

• **Method 1:** Calculate the average rating given by the user, and use it as the prediction for how the user will rate a movie.
• **Method 2:** Calculate the average rating received by each movie, and use it as the prediction for how that movie will be rated.
• **Method 3:** Find users with similar rating patterns to predict the target user's rating.
• **Method 4:** Find items that are rated similarly by users to predict missing values.

## Optimising Method 3 & Method 4 — User-based KNN and Item-based KNN

• Use print(df.shape) to know that there're 100K ratings.
• K should not be set too close to 100K
• Tested different K values to find optimal K
• In User-based KNN: K is the number of similar users with matching rating behaviour.
• In Item-based KNN: K is the number of similar items rated similarly across users.

## Optimising Method 5 — Hybrid KNN

• In Method 5, the only parameter to optimise is λ (lambda).
• Tuned λ from 0 to 1 to find the best weighting.
• λ controls how much we trust user-based prediction vs item-based prediction.

## Performance Analysis

• Method 5 provides the most accurate predictions by combining both perspectives.
• Method 4 outperforms Method 3 because predictions using similar items (movies) are often more reliable — not every user rates every movie, but each movie is rated by many users.
• Method 1 & 2 perform the worst: they are too general and don't consider similarities.