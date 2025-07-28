# Sentiment Insight Analysis — Reddit Comments EDA

An in-depth **Exploratory Data Analysis (EDA)** project focused on analyzing **Reddit comment sentiments** through statistical insights, text patterns, and visualization. TThis project conducts an exploratory data analysis (EDA) on a dataset of Reddit comments labeled with sentiment categories: negative (-1), neutral (0), and positive (1). The analysis focuses on understanding sentiment distribution, exploring text features such as word counts, stop words, punctuation, and n-grams, and visualizing these insights through various plots. The project lays the groundwork for advanced sentiment analysis and modeling by providing a clean, preprocessed dataset and detailed insights into comment characteristics.

---

## 🔍 Project Overview

This project performs a **sentiment insight analysis** on a dataset containing Reddit comments. Each comment is labeled as:

- **-1** → Negative  
- **0** → Neutral  
- **1** → Positive

We leverage **EDA, NLP techniques, and visual storytelling** to understand the language patterns and distribution of sentiments across the dataset.

---

## 🎯 Objectives

- Load and inspect the Reddit sentiment dataset.
- Clean and explore text-based data.
- Visualize linguistic metrics such as word count, stopwords, punctuation, and n-grams.
- Understand sentiment-based distributions and patterns.
- Lay the groundwork for future modeling and classification.

---

## 🗂 Dataset Details

- 📁 Source: [Reddit Sentiment Dataset](https://raw.githubusercontent.com/Himanshu-1703/reddit-sentiment-analysis/refs/heads/main/data/reddit.csv)
- 📊 Size: **37,249 rows × 2 columns**
- Columns:
  - `clean_comment`: The comment text (some missing).
  - `category`: Sentiment label (-1, 0, 1)

---

## ⚙️ EDA & Key Analysis Performed

### 📌 General Structure & Stats:
- Loaded and previewed first 10 rows
- Dataset shape: `(37,249, 2)`
- Found `100` missing values in `clean_comment`
- Sentiment Distribution:
  - Slightly skewed toward **positive and neutral**
  - Mean: `0.202771`
  - Std Dev: `0.778515`

---

### 📊 Visual Explorations:

#### 🧱 Distributions:
- **Sentiment Category Distribution** (CountPlot)
- **Word Count Distribution** (Histogram)
- **Word Count KDE by Category**
- **Boxplots of Word Count Per Comment**
- **Boxplots and Stripplots by Sentiment**
- **Median Word Count per Category (Bar Plot)**

#### 🛑 Stop Words Analysis:
- Created `num_stop_words` column
- Distribution of stop words overall & per category
- Top 25 most common stopwords (Bar Plot)

#### ✍️ Textual Characteristics:
- Created `num_punctuation_chars` column
- Calculated `num_characters` in each comment
- Top frequent words overall
- Stacked bar chart for top frequent words across sentiments

#### 🔤 N-Gram Analysis:
- Combined all comments into a large string
- Extracted and visualized:
  - Top 25 **bigrams**
  - Top 25 **trigrams**

---

### 🧼 Text Preprocessing Steps:
- Removed non-English characters
- Lemmatized comments (stored in `clean_comment_no_stopwords`)

---

## 🧠 Key Insights

- **Most comments are neutral or slightly positive**, which may impact model bias.
- **Stopwords and word count patterns differ across sentiment categories.**
- **Punctuation and character count** provides clues on intensity or tone.
- Frequent n-grams and keywords can help build sentiment-based features for classification models.

---

## 📌 Limitations

- Visualizations are limited to EDA only (no modeling yet).
- `clean_comment` column contains 100 missing values, not handled yet.
- No class balancing or advanced feature engineering in this stage.

---
## 📌 License

This project is licensed under the MIT License - see the LICENSE file for detail
