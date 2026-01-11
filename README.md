# 🎬 Movie Recommender System

<p align="center">
  <img src="https://img.shields.io/badge/python-3.9+-blue.svg" alt="Python"/>
  <img src="https://img.shields.io/badge/FastAPI-backend-green.svg" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Streamlit-frontend-red.svg" alt="Streamlit"/>
  <img src="https://img.shields.io/badge/Machine%20Learning-TF--IDF-orange.svg" alt="TF-IDF"/>
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"/>
</p>

<p align="center">
  <strong>A modern full-stack movie recommendation system using content-based filtering and live movie data.</strong>
</p>

<p align="center">
  <a href="#-features">✨ Features</a> •
  <a href="#-architecture">🏗️ Architecture</a> •
  <a href="#-tech-stack">🛠️ Tech Stack</a> •
  <a href="#-quick-start">🚀 Quick Start</a> •
  <a href="#-deployment">🌐 Deployment</a>
</p>

---

## 🎯 Overview

This project is a **content-based movie recommender system** built with a **FastAPI backend** and **Streamlit frontend**.
It recommends movies based on semantic similarity using **TF-IDF vectorization**, combined with **genre-based filtering** for better relevance.

The application fetches **real-time movie posters, metadata, and descriptions** using the TMDB API and presents recommendations in a clean, modern UI.

---

## ✨ Key Features

### 🔍 Smart Search & Autocomplete

* Real-time movie name suggestions
* Helps users quickly find relevant titles
* Reduces spelling and discovery friction

### 🎯 Hybrid Recommendation Engine

* TF-IDF cosine similarity for content-based filtering
* Genre-based constraints to improve relevance
* Fast inference using precomputed vectors

### 🎥 Rich Movie Details

* Movie posters and backdrops
* Release date, genres, and overview
* Clean grid-based movie layout

### 🖥️ Modern Frontend

* Built with Streamlit
* Responsive layout and smooth user experience
* Designed for simplicity and speed

### 🌐 Live Movie Data

* Real-time movie metadata and images
* Powered by The Movie Database (TMDB) API

---

## 🏗️ Architecture

```
User (Streamlit UI)
        ↓
Search / Movie Selection
        ↓
FastAPI Backend
        ↓
TF-IDF Vector Similarity
        ↓
Genre-Based Filtering
        ↓
Top-N Recommendations
        ↓
TMDB API (Posters & Metadata)
        ↓
Rendered Results (Streamlit)
```

---

## 🛠️ Tech Stack

| Layer            | Technology           |
| ---------------- | -------------------- |
| Language         | Python 3.9+          |
| Backend          | FastAPI              |
| Frontend         | Streamlit            |
| Machine Learning | TF-IDF, Scikit-learn |
| Data Processing  | Pandas, NumPy        |
| External API     | TMDB API             |
| Deployment       | Heroku               |
| Model Storage    | Pickle               |

---

## 🚀 Quick Start

### Prerequisites

* Python 3.9+
* TMDB API key (free)

Get your API key from:
[https://www.themoviedb.org/settings/api](https://www.themoviedb.org/settings/api)

---

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd Movie_Recommended_System

# Create virtual environment
python -m venv .venv
source .venv/bin/activate      # Linux/Mac
.venv\Scripts\activate         # Windows

# Install dependencies
pip install -r requirements.txt
```

### Environment Variables

Create a `.env` file:

```
TMDB_API_KEY=your_api_key_here
```

---

## ▶️ Running the Application

### Start Backend (FastAPI)

```bash
uvicorn main:app --reload
```

Backend runs at:
[http://127.0.0.1:8000](http://127.0.0.1:8000)

---

### Start Frontend (Streamlit)

```bash
streamlit run app.py
```

Frontend runs at:
[http://localhost:8501](http://localhost:8501)

---

## 📁 Project Structure

```
Movie_Recommended_System/
├── app.py                  # Streamlit frontend
├── main.py                 # FastAPI backend
├── movies.ipynb            # Data preprocessing & model building
├── requirements.txt        # Dependencies
├── Procfile                # Deployment config
├── data/
│   └── movies_metadata.csv
└── models/
    ├── df.pkl
    ├── indices.pkl
    ├── tfidf_matrix.pkl
    └── tfidf.pkl
```

---

## 🔧 API Endpoints

| Method | Endpoint                     | Description               |
| ------ | ---------------------------- | ------------------------- |
| GET    | `/`                          | Health check              |
| GET    | `/movie/autocomplete?query=` | Autocomplete movie search |
| GET    | `/movie/search`              | Get movie recommendations |
| GET    | `/movie/{tmdb_id}`           | Fetch movie details       |

---

## 📊 How It Works

1. Movie metadata is cleaned and vectorized using TF-IDF
2. User selects or searches for a movie
3. Cosine similarity finds semantically similar movies
4. Genre filtering refines the recommendations
5. TMDB API enriches results with posters and metadata
6. Results are displayed in the Streamlit UI

---

## 🌐 Deployment

### Heroku Deployment

```bash
# Create app
heroku create your-app-name

# Set environment variable
heroku config:set TMDB_API_KEY=your_api_key_here

# Deploy
git push heroku main

# Scale dyno
heroku ps:scale web=1
```

---

## 🔮 Future Improvements

* Collaborative filtering integration
* User profiles and watch history
* Hybrid ML + deep learning recommendations
* Caching layer for faster API responses
* Improved ranking with popularity signals

---

## 🤝 Contributing

Contributions are welcome.
Feel free to open issues, suggest enhancements, or submit pull requests.

---

## 📄 License

MIT License © 2025 Vivek Kumar Gupta

---

## 🙏 Acknowledgments

* The Movie Database (TMDB) for movie data and images
* Kaggle TMDB movie metadata dataset

 Align it tightly with ML Engineer / Backend Engineer roles
