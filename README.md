# 🎬 Movie Recommender System

A content-based movie recommendation system built with Python and machine learning. It analyzes movie metadata to recommend five similar movies based on a user's selected title. The project also includes a Streamlit application that displays movie recommendations and fetches posters using the TMDB API.

## ✨ Features

- **Content-Based Recommendations:** Recommends movies based on similarities in their metadata.
- **Text Feature Extraction:** Uses CountVectorizer to convert movie tags into numerical vectors.
- **Cosine Similarity:** Calculates similarity scores between movies to identify relevant recommendations.
- **Movie Poster Integration:** Fetches movie posters through The Movie Database (TMDB) API.
- **Interactive Web App:** Select a movie and view five recommendations through Streamlit.
- **Data Preprocessing:** Processes movie genres, keywords, cast members, and director information.

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Text Processing | CountVectorizer, NLTK PorterStemmer |
| Similarity Algorithm | Cosine Similarity |
| Web Application | Streamlit |
| API Integration | TMDB API, Requests |
| Data Storage | Pickle |
| Additional UI Prototype | HTML, CSS, JavaScript |

## 🧠 How It Works

1. **Data Loading:** Loads the TMDB 5000 Movies and Credits datasets and merges them using movie titles.
2. **Data Preprocessing:** Selects movie IDs, titles, overviews, genres, keywords, cast, and crew information. Missing values are removed.
3. **Feature Engineering:** Extracts genre names, keywords, the first three cast members, and director names.
4. **Tag Creation:** Combines genres, cast, directors, and keywords into a single text representation for each movie.
5. **Vectorization:** Uses CountVectorizer with a maximum of 5,000 features and English stop-word removal.
6. **Similarity Calculation:** Applies cosine similarity to compare the resulting movie vectors.
7. **Recommendation:** Sorts similarity scores and returns the five most similar movies, excluding the selected movie itself.
8. **Poster Retrieval:** Uses the TMDB API to retrieve poster images for recommended movies.

## 📂 Project Structure

```text
Movie-Recommender-System/
├── movie_recommender.ipynb
├── app.py
├── index.html
├── tmdb_5000_movies.csv
├── tmdb_5000_credits.csv
├── movie_dict.pkl
├── similarity.pkl
├── movies.pkl
├── style.css
├── js/
│   └── app.js
├── images/
├── .gitignore
└── README.md
```

*The structure is illustrative. Include only files and folders that actually exist in your repository. The Streamlit app requires `movie_dict.pkl` and `similarity.pkl`; the HTML prototype references additional CSS, JavaScript, and image assets.*

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Aashir-Ali27/Movie-Recommender-System.git
cd Movie-Recommender-System
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install streamlit pandas numpy scikit-learn requests nltk jupyter
```

### 4. Prepare the datasets

Place the following files in the project directory:

- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

### 5. Generate the model files

Open `movie_recommender.ipynb` in Jupyter Notebook and execute the preprocessing and model-generation cells.

The notebook generates:

- `movies.pkl`
- `movie_dict.pkl`
- `similarity.pkl`

Keep these generated files in the directory from which you run the application, unless you update the file paths in your code.

### 6. Configure the TMDB API

Configure your TMDB API key securely using an environment variable or Streamlit secrets. Do not publish private credentials in source code.

### 7. Run the application

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal to use the recommendation system.

## 📊 Dataset

The project uses the TMDB 5000 Movie Dataset, comprising movie metadata and credits information.

The data is used to extract movie attributes and construct text-based representations for similarity comparison.

## 🔮 Future Improvements

- Incorporate movie overviews into the recommendation tags.
- Apply stemming consistently during feature preprocessing.
- Improve error handling for movies that are not found.
- Add genre filtering, movie search, and watchlist functionality.
- Connect the HTML/CSS/JavaScript interface to the recommendation backend.
- Deploy the application online.
- Optimize similarity storage and loading for improved scalability.

## 👨‍💻 Author

**Aashir Ali Shaikh**

- GitHub: [Aashir-Ali27](https://github.com/Aashir-Ali27)
- LinkedIn: [Connect with me](https://www.linkedin.com/in/aashir-ali-b134a027a/)

---

If you find this project interesting, consider starring the repository!
