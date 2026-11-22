# Instagram Insights: From BI to Predictive Intelligence

A Business Intelligence mini project built at Tunis Business School. It takes Instagram post-level analytics from raw CSV to a MySQL data warehouse, Power BI dashboards and machine learning models, to understand what drives engagement and to support content strategy.

**Team:** Malek Omri, Aicha Hriz, Rihem Abdelmoumen

## Objectives
- **Content performance:** compare engagement across media types, content categories, traffic sources and posting periods.
- **Engagement patterns:** analyze likes, comments, shares and saves by content type, traffic source and time.
- **Audience growth:** study engagement rate, reach, impressions and followers gained by category and media type.
- **Strategic insights:** turn the findings into content and posting recommendations.

## Data
Instagram Analytics dataset from Kaggle: a single CSV table of post-level observations over 12 months, covering media type, content category, caption and hashtag characteristics, engagement metrics, reach, impressions, traffic sources and follower growth. This is a public dataset, not data from a real client account.

## Architecture and Tools
| Stage | Tool | What it does |
|---|---|---|
| Extract | Python (pandas) | Loads the CSV and saves the raw data to a staging area unchanged |
| Transform | Python | Cleans, validates and structures data into fact and dimension tables |
| Load | Python + MySQL | Creates tables, loads data, handles errors and integrity checks |
| Model | MySQL | Data warehouse with a fact table and dimension tables |
| Visualize | Power BI | Connects to the warehouse, defines relationships, builds interactive dashboards |
| Predict | Python | Linear Regression and K-Means clustering on warehouse data |

## Machine Learning
- **Linear Regression:** measures the effect of media type, content category, reach, impressions and posting time on engagement, to identify key drivers.
- **K-Means Clustering:** segments posts into high, medium and low performance groups based on engagement metrics.
- Data is read from the warehouse, preprocessed (feature engineering, missing values), and the selected model is saved to make predictions on new data.

## Key Insights (from the dashboards)
- Reels have the highest average engagement rate, followed by Videos; Photos and Carousels perform moderately.
- Technology, Photography and Food lead in total engagement.
- Engagement is spread almost evenly across traffic sources (Reels Feed, Home Feed, Profile, Hashtags, Explore, External), so performance does not depend on one channel.
- A small number of posts generate a large share of engagement and are linked to higher follower gains.

## Recommendations
Prioritize Reels and Videos, keep investing in the top categories, align posting times with high-engagement periods, and keep a balanced presence across discovery channels.

## Skills Demonstrated
ETL design, data cleaning and validation, dimensional modeling (fact and dimension tables), SQL/MySQL, Power BI (ROLAP, dashboards), regression, clustering.

