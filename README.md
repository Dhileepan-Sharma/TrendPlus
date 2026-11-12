# TrendPulse — YouTube Trending Video Analysis

A four-part data project on the **Trending YouTube Video Statistics** dataset: daily snapshots of videos on YouTube's Trending list for **US, GB and IN** (46,230 raw rows, 45,908 after cleaning) plus a `categories.csv` lookup.

## Dataset name and source
* **Name:** Trending YouTube Video Statistics (public dataset, available on Kaggle).
* **Important:** the CSVs committed here are the course's **synthetic reproduction** of that dataset (same schema, same kinds of messiness, generated with a fixed seed). They are **not real YouTube data**, and I did not create the original dataset. Patterns reported in the analyses (for example "Music stays on the list longest") were built into the generator, so they demonstrate the methods rather than describing real YouTube behaviour.
* No personal or private data is included.

## Parts (each folder is self-contained, with its own data, README and requirements)
| Part | Folder | What it contains |
|---|---|---|
| 1 | [`part1_python_foundations/`](part1_python_foundations/) | Core-Python cleaning, data structures, scope, loops and rule-based video classification (Colab/Jupyter notebook) |
| 2 | [`part2_numpy_pandas/`](part2_numpy_pandas/) | NumPy engagement score, broadcasting, Pandas cleaning, merges, groupby and lifespan analysis |
| 3 | [`part3_visualization_eda/`](part3_visualization_eda/) | 7 charts, distributions/outliers, correlation, funnel, retention, cohorts and a content-strategy briefing |
| 4 | [`part4_sql_spreadsheet/`](part4_sql_spreadsheet/) | MySQL schema and 10 queries with outputs, plus an Excel workbook with pivot, lookups and cross-check |

## How to run
Each Part's README gives install and run steps. In short: `pip install -r requirements.txt` inside the Part folder, then run the notebook top to bottom (*Restart and run all*, or `jupyter nbconvert --to notebook --execute --inplace <notebook>`). Part 4 additionally needs MySQL (Workbench) for the `.sql` files.

## Git workflow
Each Part was developed on its own feature branch (`part1-cleaning`, `part2-wrangling`, `part3-eda`, `part4-sql-spreadsheet`) with several commits touching only that Part's folder, then merged into `main` with a merge commit. View it with `git log --graph --oneline --all`.
