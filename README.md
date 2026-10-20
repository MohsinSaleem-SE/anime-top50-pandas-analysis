# Anime Top 50: Feature Extraction with Pandas

A beginner-friendly data analysis project that cleans a messy, scraped anime dataset and extracts new features from a single text column using **pandas**.

## About the Dataset

`anime.csv` contains the Top 50 anime by score, scraped from MyAnimeList. The `Title` column is a long text string that mixes several pieces of information:

```
Fullmetal Alchemist: BrotherhoodTV (64 eps)Apr 2009 - Jul 20103,218,472 membersManga StoreVolume 1€4.58Preview
```

## Features Extracted

| New Column | Description | Example |
|---|---|---|
| `Episodes` | Episode count from the `(xx eps)` part | `64` |
| `Time Range` | Airing period | `Apr 2009 - Jul 2010` |
| `Months Range` | Total months aired, inclusive | `16` |

## Analysis Performed

- Anime with the highest score
- Top 5 anime by score
- Anime with the highest episode count
- Top 5 anime by episode count
- Longest running anime

## Key Findings

- **Highest score:** Fullmetal Alchemist: Brotherhood (9.10)
- **Most episodes:** Ginga Eiyuu Densetsu (110 episodes)
- **Longest running:** Ginga Eiyuu Densetsu (111 months)

## Tech Stack

- Python 3
- pandas
- NumPy
- Jupyter Notebook

## Getting Started

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
pip install pandas numpy jupyter
jupyter notebook FeatureExtraction.ipynb
```

## Project Structure

```
├── anime.csv                # Raw dataset (Top 50 anime)
├── FeatureExtraction.ipynb  # Feature extraction and analysis
└── README.md
```

## Concepts Practiced

- Reading CSV files with `pd.read_csv()`
- Writing custom functions and applying them with `.apply()`
- String parsing with `find()`, `split()`, and slicing
- Type conversion with `astype()`
- Filtering with boolean masks, `nlargest()`, and `max()`

## Future Improvements

- Parse member counts into numeric values
- Clean the scraped text out of the `Title` column
- Add charts for score vs. episodes and score vs. duration
