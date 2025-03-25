
# DS2002 Data Project 1 – ETL Pipeline for Spotify Data
Joseph Lee and Nathan Kim
## Project Overview

This project demonstrates an ETL (Extract, Transform, Load) pipeline that manipulates data from two distinct sources:
- **Remote Data:** Fetched from the Spotify API (using Spotipy) to retrieve track information.
- **Local Data:** Loaded from a CSV or JSON file containing Spotify-related data.

The pipeline merges these two datasets, performs data transformation and analysis (including summary statistics, correlation analysis, and optional visualization), and stores the final transformed data in a SQLite database. It also supports file format conversion by allowing the output to be saved as a CSV or JSON file.

## Features

- **Data Ingestion:**
  - Fetches data from the Spotify API using Spotipy.
  - Loads local data from a CSV or JSON file.
- **Data Transformation:**
  - Merges data from the two sources on a common key (`track_name`).
  - Handles column modifications such as type conversion (e.g., converting `streams` to numeric) and missing value imputation.
- **Data Summarization & Analysis:**
  - Prints out data summaries (record counts, column counts, and sample data).
  - Outputs summary statistics and a correlation matrix for numeric columns.
  - Optionally generates a histogram for the "popularity" field.
- **Data Storage:**
  - Saves the transformed data to a SQLite database.
  - Provides additional output format options (CSV or JSON).
- **Error Handling:**
  - Implements try/except blocks to provide informative error messages during data ingestion, transformation, and storage.

## Setup and Installation

### Prerequisites

- **Python 3.x**  
- Required Python packages:
  - [spotipy](https://spotipy.readthedocs.io/en/2.19.0/)
  - [pandas](https://pandas.pydata.org/)
  - [matplotlib](https://matplotlib.org/)
  - [sqlite3](https://docs.python.org/3/library/sqlite3.html) (included in the Python standard library)

### Running in Google Colab

1. Open a new Google Colab notebook.
2. Upload your local data file (e.g., `spotify_2023.csv` or a JSON file) to the Colab environment.
3. If necessary, install Spotipy by running:
   ```python
   !pip install spotipy
