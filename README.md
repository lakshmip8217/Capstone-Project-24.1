### 2024 Campaign Truth Social Truths

**Lakshmi Mannuru**
#### Executive summary
Truth Social is a media and technology platform owned by Political Leader, designed to give people a space to express their voices, share posts, and connect with others across the country. The goal of this dataset is to analyze how Truth Social is used for outreach, examining the content and interactions to understand its impact. This project will involve applying preprocessing techniques to clean the data, training a model to analyze the data, and predicting outcomes based on user engagement and content patterns

#### What are you trying to answer?
To analyze the Sentimennt Analysis and seggreagate the reviews as positive, negative, neutral etc

#### Data Sources
https://www.kaggle.com/datasets/muhammetakkurt/trump-2024-campaign-truthsocial-truths-tweets

#### Methodology
As part of preprocessing removed all NaN and considered status_text, likes, shares, replies, verified_badge_post_date as features. To create a target column, defined positive and negavtive words, apply the categorize_sentiment function on status_text column to identify whether the text is positvie(1), negative(-1) or neutral (0). Used RandomForestClassifier for traning the model. 

#### Results
Precision = 1.00 for the class Negative, means the model was perfect at predicting negative instances when it predicted negative
Precision = 0.95 for the class Neutral, 95% were correctly classified as neutral.
Precision = 0.98 for the class Positive, 98% were actually positive.

#### Next steps
What suggestions do you have for next steps?
For negative sentiment (1.00), the recall is low (0.36). This means the model rarely identifies negative sentiment correctly. Even though it doesn't make mistakes when predicting negative instances, it doesn't predict many instances as negative at all, leading to a high number of false negatives.
For Neutral sentiment, The model has very high precision (0.95) and perfect recall (1.00), indicating that it is excellent at identifying neutral sentiments without misclassifying them. It has the best overall performance in terms of both precision and recall.
For positive sentiment, The model has high precision (0.98) and recall (0.95), which suggests that it performs well in identifying positive sentiment. Both precision and recall are quite balanced.
The overall accuracy of 0.96 shows that the model performs well in general, but the low recall for negative sentiments (class -1) suggests that the model may be biased towards neutral and positive classes.
To improve performance for negative sentiment classification, fine-tuning the model might be necessary.

### Outline of project
https://github.com/lakshmip8217/CapStoneProject_20.1/blob/main/capstone_project.ipynb

### Contact and Further Information
lakshmi.mannuru17@gmail.com
