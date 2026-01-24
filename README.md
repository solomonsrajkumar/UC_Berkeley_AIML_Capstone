# Capstone Project: ChatGPT vs. Google - Impact of Generative AI on Traditional Search

## Research Question
As generative AI platforms like ChatGPT rapidly gain adoption, are users beginning to shift away from traditional search engines like Google — and if so, under what circumstances?

This project investigates usage trends, query types, and user demographics to evaluate whether tools like GPT are replacing Google for specific informational or creative tasks.

## Data Sources
- Google Trends data on “ChatGPT,” “Google,” and “Bard” over time
- Synthetic survey data on user preferences and behavior

## Techniques Used
- Exploratory Data Analysis (EDA)
- Data Visualization (seaborn, matplotlib)
- Time-Series Analysis & Changepoint Detection
- Baseline ML Classification Model (Logistic Regression)
- Clustering for user segmentation

## Visualizations

### Google Trends Over Time
![Google Trends Over Time](images/trends_over_time.png)

### Query Type Distribution
![Query Type Distribution](images/query_type_distribution.png)

### Platform Preference by Age
![Platform Preference by Age](images/platform_preference_by_age.png)

## Repository Structure
```
Capstone_GPT_vs_Search/
│
├── data/
│   ├── google_trends_data.csv
│   └── synthetic_survey_data.csv
│
├── images/
│   ├── trends_over_time.png
│   ├── query_type_distribution.png
│   └── platform_preference_by_age.png
│
├── notebooks/
│   ├── eda.ipynb
│   └── baseline_model.ipynb
│
└── README.md
```

## Key Findings (To Be Expanded in Final Report)
- Initial trend data shows a significant spike in "ChatGPT" interest after Nov 2022, with continued high volume in 2023–2024.
- Synthetic data shows younger mobile users favor GPT platforms for creative and factual tasks.
- Classification model predicts GPT preference with decent accuracy based on age and query type.
