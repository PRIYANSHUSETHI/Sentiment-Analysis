
# 📊 LinkedIn Review Sentiment Analysis using Python

Analyze user reviews from the LinkedIn app to uncover patterns in sentiment, detect possible fake reviews, and explore the relationship between textual reviews and numerical ratings.

---

## 🚀 Project Overview

This project applies advanced **Natural Language Processing (NLP)** and **Machine Learning (ML)** techniques to analyze LinkedIn app reviews. It explores sentiment trends, validates consistency between ratings and review text, compares sentiment models, and flags potentially fake reviews—using only two core attributes: `Review` and `Rating`.

---

## 🧰 Libraries Used

| Library | Purpose |
|--------|---------|
| `pandas` | Data loading, manipulation |
| `matplotlib.pyplot` & `seaborn` | Data visualization |
| `textblob` | Sentiment analysis (polarity) |
| `vaderSentiment` | Social media sentiment analysis |
| `wordcloud` | Word cloud generation |
| `sklearn` | Machine learning: model training, evaluation |
| `numpy` | Numerical computations |

---

## 🧪 Core Methodologies

### 🔹 Natural Language Processing (NLP)
- **Sentiment Analysis** using:
  - `TextBlob`: Rule-based polarity detection
  - `VADER`: Lexicon-based model for social text
- **Review Length & Word Count** extraction
- **Word Cloud Generation** for Positive, Negative, and Neutral sentiments

### 🔹 Exploratory Data Analysis (EDA)
- Distribution analysis:
  - Ratings
  - Review lengths
  - Word counts
  - Sentiment distribution per rating
- Sentiment vs. Rating **agreement evaluation**

### 🔹 Machine Learning
- **Feature Engineering**:
  - Review length
  - Word count
  - Rating
- **Fake Review Detection** using:
  - Heuristic rules
  - Logistic Regression classifier
  - Classification report
  - Confusion matrix

---

## 🔧 Functionalities and Custom Functions

### ✅ `textblob_sentiment_analysis(review)`
- Analyzes sentiment polarity using `TextBlob`
- Classifies sentiment as **Positive**, **Negative**, or **Neutral**

### ✅ `get_vader_sentiment(review)`
- Uses `VADER` sentiment intensity analyzer
- Classifies based on compound score thresholds

### ✅ `sentiment_rating_agreement(row)`
- Logic-based function to assess whether the **sentiment** of a review agrees with its **rating**
- Returns **"Agree"** or **"Disagree"**

### ✅ `generate_word_cloud(sentiment)`
- Generates a WordCloud for reviews belonging to a particular sentiment class

---

## 📊 Visualizations Included

| Chart | Description |
|-------|-------------|
| Bar Plot | Distribution of Ratings |
| Histogram + KDE | Review Length Distribution |
| Bar Plot | Sentiment Counts |
| Count Plot (Hue=Sentiment) | Sentiment vs Rating |
| Word Clouds | Separate for Positive, Negative, and Neutral |
| Agreement Plot | Sentiment vs Rating Agreement |
| Boxplot | Word Count vs Rating |
| Barplot | Avg Review Length by Rating |
| Heatmap | TextBlob vs VADER sentiment comparison |
| Confusion Matrix | Logistic Regression Fake Review Classifier |

---

## 💡 Insights Uncovered

- **Text sentiment and ratings mostly align**, but mismatches can expose anomalies.
- Short, 5-star reviews with overly positive sentiment may indicate **fake reviews**.
- **TextBlob vs VADER**: Generally agree, but differences in borderline or neutral cases.
- **Word clouds** highlight emotionally charged words linked to sentiment classes.

---

## 🛠️ How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/linkedin-review-analysis.git
cd linkedin-review-analysis
```

### 2. Install Required Libraries
```bash
pip install pandas matplotlib seaborn textblob vaderSentiment scikit-learn wordcloud
```

### 3. Run the Script
```bash
python sentiment_analysis_using_python.py
```

Make sure `linkedin-reviews.csv` is in the same directory.

---

## 🌱 Future Enhancements

- 💻 Build an **interactive dashboard** using Streamlit
- 🤖 Integrate **BERT** for state-of-the-art sentiment classification
- 🧠 Add **emotion detection** using `text2emotion` or `nrclex`
- 📝 Generate **automated PDF reports** from analysis
- 🌐 Make it a **web app** to analyze reviews on-the-fly
