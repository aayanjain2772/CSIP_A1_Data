# 🗂️ Grant Data Scraping & Analysis Project

## 📌 Objective

The goal of this project is to extract, clean, and analyze structured and unstructured data related to grants from a given dataset. The dataset mimics scraped content from a foundation’s public-facing grant records, including grant titles, funding amounts, durations, descriptions, and thematic initiatives.

---

## 🛠️ Tools & Libraries Used

- **Pandas**: For data loading, cleaning, and manipulation
- **Matplotlib & Seaborn**: For data visualization
- **Scikit-learn (CountVectorizer)**: For basic natural language processing (word frequency analysis)

---

## 📁 Files Included

- `cleaned_grants_dataset.csv`: Cleaned and preprocessed structured dataset
- `grant_analysis.ipynb`: Jupyter notebook with full implementation of cleaning, EDA, and text analysis
- `README.md`: This file
- `summary_report.pdf` *(to be submitted separately)*

---

## 🧹 Data Cleaning & Processing

- **Missing Values**: Filled missing `Grant Status` with "Unknown" and dropped rows with missing critical fields (`Title`, `Description`).
- **Data Types**: Converted date columns to datetime format, and grant amounts to numeric.
- **Duplicates**: Removed exact duplicates across all fields.

---

## 📊 Structured Data Analysis

- **Grant Frequency by Initiative**: Counted the number of grants across different programmatic initiatives.
- **Grant Amount Distribution**: Visualized distribution to understand central tendencies and spread of funding.

---

## 🧠 Unstructured Data Processing (Descriptions)

- Used **`CountVectorizer`** from `scikit-learn` with English stopwords to:
  - Tokenize and vectorize the grant descriptions.
  - Generate word frequency tables to identify the most commonly used keywords and themes.
- Presented results using bar plots of top 20 most frequent terms.

---

## 🧪 Key Observations

- Majority of the grants fall under a small number of high-focus initiatives.
- Grant amounts vary widely, with some mega grants exceeding $1M.
- Common themes in descriptions include keywords like “support,” “climate,” “development,” and “resilience,” indicating funding priorities.

---

## ⚠️ Notes

- The dataset used was pre-downloaded and structured for educational purposes.
- No actual web scraping was performed as part of this implementation due to restrictions.
- `nltk` and `wordcloud` libraries were excluded for minimal dependency.

---

## ✅ Future Improvements

- Automate the scraping pipeline using BeautifulSoup or Scrapy.
- Enhance NLP using `spaCy` or `BERTopic` for topic modeling.
- Export results
