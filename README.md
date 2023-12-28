# Claim-Opinion-Classifier-TikTok

# Overview
The goal of this project was to create a random forest model and XGBoost to classify TikTok videos as claims of opinions. This project utilized a synthetic dataset created in association with TikTok. A data dictionary has been added to assist in the understanding to the dataset. The final random forest model performed with 99.5% Recall . Performance on the test holdout data yielded near perfect scores, with only five misclassified samples out of 3,817 . Also determined what features were most important in separating claims and opinions. Based on the model, video view count , video like count and video share count were the most influential in determining a video to be a claim or an opinion.

# Business Understanding
TikTok videos receive a large number of user reports for many different reasons. Not all reported videos can undergo review by a human moderator. Videos that make claims (as opposed to opinions) are much more likely to contain content that violates the platform’s terms of service. TikTok seeks a way to identify videos that make claims to prioritize them for review. Links to refer - 
https://newsroom.tiktok.com/en-us/safety 
https://www.tiktok.com/forgood 

# Data Understanding
The data consisted of approximately 19383 published videos and 12 features. The features included information on count of video views , video likes , video shares and video duration, user status and claim status. Approximately 50.3% of the dataset represents claims and 49.7% represents opinions. In connection to this, new features were engineered to represent phrases used in video text description for a claim and an opinion.

# Modeling and Evaluation
A random forest model comprising 200 decision trees was used to determine feature importance in which video is a claim or an opinion. The below plot shows that video view count , video like count and video share count were the Top 3 most important factors in determining a video to be a claim or an opinion. The overall model performed with 99.5% Recall.

![TikTok-1](https://github.com/IamMayur95/Claim-Opinion-Classifier-TikTok/assets/67839699/980bd326-ac6a-4986-bf53-279430f870ed)


Confusion matrix for the champion RF model on test holdout data shows only five misclassified samples out of 3,817.

![TikTok-2](https://github.com/IamMayur95/Claim-Opinion-Classifier-TikTok/assets/67839699/4141ea12-7627-4662-8517-0573d1327b6d)

# Conclusion
As noted, the model performed exceptionally well on the test holdout data. With these results, we can conclude that videos with higher user engagement levels were much more likely to be claims. In fact, no opinion video had more than 10,000 views. This model can be benefitial for TikTok to reduce the backlog of user reports and prioritize them more efficiently. 
