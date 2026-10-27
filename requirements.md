# Requirements — Gemini Data Science Assistant

This file lists the software and Python packages needed to run the Gemini Data Science Assistant project.

## Software

- Python 3.10 or a version supported by the installed Google Gen AI SDK
- Anaconda Navigator with Jupyter Notebook, or another Python environment
- A Google Gemini API key from Google AI Studio: https://aistudio.google.com/app/apikey

## Python Packages

Install the packages used by the project:

```bash
python -m pip install -r requirements.txt
```

Example `requirements.txt` contents:

```text
google-genai
pandas
python-dotenv
jupyter
```

> If your notebook imports additional packages, add them to `requirements.txt`. If it uses a different Gemini SDK, update the package list to match your code.

## API Key Configuration

Set the `GEMINI_API_KEY` environment variable before starting Jupyter.

**Windows PowerShell:**

```powershell
$env:GEMINI_API_KEY="YOUR_API_KEY"
jupyter notebook
```

Read the key in Python:

```python
import os

api_key = os.getenv("GEMINI_API_KEY")
if not api_key:
    raise ValueError("Please set the GEMINI_API_KEY environment variable.")
```

Never commit your real API key, passwords, or `.env` file to GitHub.

## Dataset

- Use a CSV dataset compatible with Pandas if the notebook loads CSV data.
- Place the dataset in the project folder or update the file path in the notebook.
- Do not upload confidential, private, or personally identifiable data.

## Important

`requirements.md` documents setup requirements. Python's package installer expects a file named **`requirements.txt`** for the `pip install -r requirements.txt` command. Keep both files only if you want documentation (`requirements.md`) as well as an installable dependency list (`requirements.txt`).
