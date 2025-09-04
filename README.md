# News Article Classification 📰🤖

## 📌 Project Overview
This project focuses on **Natural Language Processing (NLP)** to build a machine learning model that automatically classifies news articles into predefined categories based on their headlines. The primary objective is to leverage text preprocessing techniques, feature extraction, and various classification algorithms to develop an accurate and efficient classifier for categorizing news content.

---

## 📂 Dataset
- **Source**: `News_Category_Dataset_v3.json`
- **Details**:
  - A collection of news headlines and their corresponding categories.
  - Features used: `headline` (input text) and `category` (target variable).
  - For this project, the analysis was focused on classifying articles into three main categories: **Sports, Politics, and Technology**.

---

## ⚙️ Text Preprocessing
Standard NLP cleaning techniques were applied to the raw headline text to prepare it for modeling:
- **Lowercasing**: Converted all text to lowercase to ensure uniformity.
- **Removing Punctuation**: Eliminated all punctuation marks.
- **Removing Stopwords**: Removed common English stopwords (e.g., "the", "a", "in") using the NLTK library to reduce noise.
- **Tokenization**: Broke down sentences into individual words or tokens.

---

## 🧑‍💻 Feature Engineering
- **TF-IDF Vectorization**: The cleaned text data was transformed into a numerical format using the **Term Frequency-Inverse Document Frequency (TF-IDF)** technique. This method converts text into a matrix of feature vectors, where each feature represents a word's importance to a specific document (headline) within the entire corpus.

---

## 🔀 Train-Test Split
- The dataset was divided into a training set and a testing set to evaluate model performance on unseen data.
- **Split Ratio**: 80% for Training and 20% for Testing.

---

## 🤖 Models Implemented
Three different classification algorithms were trained and evaluated:
- **Logistic Regression**
- **Multinomial Naive Bayes**
- **Linear Support Vector Machine (SVM)**

---

## 🏆 Model Performance
- **Best Model**: **Linear Support Vector Machine (SVM)** demonstrated the best performance among the tested models.

**Performance Metrics on Test Set (Linear SVM):**
- **Accuracy** → **~0.79**

The model showed well-balanced precision and recall across all three categories, indicating it is not significantly biased towards any single class.

---

## 🔑 Key Findings & Insights
- **Feature Importance**: An analysis of the Linear SVM model's coefficients revealed the most influential words (features) for each category.
- **Top Discriminative Terms**: Words like 'business', 'ceo', 'uber', and 'companies' were identified as highly significant predictors.
- This insight helps in understanding the key vocabulary that distinguishes one news category from another and confirms the model learned relevant patterns from the data.

---

## 🔧 Tools & Libraries Used
- **Python**
- **Pandas**: For data loading and manipulation.
- **NLTK (Natural Language Toolkit)**: For text preprocessing tasks like stopword removal.
- **Scikit-learn**: For implementing TF-IDF, train-test split, and machine learning models.
- **Matplotlib & Seaborn**: For data visualization.
