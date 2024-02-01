# YouTube_Streamer_Data_Analysis

## Table of Contents

- [Project Overview](project-overview)
- [Data Sources](data-sources)
- [Tools](tools)
- [Data Cleaning/ Preparation](data-cleaning/-preparation)
- [Exploratory Data Analysis](exploratory-data-analysis)
- [Data Analysis](data-analysis)
- [Results](results)
- [Recommendations](recommendations)
- [Limitations](limitations)
- [References](references)

### 📌 Project Overview

This Data Analysis project aims to provide insights into the performance of top performing YouTube channels by analyzing various aspects that create/ build a great channels like the number of subscribers and visits. We will identify which categories are the most popular, identify trends, make data-driven recommendations and visualize the given data.

### 📚 Data Sources

Top 1000 YouTubers Data: The primary dataset used in this analysis is the "youtubers_df.csv" file, containing all the top 1000 YouTube channels with their total number of Subscribers, Views, Comments, Visits, Likes etc. 

[Access the file here](https://drive.google.com/drive/folders/1aQqtP9-OX3BwX-olp1vD0Zq9NYBKvtJu?usp=sharing)

### 🧰 Tools

- Anaconda Navigator: launching Jupyter Notebook 
  - [Download here](https://www.anaconda.com/download)
- Jupyter Notebook: Data Analysis
- Python
  - [Check out Python Syntax here](https://www.w3schools.com/python/default.asp)

### 🧹 Data Cleaning/ Preparation

In the intial phase of my data preparation, I performed the following tasks:
1. Data loading into Jupyter Notebook.

  ```python
  data = pd.read_csv (r"C:\Users\Eza\Desktop\Data Analysis Intern\youtubers_df.csv")
  ```
2. Handle missing values and ouliers.
3. Data cleaning and formatting.

### 👓 Exploratory Data Analysis

This step of the analysis invovled answering key questions:
- Which categories are the most popular?
- Is there a correlation between the number of subscribers and the number of likes or comments?
- Are there regional preferences for specific content categories?
- Are there patterns or anomalies in these metrics?
- Which categories have the highest number of streamers?
- Are there specific categories with exceptional metrics?
- Who are top-performing content creators?

### 📊 Data Analysis

The code used in the analysis to find the/ list the top-performing content creators:

```python
import pandas as pd

# Load the dataset
df = pd.read_csv(r"C:\Users\Eza\Desktop\Data Analysis Intern\youtubers_df.csv")

# Calculate average values for each performance metric
average_subscribers = df['Suscribers'].mean()
average_visits = df['Visits'].mean()
average_likes = df['Likes'].mean()
average_comments = df['Comments'].mean()

# Identify top-performing content creators
top_performers = df[
    (df['Suscribers'] > average_subscribers) &
    (df['Visits'] > average_visits) &
    (df['Likes'] > average_likes) &
    (df['Comments'] > average_comments)
]

# Display the top-performing content creators
print("Top-performing content creators:")
print(top_performers[['Rank', 'Username', 'Categories', 'Suscribers', 'Visits', 'Likes', 'Comments', 'Links']])
```

From the code above we able were to find that Mr Beast is the number 1 top-performing content creator with the highest number of subscribers and visits. 

*The Notebook will be attached for referral*

### ⚖️ Results

The results of the analysis are summarized as follows:
- The top Category is Música y baile.
- Eucador a country in South America has the largest Audience Distribution.
- The Averages of Subscribers, Visits, Likes and Comments in our dataset:
  - Average Subscribers: 21894400.0
  - Average Visits: 1209446.3155
  - Average Likes: 53632.592
  - Average Comments: 1288.768
- There is a positive correlation of 0.25 between the number of people who visit the channel and brand collaborations.
- Mr Beast is Number One on the the list of top-performing content creators with the highest number of Subscribers and Visits.

### 📖 Recommendations

Based on the anaysis we recommend you do the following steps to grow your channel:

1. Data Collection:

   - Collect data on streamers, including categories, performance metrics, user engagement, and historical user interactions.

2. Prepocessing Data:

   - In this stage of system we deal with outliers, missing values, and data consistency.
   - We must convert the categorical variables (Categories) into numerical representations using encoding techniques.

3. Feature Engineering:

   - Create derived features that represent weighted combinations of performance metrics to capture the overall influence of a streamer.
   - Normalize performance metrics to ensure equal weight in the recommendation algorithm.

4. Content Embeddings:

   - Utilize deep learning techniques to create embeddings for streamers based on their content, categories, and performance metrics.
   - Train neural networks to learn representations that capture the semantic meaning of streamers in a continuous vector space.

5. User Profile and Preference Learning:

   **a. User Profile Creation:**
   - Build user profiles based on historical user interactions, such as watched videos, likes, dislikes, and search history.

   **b. Collaborative Filtering:**
   - Implement collaborative filtering techniques (user-based or item-based) to identify user preferences based on similar users' behaviors.
   - Use matrix factorization methods like Singular Value Decomposition (SVD) or factorization machines to uncover latent features.

6. Hybrid Recommendation System:

    **Combine Collaborative Filtering and Content Embeddings:**
    - Create a hybrid recommendation system that leverages both collaborative filtering and content embeddings to enhance accuracy and coverage.
    - Weight the contributions of each method based on user behavior and context.

7. Real-time Personalization:

    **Dynamic User Profiles:**
    - Update user profiles in real-time based on user interactions to adapt to changing preferences.
    - Implement reinforcement learning techniques to adjust the recommendation model continuously.

8. Explainability and Transparency:

    **Provide Explanations:**
    - Include explanations for recommendations to enhance user trust and understanding.
    - Highlight which aspects of a streamer's content or performance metrics contribute to the recommendation.

9. A/B Testing and Evaluation:

    **Continuous Experimentation:**
    - Conduct A/B testing to evaluate the effectiveness of new recommendation algorithms.
    - Regularly update and refine the system based on user feedback and performance metrics.
    - In an A/B test, there are two versions of a product or service - Variant A (the control group, often the existing version or the current design) and Variant B (the experimental
      group, which includes changes or modifications being tested).

10. User Feedback Loop:

    **Feedback Collection:**
    - Implement mechanisms for users to provide explicit feedback on recommendations (likes, dislikes, feedback comments).
    - Analyze implicit feedback, such as watch time and engagement, to further refine recommendations.

11. Privacy and Security:

    **Data Protection:**
    - Ensure compliance with privacy regulations and prioritize user data protection.
    - Anonymize and aggregate user data to minimize the risk of personally identifiable information exposure.

### ⏳ Limitations

I had to remove all missing values and outliers as they would affected the quality of my analysis and accuracy of my conclusions.

### 🔖 References

1. Data Analysis with Python - Full Course For Beginners.
   - [Watch Here](https://youtu.be/r-uOLxNrNk8?si=eltgSxU48XN_SQYN)
   
2. How to Find Outliers in Data Using Python.
   - [Read Here](https://careerfoundry.com/en/blog/data-analytics/how-to-find-outliers/)
  
3. Python Syntax.
   - [Read Here](https://www.w3schools.com/python/)

