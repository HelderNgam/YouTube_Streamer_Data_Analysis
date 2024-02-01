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

### 📖 Recommendations

### ⏳ Limitations


### 🔖 References

