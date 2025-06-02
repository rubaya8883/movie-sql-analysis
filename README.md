# movie-sql-analysis
SQL &amp; Python analysis of movie dataset including ratings and box office collections
# 🎬 Movie SQL Analysis: Box Office & Ratings Insights 

This project explores and analyzes a movie dataset using both **Python (Pandas)** for data cleaning and **SQL** for data querying. The goal is to uncover trends and insights about box office collections, IMDb ratings, and other key attributes of movies.

---

## 📁 Files in This Project

- `imdb_data_cleaning.ipynb` – Data cleaning and preparation using Python & Pandas
- `sql_analysis.ipynb` – SQL-based querying and visualization
- `BoxOfficeCollections_cleaned.csv` – Cleaned dataset
- `IMDB_box_office.db` – SQLite database generated from the cleaned data
- `BoxOfficeCollections_raw.csv` – Original raw dataset (for reference only)

---

## 🧼 Step 1: Data Cleaning (Python & Pandas)

Key cleaning steps included:
- Understanding the whole dataset.
- Finding missing values for each columns.
- Checking duplicates and standardizing column names.
- Droping rows where more than 6 columns contains null values.
- Filling missing values with 'unknown' for director, cast and genre column.
- Replacing null values for time_minute column with 60 minutes.
- Analyzing missing values of votes, box_office_collection, rating, metascore column using descriptive statistics method.
- Handling missing values of votes, box_office_collection, rating, metascore column using median values by genre.

---

🧾 Dataset Column Descriptions (BoxOfficeCollections_cleaned.csv)

<details>
<summary>📄 <strong>Click to view dataset details and column descriptions</strong></summary>

## 🧾 Column Descriptions (`BoxOfficeCollections_cleaned.csv`)

| Column Name             | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `movie`                 | Title of the movie                                                          |
| `year`                  | Release year of the movie                                                   |
| `score`                 | Original critic score (e.g., Rotten Tomatoes or similar, on a 0–100 scale)  |
| `adjusted_score`        | Weighted or normalized version of `score`                                   |
| `director`              | Director of the movie                                                       |
| `cast`                  | Main cast members (comma-separated)                                         |
| `consensus`             | Brief plot summary or critic consensus                                      |
| `box_office_collection` | Total worldwide box office earnings in USD                                  |
| `imdb_genre`            | Primary genre listed on IMDb (e.g., Comedy, Action)                         |
| `imdb_rating`           | IMDb rating (scale: 0–10)                                                   |
| `metascore`             | Metacritic score (0–100)                                                    |
| `time_minute`           | Runtime of the movie in minutes                                             |
| `votes`                 | Total number of IMDb user votes                                             |

---

### 🧪 Sample Preview

| movie              | year | score | adjusted_score | imdb_rating | box_office_collection |
|--------------------|------|-------|----------------|-------------|------------------------|
| Hot Rod            | 2007 | 39    | 42.918         | 6.7         | 14,371,564             |
| Game Night         | 2018 | 85    | 99.838         | 6.9         | 117,378,084            |
| The First Wives... | 1996 | 49    | 53.174         | 6.4         | 181,489,203            |

</details>

---

## 🧠 Step 2: SQL Analysis

Using SQL queries in Python to explore:
- Top-rated movies by IMDb score
- Revenue trends across genres
- Count of movies per year
- Movies with low rating but high revenue
- Correlation patterns (e.g., rating vs. revenue)

---

## 📊 Visualizations

Bar charts and line graphs were created using `matplotlib` and `pandas` to visualize:
- Top 10 movies by IMDb rating
- Box office collection trends by genre
- Average rating per release year

---

## 🛠️ Tools & Technologies

- Python
- Pandas
- SQLite
- SQL (via 'sqlite3')
- Matplotlib
- Jupyter Notebook

---

## 💡 Key Learning & Purpose

The project was built as part of my portfolio to showcase:
- Data wrangling skills in Pandas
- Ability to build and query a SQL database
- Data storytelling using Python and SQL
- Preparing datasets for real-world analytics scenarios

---

## 📌 Future Work

- Expand to a multi-table relational project (e.g., including actors, directors)
- Add more complex joins, aggregations, and visualizations

---

## 📎 Dataset Credit

- [Kaggle - Box Office Collections Dataset](https://www.kaggle.com/datasets/anotherbadcode/boxofficecollections)

---
