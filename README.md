# Olifant TODO Tracker 🐘

> A lightweight, read-only development tool that scans your project for TODO comments and generates a comprehensive report with Git blame integration.

Stop losing track of code tasks. Just write `TODO: fix this` in your code—Olifant finds it, checks who wrote it and when, and compiles everything into a clean `TODO_LIST.md` report.

---

## Features

- **Read-Only & Safe** – Never modifies your source code. Scans and reports only.
- **Git Integration** – Automatically runs `git blame` to identify the author and date for every TODO.
- **Centralized Tracking** – Generates a `TODO_LIST.md` table with descriptions, clickable file links, authors, and timestamps.
- **Clean Reports** – Smart truncation keeps descriptions readable and reports organized.
- **Language Agnostic** – Works with Python, JavaScript, C++, Java, and more.

---

## Installation

1. Clone this repository or download `Olifant.py` into your project root:
   ```bash
   git clone https://github.com/yourusername/olifant.git
   ```

2. *(Optional)* Add `TODO_LIST.md` to your `.gitignore` if you prefer not to commit tracking reports:
   ```bash
   echo "TODO_LIST.md" >> .gitignore
   ```

---

## Usage

### Step 1: Write TODO Comments

Add standard TODO comments anywhere in your codebase:

```python
# TODO: Refactor this function later
def my_function():
    pass
```

### Step 2: Run Olifant

Execute the script from your project root:

```bash
python .\Olifant.py
```

### Step 3: Review the Report

Open the generated `TODO_LIST.md` to see a formatted table:


# Olifant TODO Tracker
**Last updated:** 2025-11-22 16:42:09

| ID | Description | Location | Author | Date |
|----|-------------|----------|--------|------|
| 1 | Refactor this function later | [`test.py:1`](test.py) | Emil | 2025-11-22 |
| 2 | For future me to fix this | [`test.py:5`](test.py) | Not Committed Yet | 2025-11-22 |


**Note:** TODOs not yet committed to version control will display "Not Committed Yet" in the Author column. Once committed, Olifant updates the report with the correct contributor and commit date.

---

## How It Works

1. **Scans** your project files for TODO comments
2. **Runs** `git blame` on each file to extract authorship information
3. **Generates** a markdown table in `TODO_LIST.md` with all findings
4. **Updates** the timestamp on each run

---

## Requirements

- Python 3.6+
- Git (for blame integration)

---

**Made with 🐘 by developer who forget where he left his TODOs**
