# Capstone Project: ChatGPT vs. Google - Impact of Generative AI on Traditional Search

## Research Question
As generative AI platforms like ChatGPT rapidly gain adoption, are users beginning to shift away from traditional search engines like Google — and if so, under what circumstances?

This project investigates usage trends, query types, and user demographics to evaluate whether tools like GPT are replacing Google for specific informational or creative tasks.

[View Final Jupyter Notebook:](https://colab.research.google.com/github/solomonsrajkumar/UC_Berkeley_AIML_Capstone/blob/main/notebooks/GPT_vs_Google.ipynb)

## Data Sources
- Google Trends data on “ChatGPT,” “Google,” and “Bard” over time
- Synthetic data on user preferences and behavior

## Data Set
- platform: GPT, Google, Bard
- date, is_weekend
- queries_per_session
- Session breakdowns: query_fact, query_creative, query_coding, query_shopping
- Usage metrics: google_usage, gpt_usage
  
## Techniques Used
- Exploratory Data Analysis (EDA)
- Data Visualization (seaborn, matplotlib)
- Time-Series Analysis & Changepoint Detection
- Baseline ML Classification Model (Logistic Regression)
- Clustering for user segmentation

## Visualizations

### Google Trends Over Time
- Description: This line chart compares usage patterns of Google vs. GPT-based platforms over time.
- Insight: GPT usage shows an increasing trend, while Google usage remains stable or slightly declining.
  
![Google Trends Over Time](images/trends_over_time.png)

### Query Type Distribution
- Description: Visualizes how different types of queries (Fact, Creative, Coding, Shopping) evolved over time.
- Insight: Creative and Coding queries appear to be rising, suggesting GPT’s strength in generative use cases.

![Query Type Distribution](images/query_type_distribution.png)

### GPT Linear Forecast
- Description: A linear regression model forecasting GPT usage over time.
- Insight: Strong upward linear trend, indicating increasing adoption of generative AI.

![Query Type Distribution](images/gpt_linear_forecast.png)

### K-Means Elbow Plot
- Description: Determines the optimal number of user behavior clusters based on usage patterns and query mix.
- Insight: Elbow observed around K=3, supporting segmentation into three distinct behavior profiles.

![Query Type Distribution](images/elbow_plot.png)

### K-Means Clustering Analysis
- Description - To explore natural groupings in user behavior patterns, we applied K-Means clustering using three features:
   - google_usage
   - gpt_usage
   - query_creative
  - These represent usage volume of Google and GPT platforms, and the proportion of creative queries in a session.
- Insights from Clustering
  - The K=3 decision was guided by the elbow method to identify natural groupings in the dataset.
  - The clusters reveal distinct behavioral patterns among users:
   - Cluster 0 tends to represent users with high GPT usage and higher engagement in creative queries.
   -  Cluster 1 shows users with dominant Google usage, but limited GPT adoption.
   -  Cluster 2 might represent a hybrid group with moderate use of both platforms, possibly indicating an evolving transition or dual behavior.

- Visual Output
  - The Seaborn pairplot visualization helps depict how users are grouped across the three selected dimensions. Color coding by cluster reveals separation in the latent behavioral patterns.
  - This clustering helps identify user archetypes and could guide future personalization strategies or platform optimization.
 
![Query Type Distribution](images/K-Means_Clustering_Analysis.png)
 
### Google Trends (Search Volume)
- Description: Shows search interest for “ChatGPT,” “Google,” and “Bard” over the last 12 months.
- Insight: ChatGPT’s search interest surged after launch, eclipsing Bard and narrowing the gap with Google.

![Query Type Distribution](images/google_trends.png)


### Summary & Conclusions

- This project blends synthetic and real data to:
- Visualize the rise of generative AI over traditional search
- Detect usage shifts in query intent
- Classify temporal behaviors (weekend vs weekday)
- Cluster users into behavioral segments
- Align with real-world signals from Google Trends

## Repository Structure
```
Capstone_GPT_vs_Search/
│
├── data/
│   ├── google_trends_data.csv
│   └── 10_000-row_GPT_vs_Google_Dataset.csv
│
├── images/
│   ├── trends_over_time.png
│   ├── query_type_distribution.png
│   └── gpt_linear_forecast.png
│   └── elbow_plot.png
│   └── K-Means_Clustering_Analysis.png
│   └── google_trends.png
│
├── notebooks/
│   ├── GPT_vs_Google.ipynb
│
└── README.md
```

### Results Summary

## Key Findings:
- GPT usage is on a consistent rise, both synthetically and in real-world search data.
- Users shift from factual to more creative/coding tasks over time.
- Weekend usage patterns show distinct characteristics.
- Three behavioral segments emerged from clustering: Traditional searchers, Balanced users, and GPT-heavy power users.

## Limitations:
- Synthetic data used for user session metrics
- Google Trends reflects public interest, not direct usage
