# Pandas for Python Developers

A 45-minute practical introduction to pandas for experienced Python developers who have not used the library before. The talk assumes comfort with Python but no prior knowledge of pandas or data science tooling.

## Format

A single Jupyter notebook that doubles as both the presentation and the reference material. Markdown cells are written as prose and read directly during the talk. Code cells are executed live.

## What's Covered

- **Mental model** — Series, DataFrame, Index, and dtypes: the four concepts you need before anything else makes sense
- **Loading data** — reading CSV and JSON with `pd.read_csv` and `pd.read_json`; how this compares to doing the same work in plain Python
- **Inspection** — `shape`, `dtypes`, `head`, `info`, `describe`
- **Selection** — label-based indexing with `.loc`, boolean masks, and why chained indexing is a problem
- **Missing data** — detecting, dropping, and filling nulls with `isna`, `dropna`, and `fillna`
- **Grouping and aggregation** — `groupby` with `agg` for summarising data across categories
- **String operations** — vectorised string methods via the `.str` accessor
- **Adding data** — why `DataFrame.append` is gone in pandas 3.x, and the correct patterns using a Python list accumulator and `pd.concat`

## Dataset

All examples use a synthetic web server access log generated with a fixed random seed (`random.seed(42)`), so output is fully reproducible. The dataset contains 5,000 rows and the following columns:

| Column | Description |
|---|---|
| `timestamp` | ISO 8601 request timestamp |
| `ip` | Client IP address |
| `method` | HTTP method (`GET`, `POST`, etc.) |
| `endpoint` | Request path |
| `status_code` | HTTP response code |
| `response_ms` | Response time in milliseconds |
| `bytes_sent` | Response size in bytes |
| `log_level` | Severity level (`INFO`, `WARNING`, `ERROR`) |

The dataset is provided in both CSV and JSON formats.

## Requirements

- Python 3.11+
- pandas 3.x
- Jupyter

