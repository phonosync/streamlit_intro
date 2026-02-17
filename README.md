# Streamlit Intro - Uber Pickups in NYC

A Streamlit demo app following the official tutorial:
[Create an app](https://docs.streamlit.io/get-started/tutorials/create-an-app)

The app loads Uber pickup data for September 2014 in New York City and provides:

- A histogram of pickups by hour
- An interactive map filtered by hour using a slider
- A toggle to view raw data

## Local Development

### Prerequisites

- [uv](https://docs.astral.sh/uv/getting-started/installation/)

### Setup

```bash
uv sync
```

This creates a `.venv` with Python 3.12 and installs all dependencies.

### Run

```bash
uv run streamlit run uber_pickups.py
```

The app will open at `http://localhost:8501`.

## Deploy on Streamlit Community Cloud

Streamlit Community Cloud uses `requirements.txt` to install dependencies. This file is already included in the repo and kept separate from `pyproject.toml` (which is used for local development with uv).

You can programmatically create it from `pyproject.toml`:
```bash
uv pip compile pyproject.toml -o requirements.txt
```

1. Push this folder to GitHub.
2. Go to [share.streamlit.io](https://share.streamlit.io) and sign in with GitHub.
3. Click **Create app** and select your repository, branch (`main`), and set the main file path to `uber_pickups.py`.
4. Select Python version 3.12 (Advanced Settings)
5. Click **Deploy**.


