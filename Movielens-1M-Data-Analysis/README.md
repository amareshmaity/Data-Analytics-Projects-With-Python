# MovieLens 1M Data Analysis

<br/>

## 🚀 Project Overview

This project analyzes the MovieLens 1M dataset to uncover trends in user ratings, movie popularity, and demographic influences. Through data cleaning, automated profiling, exploratory analysis, and statistical testing, we aim to answer questions such as:

* Which users and movies drive the most engagement?

* How do rating patterns differ across genres, age groups, and genders?

* What temporal trends exist in rating behavior over time?

<br/>

## 📁 Repository Structure

```
Movielens-1M-Data-Analysis/
├── Datasets/                      # Original MovieLens `.dat` files
│   ├── ratings.dat
│   ├── users.dat
│   └── movies.dat
├── movielens_venv/                # Python virtual environment folder
├── Movielens_Analysis.ipynb       # Jupyter notebook for analysis
├── requirements.txt               # Python dependencies
└── README.md                      # Project overview & quick start

```
<br/>

## 🛠️ Setup

1. **Clone the repo**

   ```bash
   git clone https://github.com/<your-username>/movielens-1m-analysis.git
   cd movielens-1m-analysis
   ```

2. Create virtual environment **movielens_venv** and activate it

3. **Key Dependencies**
    * pandas — data manipulation and aggregation
    * numpy — numerical operations
    * matplotlib — plotting library
    * seaborn — statistical data visualization

4. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```
5. Run the **Movielens_Analysis.ipynb** notebook

<br/>

## About Dataset
### Overview
This dataset comprises over 1,000,209 anonymous ratings for nearly 3,900 movies collected from 6,040 MovieLens users who joined the community in 2000. Widely used in academic research on recommender systems, collaborative filtering, and information retrieval, the dataset captures a rich history of user behavior and movie preferences.

This contains 3 .dat files -

### 1. Ratings (`ratings.dat`)
- **Format:** `UserID::MovieID::Rating::Timestamp`
- **Details:** UserIDs (1–6040), MovieIDs (1–3952), whole-star ratings on a 5-star scale, and Unix epoch timestamps. Each user has rated at least 20 movies.

### 2. Users (`users.dat`)
- **Format:** `UserID::Gender::Age::Occupation::Zip-code`
- **Details:** Gender (`M`/`F`), age groups (e.g., "18-24", "25-34", etc.), and occupations encoded numerically.

### 3. Movies (`movies.dat`)
- **Format:** `MovieID::Title::Genres`
- **Details:** Titles include the release year (per IMDb). Genres are pipe-separated (e.g., Action, Comedy, Drama). Note that some IDs may be duplicates or test entries.

### License and Citation

- **Usage:** For research only. Redistribution or commercial use requires special permission.
- **Acknowledgment:** Publications using this dataset must cite:  
  *F. Maxwell Harper and Joseph A. Konstan. 2015. “The MovieLens Datasets: History and Context.” ACM Transactions on Interactive Intelligent Systems, 5(4), Article 19. [DOI:10.1145/2827872](http://dx.doi.org/10.1145/2827872).*

### Download the dataset
[Download](https://grouplens.org/datasets/movielens/1m/) it from grouplens website.

<br/>

## 📊 Analysis Steps

1. **Dataset Familiarization**

   * Load raw `.dat` files and inspect shapes.
   * Identify missing values and convert timestamps.

2. **Data Cleaning & Transformation**

   * Handle missing values.
   * One-hot encode genres.
   * Filter out low-activity users/movies.

3. **Automated Profiling**

   * Generate profiling reports with ydata‑profiling.
   * Summarize schema anomalies and distribution skews.

4. **Exploratory Data Analysis (EDA)**

   * Univariate (histograms, distributions).
   * Bivariate (boxplots, scatter plots).
   * Temporal patterns (time series, heatmaps).

5. **Popularity & Engagement Insights**

   * Identify top movies and users.
   * Analyze genre popularity and rating variance.

6. **Feature Assembly**

   * Compute per-movie and per-user metrics.
   * Build `analysis_table.parquet` for further testing.

7. **Statistical Testing**

   * T-tests and ANOVA on demographic groups.
   * Correlation analysis with heatmaps.

8. **Reporting & Visualization**

   * Export key figures under `reports/figures/`.
   * Draft `reports/executive_summary.md` with insights and recommendations.

<br/>

## 📄 License

This project is open source and available under the [MIT License](LICENSE).



