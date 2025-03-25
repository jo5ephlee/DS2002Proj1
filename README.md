
# DS2002 Data Project 1
Joseph Lee and Nathan Kim
## Project Overview

This project demonstrates an ETL (Extract, Transform, Load) pipeline that manipulates data from two distinct sources:
- **Remote Data:** Fetched from the Spotify API (using Spotipy) to retrieve track information.
- **Local Data:** Loaded from a CSV or JSON file containing Spotify-related data.

The pipeline merges these two datasets, performs data transformation and analysis, and stores the final transformed data in a SQL database. It also supports file format conversion by allowing the output to be saved as a CSV or JSON file which the user can choose.

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

## Instructions

### Running in Google Colab

1. Open a new Google Colab notebook.
2. Upload your local data file (e.g., `spotify_2023.csv` or a JSON file) to the Colab environment.
3. If necessary, install Spotipy by running:
   ```python
   !pip install spotipy
