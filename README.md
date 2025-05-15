# 📊 e-GMAT Reviews Analysis

This project is focused on extracting insights from reviews of e-GMAT available on [GMAT Club](https://gmatclub.com/reviews/e-gmat-6) to identify user-praised features, key improvement areas, and trends over the last 4 years using AI and NLP tools.

---

## 📥 Data Collection

Due to site-level scraping restrictions on `gmatclub.com`, direct scraping using Python tools like `requests`, `BeautifulSoup`, or `Selenium` was blocked.

👉 To bypass this, the **Chrome Extension `Instant Data Scraper`** was used. This extension mimics user interaction to scrape HTML tables and dynamically loaded content effectively.

The reviews were scraped across multiple pages and manually exported into structured CSV format, which was then used for further processing.

---

## 🧾 Repository Files Overview

### 📁 Input Data

- `gmatclub.csv`  
  → Raw exported reviews from GMAT Club using Instant Data Scraper. Includes fields like `posting-date`, `review title`, and `review_body`.

---

### 📄 Processed Review Text Files

Each `feature_X_reviews.txt` contains user review snippets specifically related to a praised or requested feature.

- `feature_1_reviews.txt` → Reviews about **Scholaranium**  
- `feature_2_reviews.txt` → Reviews about **Quant Course**  
- `feature_3_reviews.txt` → Reviews about **Verbal Course**  
- `feature_4_reviews.txt` → Reviews about **Personalized Feedback and Strategy Support**  
- `feature_5_reviews.txt` → Reviews about **Application Feedback/Mocks & Dashboards**

- `feature_requests.txt` → Extracted reviews where users explicitly **requested improvements or new features**

---

### 📦 Output JSONs

- `praise_counts.json`  
  → Contains feature-level praise counts across all reviews (used for plotting praise distribution).

- `praise_examples.json`  
  → Sampled review examples (as JSON) per feature — helpful for evidence-based documentation.

---

### 📊 Visualizations

- `gpt_feature_trend.png`  
  → Shows **how praise frequency for key features evolved from 2020–2024**, generated using GPT tagging + matplotlib/seaborn.

---

### 🧠 Codebase

- `e_gmat_scrapping_and_visualizations_code.py`  
  → Main Python code for:
  - Loading and cleaning CSV data
  - Sentiment and keyword extraction
  - GPT-based classification of reviews into features
  - Praise count and trend analysis
  - Saving filtered reviews to TXT and JSON files
  - Generating visualizations

---

## 🧪 Use Cases

This repo supports:
- Feature praise analysis
- Improvement recommendations
- Time-based feature trend tracking
- Evidence-backed product suggestions

---

## 📌 Output Used in Report

- **Feature Recommendations (1–2 pages)** → Based on `feature_requests.txt`
- **Strengths Analysis (1–2 pages)** → Based on praise counts and `feature_X_reviews.txt`
- **Trends Over 4 Years** → Visualized in `gpt_feature_trend.png`
- **Examples for Support** → Taken from `praise_examples.json`

---

## 🔗 Author Notes

This repo was built as part of an assignment analyzing customer sentiment and feature effectiveness of e-GMAT using real-world reviews.

