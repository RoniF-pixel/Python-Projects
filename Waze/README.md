Machine learning model to predict whether or not a Waze user is retained or churned.

- Churn quantifies the number of users who have uninstalled the Waze app or stopped using the app. This project focuses on monthly user churn. 
- We found out that users who churned drove farther and longer in fewer days than retained users. They also used the app about half as many times as retained users over the same period.
- Less than 18% of users churned, and ~82% were retained.
- Finally, the XGBoost model fit the data better than the random forest model. The recall score is nearly double the recall score from the logistic regression model, and it's almost 50% better than the random forest model's recall score, while maintaining a similar accuracy and precision score.
- The model predicted three times as many false negatives than it did false positives, and it correctly identified only 16.6% of the users who actually churned.
