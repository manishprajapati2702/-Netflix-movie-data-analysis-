# -Netflix-movie-data-analysis-

1. Objective
The primary goal of this project is to perform a comprehensive exploratory data analysis (EDA) on a Netflix movies dataset. The analysis aims to uncover patterns and trends related to movie releases, popularity, genre distribution, and audience ratings. The end objective is to clean, transform, and analyze the data to support data-driven insights about movies on Netflix.

2. Dataset Overview
Source: mymoviedb.csv
Initial Structure: 9 columns, 9,827 rows.

Columns:
Release_Date: Original release date (later converted to year).
Title: Movie title.
Overview: Short description (dropped during cleaning).
Popularity: Numeric score indicating popularity.
Vote_Count: Number of votes the movie received.
Vote_Average: Average user rating.
Original_Language: Language code (dropped).
Genre: Comma-separated list of genres (cleaned and exploded).
Poster_Url: Link to movie poster (dropped).

Data Quality
No missing or duplicate records after initial checks.
Well-structured for further EDA.


3. Data Cleaning and Preprocessing
3.1. Type Conversion
Release_Date is converted from string to datetime, then reduced to just the year to support trend analysis.

3.2. Column Pruning
Dropped columns: Overview, Original_Language, Poster_Url — justified as not contributing to the core analysis.

3.3. Outlier and Distribution Checks
Used describe() on numeric columns (Popularity, Vote_Count, Vote_Average) to identify outliers and general distribution.

3.4. Feature Engineering
Vote_Average Categorization:
Defined 4 bins for ratings using quartiles:
not_popular
below_avg
average
popluar (typo, should be popular)

4. Exploratory Data Analysis (EDA)
4.1. Dataset Structure (after cleaning)
Release_Year	Title	Popularity	Vote_Count	Vote_Average	Genre
2021	Spider-Man: No Way Home	5083.954	8940	popluar	Action
2021	Spider-Man: No Way Home	5083.954	8940	popluar	Adventure
...	...	...	...	...	...

4.2. Key Findings

Data Integrity: No missing values or duplicates after cleaning. Dataset is robust for analysis.
Year Distribution: Analysis-ready for time series (trend) plots, e.g., movies released per year.
Genre Distribution: With exploded genres, possible to analyze genre popularity, frequency, and co-occurrence.
Popularity and Ratings: Popularity has significant outliers (max > 5000 vs mean ~40).
Vote_Average is binned, allowing for bar plots or pie charts of movie quality distribution.
Vote Count: Ranges from 0 to over 31,000, indicating a few movies are extremely popular.

4.3. Data Preparation for Visualization
Data is now in a form that supports:
Line charts (e.g., movies per year)
Bar charts (e.g., genre counts, popular movies)
Heatmaps (e.g., genre vs year)
Boxplots (e.g., popularity/rating distributions)

5. Strengths
Comprehensive Cleaning:
Handles type conversion, deduplication, missing values, and irrelevant columns.
Clear Feature Engineering:
Thoughtful binning of ratings and transformation of genres for deep categorical analysis.
Reporting: Summarize visual findings in markdown cells for storytelling.
Automation: Modularize cleaning and analysis steps for use on future datasets.

8. Conclusion
The Netflix Movie Data Analysis project demonstrates best practices in exploratory data analysis, with effective data cleaning, transformation, and feature engineering. The dataset is well-prepared for in-depth visualization and statistical analysis, supporting a wide range of business and research questions about Netflix’s movie catalog. With further visualization and interpretation, this project can yield actionable insights into content trends, audience preferences, and platform strategy.

