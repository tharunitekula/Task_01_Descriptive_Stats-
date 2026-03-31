# Task_01_Descriptive_Stats-
## Project Description
This project analyzes a real-world dataset of Facebook political ads from the 2024 U.S. Presidential election. The goal is to compute descriptive statistics in two different ways:

1. Using only Python's standard library.
2. Using the Pandas library.

The purpose of this assignment is to understand both the mechanics of descriptive statistics and the tradeoffs between manual computation and high-level data analysis tools.

## Dataset
Source: Google Drive folder provided in the assignment.

Important: The dataset file is **not included** in this repository. Download it manually from the source link and place it in the `data/` folder.

Example:
```bash
data/2024_facebook_political_ads.csv
```

## Files
- `pure_python_stats.py` - descriptive statistics using only the Python standard library
- `pandas_stats.py` - equivalent descriptive statistics using Pandas
- `requirements.txt` - dependencies for the Pandas script
- `FINDINGS.md` - narrative summary of findings
- `COMPARISON.md` - reflection on pure Python vs Pandas

## How to Run

### 1. Clone the repository
```bash
git clone <your-repo-url>
cd Task_01_Descriptive_Stats
```

### 2. Create and activate a virtual environment
```bash
python -m venv venv
```

#### On Windows
```bash
venv\Scripts\activate
```

#### On macOS/Linux
```bash
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the pure Python script
```bash
python pure_python_stats.py data/2024_facebook_political_ads.csv
```

### 5. Run the Pandas script
```bash
python pandas_stats.py data/2024_facebook_political_ads.csv
```

## Summary of Findings
Update this section after running your analysis on the dataset. You should describe:
- Which organizations spent the most.
- Which candidates were mentioned most often.
- Whether spending appears concentrated or distributed.
- Whether there are time-based spikes in ad purchases.
- Any surprising data quality issues or outliers.

## Comparison of Approaches
The pure Python version makes every step explicit: loading data, handling missing values, inferring types, and computing statistics manually. This helps build a deeper understanding of what descriptive statistics actually require.

The Pandas version is much faster and more concise, but it also hides many implementation decisions. For example, Pandas silently handles missing values and type coercion in ways that are convenient but less transparent than the pure Python approach.

## Reproducibility
This repository avoids hardcoded absolute file paths. Anyone who downloads the dataset into the `data/` folder and installs the listed dependencies should be able to reproduce the same results.
