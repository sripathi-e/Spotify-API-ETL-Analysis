# Spotify API for Data Engineering Pipeline (ETL) & Analysis

A mini-intermediate data engineering pipeline (ETL) and analytics project that pulls Spotify playlist data, stores it in MySQL, analysis using Python , and extract as csv.

---

This project demonstrates an end-to-end data engineering pipeline that ingests music metadata from the Spotify Web API, 
processes and normalizes raw JSON data using Python, and loads it into a MySQL relational database following ETL.

---

## Data Pipeline Architecture

Spotify Web API  ->  Python (Spotipy)  ->  Data Extraction & Transformation  ->  MySQL (Relational Data Store)  ->  Pandas (Analytics)  ->  CSV


## What This Project Does
- Reads playlist URLs from a text file
- Fetches track details using the Spotify API
- Loads tracks into a MySQL database
- Exports a clean CSV for analysis
- Using pandas for analysis.

---

## Tech Stack
- Python
- Spotify Web API (Spotipy)
- MySQL + SQLAlchemy
- Pandas

## Data Modeling & Schema Design

Artists Table
- artist_id (Primary Key)
- artist_name
- popularity
- followers
- genres

Albums Table
- album_id (Primary Key)
- album_name
- artist_id (Foreign Key)
- release_date
- total_tracks
- album_type

Tracks Table
- track_id (Primary Key)
- track_name
- artist_id (Foreign Key)
- album_id (Foreign Key)
- duration_sec
- explicit
- popularity

## ETL Pipeline

### Extract
- Reads Spotify track URLs from a file.
- Fetches track, artist, and album metadata via API calls.
- Handles invalid URLs using regex validation.

### Transform
- Parses nested JSON responses.
- Performs schema mapping and normalization.
- Converts duration from milliseconds to minutes.
- Cleans and formats genre data.
- Ensures consistent data types before loading.

### Load
- Loads transformed data into MySQL tables.
- Uses idempotent inserts to prevent duplication.
- Commits data incrementally for reliability.

## After ETL completion:
Data is queried from MySQL using SQLAlchemy

Pandas is used for:
- Exploratory analysis
- Business metrics calculation
- Dataset validation

Curated datasets are exported as CSV files:
- artists.csv
- albums.csv
- tracks.csv

---

👤 Author

Sripathi.E
Aspiring Data Engineer.
