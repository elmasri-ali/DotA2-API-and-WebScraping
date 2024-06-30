# DotA2-API-and-WebScraping

## Overview
This project focuses on analyzing DotA 2 match data to derive meaningful insights related to gaming performance. The analysis includes data extraction, cleaning, and visualization of match data from various sources such as CSV files, JSON files, API calls, and web scraping.

## Data Sources
1. **CSV File**: Extracted from Opendota.com, includes game details for Team Spirit, the international winning team of the past two years.
2. **JSON File**: Extracted from Opendota.com, includes hero roles.
3. **API Calls**: Extracted detailed game information based on Match IDs, encompassing over 1500 games played by Team Spirit and approximately 800 personal games.
4. **Website Table**: Data from https://www.unitstatistics.com/dota2/ provides a breakdown of each hero’s base characteristics.

## Project Objectives
- Link heroes' attributes and roles with gameplay details.
- Clean, drop, and merge data to create a comprehensive dataset.
- Add a column identifying player names based on account ID for comparative analysis.

## Repository Structure
DotA2-Analysis-Project
│
├── README.md
├── data
│ ├── raw
│ │ ├── Data Team Spirit.csv
│ │ ├── Heroes.json
│ │ └── additional_data.csv
│ ├── processed
│ │ └── TeamspiritCleaned.csv
│ └── external
│ └── web_scraped_heroes.csv
├── notebooks
│ ├── 01_data_cleaning.ipynb
│ ├── 02_api_extraction.ipynb
│ ├── 03_web_scraping.ipynb
│ └── 04_data_analysis.ipynb
├── scripts
│ ├── data_cleaning.py
│ ├── api_extraction.py
│ ├── web_scraping.py
│ └── data_analysis.py
├── .env.example
├── requirements.txt
└── LICENSE
