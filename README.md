# Social Engine — Data Cleaning & EDA

Data cleaning and exploratory data analysis for the **Social Engine Slayers — Round 1: Rebuilding the Social Engine** challenge.

## Overview

The project cleans a deliberately corrupted social-media dataset and performs EDA to identify patterns, anomalies, distributions, and relationships.

### Final Dataset
- **12,000** cleaned posts
- **1,500** users
- **01 May 2024 – 30 April 2025**
- 5 platforms: Facebook, YouTube, Twitter, Reddit, Instagram

## Data Cleaning

The cleaning workflow includes:

- Timestamp format standardisation
- Duplicate post removal
- User ID validation
- Post-date validation against account creation
- HTML and text artefact removal
- Numeric type standardisation
- Negative engagement correction
- Missing-value handling without fabrication
- Platform value validation

The original **12,360 records** were reduced to **12,000 unique posts** after duplicate removal.

## EDA

The analysis covers:

- Platform distribution
- Daily, weekly, and hourly posting activity
- Likes, shares, and comments
- Engagement by platform
- Engagement correlations
- User activity
- Follower count vs. likes
- Language and geographic distribution
- Text length
- Text length vs. likes

### Key Findings

- Platform volumes are relatively balanced.
- Posting activity remains stable across the year.
- Wednesday is the busiest day with **1,771 posts**.
- 23:00 is the busiest known posting hour with **388 posts**.
- Likes, shares, and comments have almost **zero correlation** with each other.
- Follower count has almost no correlation with likes (**r = 0.01**).
- Text length has almost no correlation with likes (**r ≈ -0.00**).
- The dataset has substantial geographic and multilingual diversity.

## Repository Structure

```text
├── Data_Cleaning.ipynb
├── EDA_Professional.ipynb
├── Social_Engine_Users.csv
├── Social_Engine_Posts_Corrupted.csv
├── Social_Engine_Posts_Cleaned.csv
├── Social_Engine_EDA_Final.pdf
├── dataset.js
└── README.md
````

## Reproducibility

Install the required packages:

```bash
pip install pandas numpy matplotlib seaborn jupyter reportlab
```

Run:

```text
Data_Cleaning.ipynb
```

to generate the cleaned dataset, followed by:

```text
EDA_Professional.ipynb
```

to reproduce the exploratory analysis and report. This report had text content added after the analysis manually as expert analysis report.

## Outputs

* **Cleaned Dataset:** `Social_Engine_Posts_Cleaned.csv`
* **EDA Notebook:** `EDA_Professional.ipynb`
* **Final EDA Report:** `Social_Engine_EDA_Final.pdf`