# Source Code

## What lives here
Scripts, pipeline code, and utilities. Exploratory work goes in `notebooks/`.

## Setup
```bash
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## How to run
```bash
python src/main.py --input data/sample/example.csv --output work-in-progress/
```

## Structure
| File | Purpose |
|---|---|
| | |

## Conventions
- Add docstrings/comments explaining *why*, not just *what*.
- Read file paths from arguments or a config, not hard-coded to your machine.
- Never hard-code credentials. Use environment variables or a `.env` file (gitignored).
- Test on `data/sample/` before running on real data.

## If you used AI coding tools
Note which tools you used and for what, and confirm you did not send sensitive data to non-approved tools.
