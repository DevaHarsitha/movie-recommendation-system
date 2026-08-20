# CineVault — Movie Recommendation System

> A content-based movie recommendation web application built with Python, Flask, Machine Learning, and MongoDB.

**Live Demo:** https://movie-recommendation-system-tjad.onrender.com/
**Source Code:** https://github.com/DevaHarsitha/movie-recommendation-system

---

## Overview

CineVault is a web-based movie recommendation system designed to help users discover movies based on their interests.

The system uses a content-based filtering approach that analyzes movie metadata such as genres and cast. These features are transformed using TF-IDF vectorization and similar movies are identified using K-Nearest Neighbors with cosine distance.

The application also provides user authentication, movie search, search history, watchlist management, and trending movie discovery.

---

## Features

* Content-based movie recommendations
* Movie search by title, genre, and cast
* User registration and login
* Password hashing and session-based authentication
* Personal watchlist management
* Search history tracking
* Trending movie discovery
* REST API endpoints for application functionality
* Responsive web interface

---

## Recommendation System

CineVault uses a content-based filtering approach to recommend movies with similar characteristics.

### Recommendation Pipeline

Movie Dataset
      |
      v
Data Preprocessing
      |
      v
Extract Movie Features
(Genres + Cast)
      |
      v
TF-IDF Vectorization
      |
      v
Feature Weighting
      |
      v
Combined Feature Matrix
      |
      v
KNN Model
(Cosine Distance)
      |
      v
Similarity Ranking
      |
      v
Recommended Movies


### How It Works

1. Movie genres and cast information are extracted from the dataset.
2. The textual features are converted into numerical representations using TF-IDF.
3. Genre features are given higher importance than cast features.
4. The weighted feature representations are combined.
5. A KNN model calculates the nearest movies using cosine distance.
6. The most similar movies are returned as recommendations.

---

## Technology Stack

| Category         | Technologies                    |
| ---------------- | ------------------------------- |
| Frontend         | HTML5, CSS3, JavaScript, Jinja2 |
| Backend          | Python, Flask                   |
| Machine Learning | Scikit-learn, TF-IDF, KNN       |
| Data Processing  | Pandas, NumPy, SciPy            |
| Database         | MongoDB, PyMongo                |
| Authentication   | Flask Sessions, Werkzeug        |
| Deployment       | Render, Gunicorn                |

---

## Project Structure

movie-recommendation-system/
│
├── data/
│   └── movies.csv
│
├── static/
│   ├── posters/
│   └── style.css
│
├── templates/
│   ├── history.html
│   ├── index.html
│   ├── login.html
│   ├── recommend.html
│   ├── register.html
│   └── results.html
│
├── app.py
├── requirements.txt
├── Procfile
├── .gitignore
└── README.md

---

## API Endpoints

| Endpoint                | Method | Description                       |
| ----------------------- | ------ | --------------------------------- |
| `/api/history`          | GET    | Retrieve user search history      |
| `/api/history/remove`   | POST   | Remove a search entry             |
| `/api/history/clear`    | POST   | Clear search history              |
| `/api/watchlist`        | GET    | Retrieve user's watchlist         |
| `/api/watchlist/add`    | POST   | Add a movie to the watchlist      |
| `/api/watchlist/remove` | POST   | Remove a movie from the watchlist |
| `/api/watchlist/status` | GET    | Check watchlist status            |
| `/api/trending`         | GET    | Retrieve trending movies          |

---

## Getting Started

### Prerequisites

* Python 3.9+
* Git
* MongoDB

### Create a Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

Create a `.env` file or configure environment variables for the application.

```env
MONGO_URI=your_mongodb_connection_string
SECRET_KEY=your_secret_key
```

Do not commit database credentials, secret keys, API keys, or other sensitive information to GitHub.

### Run the Application

python app.py


The application will be available at:

http://127.0.0.1:5000


---

## Live Demo

**CineVault:**
https://movie-recommendation-system-tjad.onrender.com/

---

## Future Enhancements

* Collaborative filtering
* Hybrid recommendation system
* User ratings and reviews
* Personalized recommendations based on user behavior
* Movie trailers and additional metadata
* Advanced filtering and sorting
* Recommendation performance evaluation

---

## Author

### Deva Harsitha B V

Computer Science Engineering Student

**GitHub:** https://github.com/DevaHarsitha\

