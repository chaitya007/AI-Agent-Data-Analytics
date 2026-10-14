# Data Analytics AI Agent

A Streamlit application for importing, cleaning, querying, visualizing, and profiling datasets.

## Features

- Import CSV and Excel files, JSON/CSV API responses, and database tables through SQLAlchemy.
- Assess and clean missing values, duplicates, whitespace, dates, data types, and outliers.
- Store cleaned data in a temporary SQLite database and run SQL queries.
- Generate natural-language SQL and data insights with the optional Hugging Face Inference API; rule-based fallbacks are available without a token.
- Create interactive Plotly visualizations and downloadable HTML profiling reports.
- Save version snapshots as CSV files with JSON metadata under `data_versions/`.

## Tech Stack

Python, Streamlit, pandas, NumPy, SQLAlchemy, SQLite, Plotly, scikit-learn, requests, and ydata-profiling.

## Run Locally

Python 3.11 or newer is recommended.

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
streamlit run app.py
```

Open the local URL printed by Streamlit, typically `http://localhost:8501`.

AI features are optional. To enable them, set the `HF_API_KEY` environment variable to a Hugging Face token before starting the app. Do not commit API tokens or other secrets.

## Project Structure

```text
.
├── app.py
├── modules/
│   ├── ai_services.py
│   ├── data_cleaning.py
│   ├── data_ingestion.py
│   ├── database_manager.py
│   ├── profiling.py
│   ├── version_control.py
│   └── visualization.py
├── utils/
│   └── helpers.py
├── requirements.txt
└── data_versions/       # Version metadata and saved snapshots
```

---

## 📈 Future Enhancements

- ☁️ Streamlit Cloud / GCP Deployment for scalable access.
- 🧾 Role-Based Access Control (RBAC) for governed environments.
- ⏱ Automated Scheduling & Reporting Pipelines.
- 🗃 Integration with BigQuery or Hive for big-data scalability.
