# Netflix Data Analysis

![Netflix](https://img.shields.io/badge/Netflix-E50914?style=for-the-badge&logo=netflix&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

**A comprehensive Exploratory Data Analysis (EDA) of Netflix's Movies and TV Shows catalog.**

---

## Overview

This project performs an in-depth analysis of Netflix's content portfolio using a publicly available dataset. It explores **content type distribution**, **geographic contributions**, **genre popularity**, and **frequent actors**, while addressing data quality challenges such as missing values and format inconsistencies.

The analysis provides actionable insights into Netflix’s content strategy, highlighting strengths, imbalances, and opportunities for better audience engagement and catalog growth.

---

## Dataset

- **Source**: Netflix Titles Dataset (Kaggle)
- **Period**: Historical snapshot of Netflix catalog
- **Structure**: Tabular data with each row representing a unique title (`show_id`)
- **Key Columns**: `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

**Data Credibility Note**: The dataset offers a reliable view of Netflix’s catalog during the collection period but has limitations — no viewer engagement metrics (watch time, ratings), and significant missing values in `director` and `cast` columns.

---

## Data Cleaning & Methodology

Key data preparation steps included:

- **Missing Value Handling**: Replaced NaN values in `director`, `cast`, and `country` with "Unknown" categories.
- **Duration Standardization**: Split `duration` into `movie_duration_min` and `tv_seasons` for accurate analysis.
- **Text Processing**: Split comma-separated fields (`listed_in`, `country`, `cast`) and exploded them for frequency counting.
- **Sanity Checks**: Verified data integrity after transformations.

```python
# Libraries Used
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px
