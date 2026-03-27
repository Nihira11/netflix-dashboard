# Netflix Content Analysis (Power BI)

An exploratory analysis of Netflix's content catalogue using Power BI to uncover trends in content production, genre distribution, audience ratings, and global availability across 9,000+ titles.

---

## Dashboard Preview

### Overview
![Overview](screenshots/dashboard_overview.png)
*The overview page shows Netflix's full catalogue split across Movies (71%) and TV Shows (29%) with genre rankings, rating distribution, a content growth trend peaking in 2019 and a global map of content origin.*

### Country Interaction
![Country](screenshots/dashboard_country_filter.png)
*Clicking a country on the map cross-filters all visuals, here showing how content mix, genre preferences and ratings shift dramatically by region.*

### Filtered on Movies
![Movies](screenshots/dashboard_movie_filter.png)
*Filtering to Movies only reveals a different genre landscape. International Movies drop out of top position, Dramas and Comedies dominate and the US skews heavily movie-focused at 74.57%.*

---

## Project Overview

What drives Netflix's content strategy? This project analyses Netflix's catalogue to explore how the platform has evolved over time, examining which content types, genres and regions dominate, and where interesting gaps or trends exist.

The analysis is built in Power BI and covers the full analytics workflow from raw data to interactive dashboard, designed to surface actionable insights about Netflix's global content decisions.

---

## Dataset

Source: [Netflix Movies and TV Shows Dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows)

The dataset contains information about movies and TV shows available on Netflix, including:

| Field | Description |
|---|---|
| show_id | Unique identifier per title |
| type | Movie or TV Show |
| title | Title name |
| director | Director(s) |
| cast | Main cast members |
| country | Country of production |
| date_added | Date added to Netflix |
| release_year | Original release year |
| rating | Audience rating (e.g. TV-MA, PG-13) |
| duration | Runtime (movies) or seasons (TV shows) |
| listed_in | Genre categories |
| description | Short synopsis |


Dataset file used in this project:

```
netflix_titles.csv
```

---

## Tools Used

**Power BI -** Dashboard design \& visualisation  
**Power Query -** Data cleaning \& transformation  
**DAX -** Calculated measures \& KPIs

---

## Project Workflow

This project follows a structured data analytics workflow:

**1. Data understanding**  
Explored dataset structure, key fields and data quality issues

**2. Data Cleaning (Power Query)**
- Converted `date_added` to proper date format
- Cleaned and standardised text fields (country, genre, etc.)
- Split multi-value columns (e.g., country) for better analysis
- Removed inconsistencies and invalid entries

**3. Data Modeling & DAX**  
Created measures to support KPI cards and summary visuals:  
- `Total Titles`
- `Total Movies`
- `Total TV Shows`
- `Peak Content Year`

**4. Exploratory Analysis**
Explored the dataset through visuals to identify the most useful questions the dashboard should answer, focusing on:  
- Overall platform size
- Movies vs TV Shows split
- Top genres and rating distribution
- Growth in content additions over time
- Top countries by content and geographic spread

**5. Dashboard Design**
- Built interactive dashboard with Netflix-style dark theme
- Used appropriate visuals (donut, bar charts, area chart, map)

**6. Interaction and Refinement**
- Enabled cross-filtering between visuals
- Tested filters (country, type) and refined layout for usability

---

## Dashboard Features

The Power BI dashboard provides insights into:

- **KPI Cards -** Total titles, movies, TV shows, and peak content year at a glance
- **Donut Chart -** Distribution of Movies vs TV Shows
- **Horizontal Bar Chart -** Top genres ranked by volume, filterable by content type
- **Area Chart —** Content growth over time split by Movies and TV Shows
- **World Map —** Geographic distribution of content origin with bubble sizing by volume
- **Rating Bar Chart —** Distribution of titles across audience rating categories
- **Country Bar Chart —** Top 10 countries with Movie/TV Show split percentages

### Interactivity

- Cross-filtering across all visuals - clicking any data point (country, genre, rating) filters the entire dashboard
- Content type filter to toggle between Movies, TV Shows, or both
- Dynamic KPI cards that update with every filter selection

---

## Key Insights

- Netflix content saw rapid growth post-2015, peaking in 2019 before declining
- Movies dominate the platform, contributing ~71\% of total content, but TV Shows are strong in regions like South Korea and Japan
- The United States has the highest content volume, followed by India, heavily movie-focused (~92\% ), and the UK
- Dramas and International content dominate the catalogue
- Most titles fall under TV-MA and TV-14 ratings, indicating a mature audience focus
- South Korea stands out as a TV Show–heavy market, reflecting strong regional series production

---

## Project Structure

```
netflix-content-analysis
├── README.md
├── netflix_titles.csv
├── netflix_dashboard.pbix
└── screenshots
    └── dashboard_country_filter.png
    └── dashboard_movie_filter.png
    └── dashboard_overview.png
    
```

---

## Future Improvements

- **Director and cast analysis —** Identify which creators and talent are most prolific on Netflix, and whether certain directors skew toward specific regions or genres
- **Year slicer for time-based filtering —** Allow users to explore how genre and country distributions shifted across different eras of Netflix's growth
- **Drill-through pages —** Enable clicking a country or genre to navigate to a dedicated detail page with deeper breakdowns
- **Duration analysis -** Compare average movie runtimes and TV Show season counts across genres and regions
- **Mobile layout —** Optimise the dashboard layout for Power BI mobile view
- **Annotations on growth chart —** Mark key Netflix milestones (e.g. international expansion, original content push) directly on the trend line for richer storytelling

---

## Author

Built as part of a Data Science \& Business Analytics portfolio
