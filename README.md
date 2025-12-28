# Spotify API for Data Engineering & Analysis

A mini-intermediate data engineering and analytics project that pulls Spotify playlist data, stores it in MySQL, analysis using Python , and extract as csv.

---

This project started as a  “To explore my playlists 🎧" and grew into a small, reusable pipeline. 
It demonstrates practical skills in data extraction, storage, and analysis, with room for future enhancements like dashboards and Airflow ETL pipelines.

---

## What This Project Does
- Reads playlist URLs from a text file
- Fetches track details using the Spotify API
- Loads tracks into a MySQL database
- Exports a clean CSV for analysis
- Using pandas for analysis.

---

## Tech Stack
- Python
- Spotipy (Spotify Web API wrapper)
- MySQL + SQLAlchemy
- Pandas

## ETL Architecture
Spotify API
   ->
Python (Spotipy)
   ->
Data Cleaning & Transformation
   ->
MySQL (Artists | Albums | Tracks)
   ↓->
Pandas
   ->
CSV / Analysis
