## Netflix Content Strategy & Data Analysis

Exploratory data analysis of the Netflix catalogue (movies and TV shows) in Python. The project cleans a raw dataset of 7,789 titles and uses Seaborn to study how the catalogue is split by type, release year, country, genre, rating and duration.

## Tech Stack

Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## Dataset

- **File:** `8. Netflix Dataset.csv` (7,789 rows × 11 columns)
- **Source:** [Google Drive link](https://drive.google.com/file/d/1p630pDcSkbQp_WXig8PeEVevZtSo4GQK/view)
- **Columns:** `Show_Id`, `Category`, `Title`, `Director`, `Cast`, `Country`, `Release_Date`, `Rating`, `Duration`, `Type`, `Description`

## Data Cleaning

1. Removed 2 duplicate rows (7,789 → 7,787).
2. Filled missing `Director`, `Cast` and `Country` values with placeholders (`No Direction`, `No Cast`, `Country Unavailable`).
3. Dropped rows missing `Release_Date` or `Rating` (final: 7,770 rows).
4. Converted `Release_Date` (mixed formats) to datetime and extracted `Release_year`.
5. Split the data into separate movie and TV show DataFrames; for TV shows, converted the duration to an integer number of seasons.

## Analysis Performed

- Count of movies vs TV shows
- Year-wise release/addition trend by category
- Top 20 countries and top 20 genres
- Ratings distribution for movies and TV shows
- Movie duration distribution and TV show season distribution
- Null-value heatmap (before cleaning)

## Key Findings

- Movies make up about **69%** of the catalogue and TV shows about **31%**.
- About **67%** of TV shows have only one season.
- Content additions peaked in **2019** (2,153 titles) among the years in the data.
- The **United States** (~3,300 titles) and **India** (~990) have the most titles; the median movie runs about 98 minutes.
- **TV-MA** and **TV-14** are the most common ratings.
- **International Movies** and **Dramas** are the most common genres.

> Note: `Release_year` is derived from the `Release_Date` column, which records when a title was added to Netflix, not necessarily its original release year.

## How to Run

```bash
git clone https://github.com/nobitha24/<repo-name>.git
cd <repo-name>
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Netflix_Data_Analysis_with_python.ipynb
```

Place `8. Netflix Dataset.csv` in the same folder as the notebook before running it.

## Repository Structure

```
├── Netflix_Data_Analysis_with_python.ipynb   # cleaning + EDA
├── 8. Netflix Dataset.csv                    # dataset
└── README.md
```

## Author

**Kadiyala Sai Srinath** — B.Tech, Electrical Engineering, IIT (ISM) Dhanbad
[GitHub](https://github.com/nobitha24) · [LinkedIn](https://www.linkedin.com/in/srinath-kadiyala-5792b3289/)
