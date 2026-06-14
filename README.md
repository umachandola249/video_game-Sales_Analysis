# video_game-Sales_Analysis
'An ETL pipeline and data analysis project built  in my first sem.'
# Global Video Game Market Analysis (ETL Pipeline)


## Project Overview
This project establishes an automated Python data ingestion, cleaning, and SQL analytics pipeline to analyze historical market patterns across **16,500+ global video game records**. Using regional and global sales matrices, this analysis uncovers how consumer entertainment software demand shifts across hardware generations, timelines, and industry production houses.

##  Tech Stack & Tools
* **Programming Language:** Python 3
* **Data Ingestion Framework:** KaggleHub API
* **Query Implementation:** SQL (via `pandasql` library)
* **Libraries:** Pandas, NumPy, Seaborn
* **Environment:** Google Colab 

##  The ETL Pipeline (Step-by-Step)

### 1. Extraction (Data Ingestion)
The raw dataset is dynamically downloaded directly from Kaggle via the `kagglehub` library. This ensures technical reproducibility and programmatic control over data ingestion without manual files or uploads.

### 2. Transformation (Data Hygiene & Cleaning)
* Filtered out incomplete historical records containing missing fields in publication timelines (`Year`) and market distribution labels (`Publisher`).
* Rectified decimal parsing issues by standardizing release timelines into clean, database-friendly integer values.
* Processed raw matrices into a fully normalized data asset ready for downstream analytics.

### 3. Loading & Custom SQL Analytical Views
Instead of basic filtering, custom SQL (`pandasql`) queries were written to extract aggregate corporate insights across three core business dimensions:
* **Platform Performance:** Evaluated total market sales grouped by gaming hardware platforms to isolate dominance lifecycles.
* **Timeline Metrics:** Aggregated historical revenue records sorted by release calendar years to map global software consumption trends over time.
* **Corporate Market Share:** Grouped global performance matrices by distribution publishers to identify top revenue-generating gaming entities.

## Key Analytical Insights
* **Platform Dominance:** Hardware distribution platforms dictate sales caps, with specific legacy systems holding highly concentrated historic market share.
* **Strategic Distribution:** A small segment of top-tier publishers represents an exponential percentage of total lifetime global software revenue.

##  Repository Structure
* `games.ipynb` -> Core Google Colab analytical script running Python and custom SQL queries.
* `cleaned_vgsales.csv` -> Output dataset prepared for downstream reporting.
* `README.md` -> Project documentation page.
*
