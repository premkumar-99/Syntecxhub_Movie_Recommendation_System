# 🎬 Movie Recommendation System

**Syntecxhub — Machine Learning Task 4**

This project is a **content-based movie recommendation system** built using the **TMDB 5000 dataset**.
It uses **text metadata**, **vectorization**, and **cosine similarity** to recommend movies similar to a user-selected film.

---

## 🚀 Features

* Clean and structured movie metadata
* Extracted:

  * Genres
  * Keywords
  * Top 3 actors
  * Director
  * Plot overview
* Engineered a unified **tags vector**
* Vectorized movie text using **CountVectorizer (5000 features)**
* Calculated **cosine similarity** between all movies
* Fast recommendation function returning **Top 5 similar movies**
* Ready for deployment or API integration

---

## 🗂 Dataset

This project uses:

* `tmdb_5000_movies.csv`
* `tmdb_5000_credits.csv`

Dataset source (Kaggle):
[https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

Place the files inside:

```
/data/
```

---

## 📁 Project Structure

```
Syntecxhub_Movie_Recommendation_System/
│── data/
│   ├── tmdb_5000_movies.csv
│   ├── tmdb_5000_credits.csv
│
│── notebooks/
│   ├── movie_recommendation.ipynb
│
│── src/
│   ├── recommender.py
│
│── outputs/
│   ├── similarity_matrix.npy
│   ├── vectorizer.pkl
│
│── README.md
```

---

## 🧠 How It Works

### **1️⃣ Data Cleaning**

* Merged movie + credits file
* Parsed JSON-like columns
* Extracted director & top 3 cast members
* Cleaned overview text

### **2️⃣ Tags Creation**

Combined:

* Overview
* Genres
* Keywords
* Actors
* Director

into a single **tags** field.

### **3️⃣ Vectorization**

Applied:

```
CountVectorizer(max_features=5000, stop_words='english')
```

### **4️⃣ Similarity Matrix**

Used:

```
cosine_similarity(vectors)
```

### **5️⃣ Recommend Function**

Input: `"Avatar"`
Output: Top 5 similar movies.

---

## ▶️ How to Run

### **Option 1: Notebook**

1. Open `/notebooks/movie_recommendation.ipynb`
2. Run all cells
3. Try:

```python
recommend("Avatar")
```

### **Option 2: Script**

Run:

```bash
python src/recommender.py
```

---

## 📌 Sample Output

Example results for `"Avatar"`:

```
[ 'John Carter', 'Guardians of the Galaxy', 'The Matrix', 'Interstellar', 'Star Trek' ]
```

*(Output may vary based on preprocessing)*

---

## ⭐ Future Enhancements

* Add weighted hybrid filtering
* Deploy as a Flask API
* Build a Streamlit UI
* Add user-based collaborative filtering

---

## 🧑‍💻 Author

**Premkumar**
Machine Learning Intern — Syntecxhub

---

## 🔗 Connect

LinkedIn: [*Add your link here*](https://www.linkedin.com/posts/premkumar-a-39398a355_just-wrapped-upmachine-learning-task-4-activity-7402218482148425728-QWsk?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFiZiZ8B_FzrednhfowvJ0bks6rrUu1bLC0)

