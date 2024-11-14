# TikTok Data Analysis Project

This project involves an exploratory data analysis (EDA) of a TikTok dataset to uncover insights into video engagement and user behavior. Using Python, this project performs data cleaning, visualization, and analysis to support data-driven insights for the TikTok team.

## Project Overview

The goal of this project is to:
1. **Structure and clean** the data for analysis.
2. **Explore and visualize** patterns in video metrics, user behavior, and engagement.
3. **Identify insights** that could inform future strategic decisions.

Key areas of analysis include claim vs. opinion counts, video engagement metrics (such as duration, likes, comments, views), and the distribution of author ban statuses.

## Table of Contents

- [Technologies Used](#technologies-used)
- [Data Cleaning and Structuring](#data-cleaning-and-structuring)
- [Exploratory Data Analysis](#exploratory-data-analysis)
  - [Claim Counts vs. Opinion Counts](#claim-counts-vs-opinion-counts)
  - [Boxplots of Engagement Metrics](#boxplots-of-engagement-metrics)
  - [Author Ban Status Breakdown](#author-ban-status-breakdown)
- [Installation and Setup](#installation-and-setup)
- [How to Use](#how-to-use)
- [Results and Insights](#results-and-insights)
- [Contributing](#contributing)
- [License](#license)

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn

## Data Cleaning and Structuring

1. **Missing Values**: Inspected for missing values in all columns and applied appropriate handling strategies (e.g., filling, dropping, or imputing).
2. **Data Types**: Converted columns to the correct data types to ensure compatibility with analytical methods.
3. **Duplicates**: Checked for duplicates in the dataset and removed them if necessary to maintain data integrity.

## Exploratory Data Analysis

### Claim Counts vs. Opinion Counts

A scatter plot visualizes the relationship between claim counts and opinion counts, highlighting potential correlations or patterns in how content is perceived by the audience.

```python
import matplotlib.pyplot as plt
import seaborn as sns

# Scatter plot for Claim Counts vs. Opinion Counts
plt.figure(figsize=(10, 6))
sns.scatterplot(x='claim_count', y='opinion_count', data=df)
plt.title("Claim Counts vs. Opinion Counts")
plt.xlabel("Claim Count")
plt.ylabel("Opinion Count")
plt.show()




Boxplots of Engagement Metrics
Boxplots help detect outliers and understand the distributions of key engagement metrics, including:

Video Duration
Video Like Count
Video Comment Count
Video View Count

important_vars = ['video_duration', 'video_like_count', 'video_comment_count', 'video_view_count']
plt.figure(figsize=(15, 10))
for i, var in enumerate(important_vars, 1):
    plt.subplot(2, 2, i)
    sns.boxplot(data=df, x=var)
    plt.title(f"Boxplot of {var}")
plt.tight_layout()
plt.show()

Author Ban Status Breakdown
A bar plot visualizes the distribution of author ban statuses, showing the prevalence of each status and offering insights into community behavior and content moderation patterns.

# Count plot for Author Ban Status
plt.figure(figsize=(8, 6))
sns.countplot(x='author_ban_status', data=df, palette="viridis")
plt.title("Author Ban Status Counts")
plt.xlabel("Ban Status")
plt.ylabel("Count")
plt.show()

Results and Insights
Key Findings
Claim vs. Opinion Correlation: Initial analyses showed that claim and opinion counts had specific patterns that could inform content strategies.
Video Engagement Outliers: Boxplot analysis of engagement metrics identified outliers in video duration and views, suggesting certain types of content may drive higher engagement.
Author Ban Patterns: The breakdown of ban statuses provided insights into the content moderation landscape, helping the TikTok team understand community dynamics.
Future Directions
Apply machine learning models for further analysis.
Conduct A/B testing on the highest-engagement content types.
Contributing
Contributions are welcome! Please fork this repository, make your changes, and submit a pull request.

