# Recommendation_System
Recommendation System Competition Project based on Yelp Business Reviews Dataset

Method Description:

This code is a combination of collaborative filtering and XGBoost for predicting user ratings for businesses in a recommendation system. It utilizes PySpark for data processing and XGBoost for training and predicting.
The main part of the code starts by initializing the Spark context, loading the training and test data, and creating user-business dictionaries. 
Then, it computes rating averages for both users and businesses. The test data is processed, and collaborative filtering predictions are generated using the calculate_final_prediction() function.
Next, the code loads and processes user, business, and review features. The training and test datasets are created using these features. 
The XGBoost model is trained with the best parameters obtained through hyperparameter tuning (using Optuna and 5-fold cross-validation). The XGBoost model is then used to predict ratings on the test dataset.
Finally, the RMSE and error distribution for the XGBoost predictions are calculated using the compute_rmse_and_error_distribution() function.
The features used in this code for improving the RMSE (Root Mean Square Error) of the prediction model are a combination of user, business, and review-related features.
For user-related features, the following features are considered: useful, compliment_hot, fans, review_count, average_stars, compliment_funny, compliment_more, compliment_cool, compliment_profile, compliment_note, compliment_cute, compliment_list, compliment_plain, compliment_writer, and compliment_photos.
For business-related features, the following features are considered: review_count, stars, is_open, latitude, longitude, price range, acceptance of credit cards, bike parking, outdoor seating, restaurants good for groups, restaurants delivery, caters, hasTV, restaurants reservations, restaurants table service, outdoor seating, by appointment only, restaurants takeout, accepts insurance, wheelchair accessible, and good for kids.
For review-related features, the following features are considered: stars, useful, funny, and cool.
Using these features in combination with the collaborative filtering technique helped in improving the RMSE of the prediction model. Additionally, hyperparameter tuning using Optuna with 5-fold cross-validation was used to fine-tune the XGBoost model's hyperparameters to obtain better results.
Overall, these features' combination helped in better capturing the user's preferences, the business's characteristics, and the reviews' sentiment, thus improving the prediction.

Error Distribution based on Rating:<br />
<br />
Between 0 and 1: 102633,<br />
Between 1 and 2: 32447,<br />
Between 2 and 3: 6114,<br />
Between 3 and 4: 849,<br />
Greater than 4: 1

RMSE: 
0.9763456442333556

Execution Time:
1066.1266582012177s
