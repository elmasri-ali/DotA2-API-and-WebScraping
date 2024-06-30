# DotA2 Data Extractio-API-and-WebScraping

## Overview
This project focuses on analyzing DotA 2 match data to derive meaningful insights related to gaming performance. The analysis includes data extraction, cleaning, and visualization of match data from various sources such as CSV files, JSON files, API calls, and web scraping.

## Data Sources
1. **CSV File**: Extracted from Opendota.com, includes game details for Team Spirit, the international winning team of the past two years.
2. **JSON File**: Extracted from Opendota.com, includes hero roles.
3. **API Calls**: Extract detailed game information based on Match IDs, encompassing over 1500 games played by Team Spirit and approximately 800 personal games.
4. **Website Table**: Data from https://www.unitstatistics.com/dota2/ provides a breakdown of each hero’s base characteristics.

## Project Objectives
- Link heroes' attributes and roles with gameplay details.
- Clean, drop, and merge data to create a comprehensive dataset.
- Add a column identifying player names based on account ID for comparative analysis.


## Setup Instructions
1. Clone the repository:
2. Install the required dependencies:
3. Set up your environment variables by renaming `.env.example` to `.env` and adding your API key.
4. 4. Review the OpenDota API documentation to understand the JSON format and dictionaries used:
- [OpenDota API Documentation](https://docs.opendota.com/)

## Milestones

### 1: Data Cleaning

#### Objective
Clean and format the raw data extracted from Opendota.com, including both CSV and JSON files, to prepare for further analysis and extraction.

#### Process
1. **Loading Data**: Load the raw CSV and JSON files.
2. **Cleaning CSV Data**:
- Standardize column headers.
- Map account IDs to playing positions.
- Convert Unix timestamps to human-readable dates.
- Identify and remove duplicate rows based on Match ID.
- Drop irrelevant columns.
3. **Cleaning JSON Data**: Extract relevant hero roles and attributes.

#### Usage
Run the Jupyter notebook `01_data_cleaning.ipynb` to perform data cleaning.

### 2: API Data Extraction

#### Objective
Extract detailed match data using the Opendota API based on Match IDs, fetching match details and preparing the data for analysis.

#### Process
1. **Setup**:
- Load environment variables for API key. MAKE SURE TO REPLACE THE FAKE KEY WITH YOUR OWND API KEY
- Define the base URL for API calls.
2. **Fetch Matches**:
- Use Match IDs to fetch detailed match data from the API.
- Handle API rate limits by introducing delays between requests.
3. **Explore JSON Data**:
- Analyze the structure and complexity of the fetched JSON data.
4. **Data Extraction**:
- Extract relevant columns from the nested JSON data.
- Transform and format the data for analysis.
5. **Data Validation**:
- Identify and handle missing values and outliers.

#### Usage
Run the Jupyter notebook `02_api_extraction.ipynb` to extract match data using the Opendota API.

### 3: Web Scraping

#### Objective
Scrape hero attributes data from the website https://www.unitstatistics.com/dota2/ to complement the data from the JSON file.

#### Process
1. **Setup**:
- Use BeautifulSoup and requests libraries for web scraping.
2. **Extract Table Data**:
- Locate the table containing hero attributes on the webpage.
- Extract headers and row data from the table.
3. **Data Cleaning**:
- Clean and standardize the extracted data.
- Merge with the existing JSON data.
4. **Save Data**:
- Save the cleaned and merged data to a CSV file.

#### Usage
Run the Jupyter notebook `03_web_scraping.ipynb` to perform web scraping.

### 4: Data Analysis:

#### Objective
Analyze the cleaned and merged dataset to derive meaningful insights related to DotA 2 Teams gameplay and performance metrics.

#### Usage
Run the Jupyter notebook `04_data_analysis.ipynb` to perform data analysis and generate insights.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
