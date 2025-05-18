# 🎯 TikTok Video Claim Classification — Google Advanced Data Analytics Capstone
## Project: Analyzing User Engagement and Predictive Moderation on TikTok

This project was completed as part of the Google Advanced Data Analytics Certificate. I analyzed a dataset of approximately 19,000 TikTok videos with the goal of supporting content moderation by identifying whether a video presents a **"Claim"** or an **"Opinion"**.

TikTok receives a high volume of user reports flagging content for potential misinformation or personal views. To assist moderators and streamline the review process, the objective was to explore the data and develop models that can classify videos based on their metadata and engagement metrics.

![Untitled](https://github.com/RoniF-pixel/Projects/assets/121540731/070ae4ab-61d3-4132-be21-7fd8a9d6088f)

## 🔍 Project Objectives
#### 1. View Count Comparison: Verified vs. Unverified Accounts
- **Goal**: Determine whether verified accounts receive more views than unverified ones.
- **Method**: Hypothesis testing
- **Result**: There was a statistically significant difference—verified accounts tend to have higher view counts on average.

#### 2. Text Length Feature Engineering
- Engineered a new feature called text_length, measuring the character count of video_transcription_text.
- Used this to compare the nature of video transcriptions between verified and unverified users.
- This helped explore whether verified accounts tend to publish more elaborate or complex content.

#### 3. Logistic Regression Model: Predicting Verified Status
- Built a logistic regression model using video features to predict whether an account is verified.
- Key Insight: Longer videos were associated with higher odds of being from verified accounts.
- Other features had weaker predictive value, indicating a possible content-length verification bias.

#### 4. Classification Models: Claim vs. Opinion
- Goal: Predict whether a video presents a claim or an opinion.
- Built two models:
    - Random Forest
    - XGBoost
- Both models performed exceptionally well (near-perfect classification), with the random forest slightly outperforming XGBoost.
- Top Predictive Features:
    - Number of views
    - Likes
    - Shares
    - Downloads
      These indicate that user engagement metrics were highly predictive of the nature of the video content.

## 🧠 Key Takeaways
- Demonstrated the ability to handle a real-world classification problem involving social media content moderation.
- Applied statistical hypothesis testing, feature engineering, and machine learning (logistic regression, random forest, XGBoost).
- Addressed imbalance and potential bias by interpreting engagement-driven predictions carefully.
- Gained experience in interpreting model outputs to inform business and operational decisions.

![image](https://github.com/RoniF-pixel/Projects/assets/121540731/fedccf58-6eb0-491b-871d-3c4ba9e9bd99)

## 📂 Repository & Files
- Jupyter Notebook: [tiktok-analysis.ipynb](https://github.com/RoniF-pixel/Python-Projects/blob/main/TikTok/Tik%20Tok.ipynb)
Includes EDA, model training, evaluation metrics, and visualizations.

This project showcases rigorous exploratory analysis, craft interpretable models, and support practical, high-impact applications in tech platforms. I hope you find this repo a helpful demonstration of my **data analytics**, **machine learning**, and **feature engineering skills!**
