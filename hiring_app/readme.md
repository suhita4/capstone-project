# HireIQ - AI-Powered Candidate Ranking

## Requirements

- Python 3.11+
- pip

## Setup

```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

## Run

```bash
cd hiring_app
py -3.11 app.py
```

App runs at `http://localhost:5000`

## API

```
POST /recommend
Content-Type: application/json

{"job_description": "Looking for a Python data scientist with SQL experience.", "top_n": 5}
```

Response includes ranked candidates with `matched_skills`, `missing_skills`, and `total_score`.

## Tests

```bash
cd hiring_app
pytest test_pipeline.py -v
```
