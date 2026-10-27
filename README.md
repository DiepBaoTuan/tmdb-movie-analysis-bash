# Movie Data Analysis with Bash

Analysis of the **TMDB movie dataset** (10K+ movies) using only command-line tools: `curl`, `sed`, `awk` and `sort`. No Python, no database.

**Script:** [`DiepBaoTuan_K19_LV1_Project1.sh`](DiepBaoTuan_K19_LV1_Project1.sh)

## Questions answered

| # | Question | Output |
|---|---|---|
| 1 | Sort movies by release date, newest first | `resultQ1.txt` |
| 2 | Movies with an average rating of 7.5 or higher | `ResultQ2.txt` |
| 3 | Movies with the highest and lowest revenue | Console |
| 4 | Total revenue of all movies | Console |
| 5 | Top 10 movies by revenue | Console |
| 6 | Director and actor with the most movies | Console |
| 7 | Number of movies per genre | Console |

## Data-cleaning techniques

- Commas inside quoted fields are replaced with `awk`, so CSV columns split correctly.
- Columns are looked up by **header name** instead of a fixed position, so the script is robust to column order.
- Two-digit years (`12/15/15`) are converted to sortable `yyyy-mm-dd` dates.
- Multi-value fields (`director`, `cast`, `genres`, separated by `|`) are split and counted with associative arrays.

## How to run

```bash
bash DiepBaoTuan_K19_LV1_Project1.sh
```

The script downloads the dataset automatically.
