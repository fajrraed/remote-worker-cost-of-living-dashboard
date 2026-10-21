### Remote Worker Cost-of-Living Crisis Dashboard

###  Project Overview

Finding the perfect city to work remotely is a major challenge. Remote employees often struggle to find global destinations that balance a low cost of living with a high quality of life and reliable internet infrastructure. 

This project solves that problem by building a complete data pipeline. It cleans raw time-series data using **Python**, evaluates city metrics, and presents an interactive **Power BI Dashboard** that allows users to filter cities based on their budget and infrastructure needs. 

###  Tech Stack & Tools

* **Data Engineering & Cleaning:** Python, Pandas, Jupyter Notebook
* **Business Intelligence & Visualization:** Power BI Desktop
* **Data Source:** Kaggle Global City Indices Dataset

###  Data Pipeline & Workflow

### 1. Data Cleaning (Jupyter Notebook)

The raw dataset was messy and contained duplicate tracking data over multiple years. The Python pipeline performed the following optimization steps: 

* **Time-Series Deduplication:** Sorted records by survey dates and retained only the most recent entry for each city.
* **Missing Value Handling:** Removed rows missing critical metrics like internet speed, as reliable connectivity is a dealbreaker for remote work.
* **Feature Dropping:** Cleaned up unused data blocks and empty analyst notes to minimize file size and maximize Power BI performance.
* **Data Export:** Saved the polished data into a clean cleaned_nomad_cities.csv file.

### 2. Dashboard Architecture (Power BI)

The clean dataset was imported into Power BI to create a highly visual decision-making tool: 

* **Value-for-Money Scatter Chart:** Plots the *Cost of Living Index* against the *Quality of Life Index*. This enables users to instantly isolate "sweet spot" cities (high quality of life at a lower cost).
* **Global Hotspot Map:** Pins cities geographically, using bubble sizes to represent cost tiers.
* **Interactive Slicers:** Allows users to filter all visuals instantly by Region, Quality of Life Category, and Development Tier.
* **Executive KPIs:** Displays total city counts, average quality of life, and average global internet speeds based on the user's active filters.

###  Key Insights from the Data

* **The Sweet Spot:** Several cities in the Eastern European and Asian regions offer a high quality of life index while maintaining a cost of living index below 50.
* **The Correlation:** There is a clear positive correlation between cost and quality of life, but the scatter plot highlights clear outliers where remote workers can get incredible value for their money.

###  How to Run this Project

1. Clone this repository to your local machine.
2. Open the Jupyter Notebook file to view the step-by-step Python cleaning script.
3. Open the .pbix file using **Power BI Desktop** to interact with the dashboard live.
