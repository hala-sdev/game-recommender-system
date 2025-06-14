# 🎮 Game Recommender System

A machine learning-based recommendation engine that suggests Steam video games based on game descriptions, genres, categories, and user preferences.

## 📌 Project Overview

This project builds a **content-based recommendation system** using:
- Natural language processing on game descriptions.
- TF-IDF features for genres and categories.
- Word2Vec embeddings for semantic similarity.
- FAISS for fast similarity search.

It helps users discover similar games to the ones they already like.

---

## 📂 Dataset

- **Source:** Steam Game Dataset (CSV format)
- **Features used:**
  - `about_description` (preprocessed and embedded using Word2Vec)
  - `genres`, `categories` (vectorized using TF-IDF)
  - `overall_review_%`, `review_count`, platform support

---

## 🚀 How It Works

1. Loads and cleans the Steam game dataset.
2. Processes text data:
   - Removes stopwords and punctuation.
   - Tokenizes descriptions.
   - Trains a Word2Vec model on the `about_description` field.
3. Vectorizes:
   - Descriptions (Word2Vec + average embedding)
   - Genres and categories (TF-IDF)
4. Combines all vectors.
5. Builds a similarity index using **FAISS**.
6. Given a game title, returns top 10 similar games.

---

## 🧪 Example Output

```text
🎮 Recommendations for the game 'Danganronpa: Trigger Happy Havoc':
• Danganronpa 2: Goodbye Despair
• Zero Escape: The Nonary Games
• Phoenix Wright: Ace Attorney Trilogy
• Corpse Party
• Steins;Gate
• The House in Fata Morgana
• AI: The Somnium Files
• 999: Nine Hours, Nine Persons, Nine Doors
• Your Turn To Die -Death Game By Majority-
• Clannad
```

---

## 🛠️ Tools & Libraries Used

- Python 🐍
- Pandas & NumPy
- NLTK
- Gensim (Word2Vec)
- FAISS
- Scikit-learn
- SciPy

---

## 📄 License

This project is licensed under the MIT License.
