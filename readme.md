# Quickstart
1. Pull the GitHub repository by running:
    ```
    git clone https://github.com/Alan-Grech295/ics5110-news-analysis.git
    ```
2. Create a python virtual environment using python 3.13.
  > - If using Anaconda, run: 
  > ```cmd
  > conda create -n news-analysis python=3.13 -y
  > conda activate news-analysis
  > ```
3. Install Python modules. In the project, run:
    ```
    pip install -r requirements.txt
    ```

# Project Structure

```text
ics5110-news-analysis/
├── data/
│   ├── police_press_releases.csv
│   ├── local_news_articles.csv
│   ├── intermediate/
│   │   ├── local_news_articles.csv
│   │   ├── local_news_articles_exclusions.csv
│   │   ├── local_news_articles_llm_exclusions.csv
│   │   └── local_news_articles_llm_manual_exclusions.csv
│   └── original/
│       ├── local_news_articles.csv
│       └── police_press_releases.csv
└── 1_data_preparation.ipynb
```

## File Explanation
- `data/police_press_releases.csv` - The police press releases dataset, containing only valid articles. **This should be used for data extraction.**
- `data/local_news_articles.csv` - The local news articles dataset, containing only valid articles. **This should be used for data extraction.**
---
- `data/intermediate/local_news_articles.csv` - The news articles filtered using spaCy.
- `data/intermediate/local_news_articles_exclusions.csv` - The news articles excluded using spaCy.
- `data/intermediate/local_news_articles_llm_exclusions.csv` - The news articles excluded by the LLMs.
- `data/intermediate/local_news_articles_llm_manual_exclusions.csv` - The news articles excluded by the LLMs, then 
manually reviewed to keep any valid articles wrongly excluded.
---
- `data/original/local_news_articles.csv` - The original, unchanged local news articles dataset.
- `data/original/police_press_releases.csv` - The original, unchanged police press releases dataset.