
# 🎬 OTT Platform Trends – EDA Project

![Netflix Banner](https://upload.wikimedia.org/wikipedia/commons/0/08/Netflix_2015_logo.svg)

## 📌 Project Overview
This project performs **Exploratory Data Analysis (EDA)** on a global OTT TV shows dataset to uncover patterns in content trends, viewer preferences, and platform growth.  
It is designed at an **intermediate** level, with clean visualizations and feature engineering for interview-ready storytelling.

The dataset used: `cleaned_tvshows_data.csv`.

---

## 🗂 Dataset Description
Each row represents a TV show with attributes like:
- **title** – Name of the show
- **type** – Content type (e.g., TV Show, Movie)
- **genre** – Show genre(s)
- **rating** – Age rating (e.g., TV-MA, TV-14, TV-PG)
- **seasons** – Number of seasons
- **release_year** – Year the show was released
- **added_date** – Date added to the platform
- **country** – Country of origin

---

## 🔍 EDA Steps Performed
### 1. Data Cleaning
- Removed duplicates at **show-level** (merged multiple genre rows per title)
- Converted date columns to `datetime`
- Filled missing values in key fields (rating, country, seasons)
- Dropped irrelevant or empty columns

### 2. Feature Engineering
- **content_age** – How old the show is in years
- **is_recent** – Whether the show was released in the last 5 years
- **added_year**, **added_month** – Extracted from `added_date` for trend analysis

### 3. Data Transformation
- Created **genre-exploded dataset** for per-genre analysis
- Aggregated counts for ratings, genres, countries, and release years

### 4. Visualizations
- **Content type distribution** (pie chart)
- **Top 15 ratings** (bar chart)
- **Top genres** (bar chart)
- **Seasons distribution** (histogram)
- **Releases per year** (line chart)
- **Additions per year** (line chart)
- **Top content-producing countries** (bar chart)

---

## 📊 Key Insights
- **Ratings Mix**: TV-MA (~43%), TV-14 (~27%), TV-PG (~12%) dominate.
- **Top Genres**: International TV Shows, TV Dramas, TV Comedies, Crime TV Shows, Kids’ TV.
- **Season Count**: Median = 1 (short-run shows dominate).
- **Geography**: US, UK, Japan, and South Korea lead content production.
- **Growth**: Significant acceleration in releases post-2015.

---

## 💡 Business Impact & Actionable Insights
- Focus investment on **international originals** in high-demand genres (Drama, Comedy, Crime).
- Experiment with **short-format series** (given dominance of 1-season shows).
- Strengthen **country-specific content hubs** in US, UK, Japan, and Korea.
- Maintain strong pipeline of **mature-audience content** (TV-MA, TV-14).

---

## 🛠 Tools & Libraries Used
- **Python**
- **Pandas** – Data cleaning & transformation
- **Matplotlib** / **Seaborn** – Data visualization
- **Jupyter Notebook** – Interactive analysis

---

## 📂 Repository Structure
```
├── cleaned_tvshows_data.csv            # Raw cleaned dataset
├── ott_show_level.csv                  # Show-level dataset after merging duplicates
├── ott_show_level_genre_exploded.csv   # Genre-exploded dataset
├── summary_type_counts.csv             # Summary of content type distribution
├── summary_rating_counts_top15.csv     # Top 15 ratings distribution
├── summary_top_genres.csv              # Top genres list
├── summary_top_countries.csv           # Top content-producing countries
├── README.md                           # Project documentation
└──
```
