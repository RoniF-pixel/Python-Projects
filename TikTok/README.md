This is the TikTok dataset analyzed by me. It was a great part of my project of Google Advanced Data Analytics course. TikTok users have the ability to submit reports that identify videos and comments that contain user claims. These reports identify content that needs to be reviewed by moderators. The process generates a large number of user reports that are challenging to consider in a timely manner. 
TikTok is working on the development of a predictive model that can determine whether a video contains a claim or offers an opinion. With a successful prediction model, TikTok can reduce the backlog of user reports and prioritize them more efficiently.

![Untitled](https://github.com/RoniF-pixel/Projects/assets/121540731/070ae4ab-61d3-4132-be21-7fd8a9d6088f)

We had three goals:

- First, after going through EDA process, we are asked to see if there is no diference in number of views between TikTok videos posted by verified accounts and TikTok videos posted by unverified accounts. The data consisted of approximately 19k unique videos and 12 features.We used hypothesis testing which resulted in a statistically significant difference in the average view counts between videos from verified accounts and videos from unverified accounts.
- We engineered a feature called `video_transcription_text`, to see if there is a difference in `video_transcription_text` length for videos posted by verified accounts and videos posted by unverified accounts.
- Then, we developed a logistic regression model for verified status based on video features. Based on the model, we predicted that longer videos tend to be associated with higher odds of the user being veified. Other features associated with verified status seemed to be small.
- Finally, we built models that whether a TikTok video presents a "Claim" or presents an "Opinion". We built two models, Rndom Forest model and XGBoost model. Both resulted in perfect models, but random forest performed a little bit better. The model's most predictive features were all related to the user engagement levels associated with each video. It was classifying videos based on how many views, likes, share, and downloads they received.

![image](https://github.com/RoniF-pixel/Projects/assets/121540731/fedccf58-6eb0-491b-871d-3c4ba9e9bd99)

Hope this reop will help you to assess my coding, data analytics skills or will be just fun for you to look through. 
