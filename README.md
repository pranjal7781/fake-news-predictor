# Fake News Predictor - By Pranjal Saxena

---

## 📁 Dataset & Model Files

To keep the repository lightweight, the dataset and trained model files are not included here. You can download them from the following links:

### 📦 Dataset
- [Download `dataset_fake.csv`](https://drive.google.com/file/d/1TixgK-_oSp3Gk61OQLJXnLRNcH5LqZ9y/view?usp=drive_link)

- [Download `dataset_true.csv`](https://drive.google.com/file/d/1DV6TkJA4uOGEluNBHedQDx0tieZ_HIlw/view?usp=drive_link)

Place them in a folder named `data/`.


### 🤖 Model Files
- [Download `fake_news_model.pkl`](https://drive.google.com/file/d/1cRFs3CsSPgtbI2hkohLee6sLt9Lu0IxT/view?usp=drive_link)

- [Download `tfidf_vectorizer.pkl`](https://drive.google.com/file/d/1XL4VGVe26aQSE4qNXnhPm27CfGDOzhk8/view?usp=drive_link)

Place them in a folder named `models/`.

---

## **Inspiration**

When brainstorming a creative AI project to address a common issue,I struck by the prevalence of misinformation in today’s world. From sensationalized news on platforms like TikTok to misleading articles circulating online, fake news is produced and shared at an alarming rate. Recognizing how easily people can fall for and spread such information, I inspired to develop a simple yet powerful tool. Our goal was to empower users to evaluate the credibility of articles quickly and effectively, equipping them with the means to combat fake news and promote informed decision-making.

---
## **What it does**

Fake News Predictor is a simple yet powerful tool designed to help users analyze the credibility of news articles. Users can paste any article into the platform and instantly receive a classification of whether the news is **True** or **False**, alongside a confidence score represented as a percentage. This confidence score allows users to gauge how certain the AI is in its prediction, with higher percentages reflecting greater certainty. 

To provide further insights, Fake News Predictor also analyzes the article for bias using polarity and subjectivity scores:
- **Polarity** measures the sentiment of the text, ranging from -1 (negative) to 1 (positive), helping users understand the tone of the article.
- **Subjectivity** evaluates how opinion-based the article is, ranging from 0 (completely objective) to 1 (highly subjective), enabling users to distinguish between factual reporting and personal opinions.

Together, these metrics empower users to critically assess the tone and bias of the content they’re consuming. If a user disagrees with the AI’s classification, they can submit feedback directly within the platform. This feedback is stored in a database, helping refine and improve the system over time.

## **How I built it**

To create Fake News Predictor, I began by sourcing and preprocessing a large dataset of fake and real news articles. Using **TF-IDF Vectorization**, I analyzed word frequencies and patterns, enabling our AI model to identify common traits in fake news, such as sensational language or repetitive phrases.

I trained and evaluated three machine learning models:
- Logistic Regression
- Random Forest
- XGBoost

I selected the most accurate model, which achieved a **96% success rate**.

The backend was developed using **Flask**, which also processes bias analysis and feedback collection. For additional insights, I implemented **TextBlob** to provide polarity and subjectivity scores to detect tone and bias in articles.

User feedback is stored in a **SQLite** database, creating a system that can learn and improve over time. To ensure a user-friendly experience, I designed the interface in **Figma**, and developed it using **HTML and CSS**.

## **Challenges I ran into**

There were a lot of new frameworks I learned about during this project, allowing us to gain valuable experience. Although it was time-consuming, learning **scikit-learn** and training machine learning models (including logistic regression, random forest, and XGBoost) was exciting.

Initially, our AI model had only **50% accuracy**, and improving it was a tedious process. I had to research and implement different data processing techniques to train the AI more effectively, eventually achieving **96% accuracy**.

Additionally, none of us had experience with **SQLite** or any other database engine, so learning how to use it from scratch to store user feedback was a significant challenge.

## **Accomplishments that I proud of**

- Successfully training a machine learning model to detect fake news with **96% accuracy**.
- Integrating multiple features—bias detection, sentiment analysis, and user feedback—into one cohesive system.
- Building a working **feedback loop** using SQLite, despite no prior database experience.

## **What I learned**

- Training machine learning models using **scikit-learn**.
- Text processing with **TF-IDF Vectorization**.
- Implementing **sentiment and bias analysis** with **TextBlob**.
- Storing and managing data using **SQLite**.
- Creating a clean, responsive user interface with **HTML/CSS**.

## **What’s Next for Fake News Predictor**

- **Image processing**: Allow users to upload screenshots of articles or posts for analysis.
- **PDF scanning**: Enable full-document uploads for misinformation detection.
- **Related articles**: Suggest credible articles on the same topic when fake news is detected, promoting informed decision-making.

