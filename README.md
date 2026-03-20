# Examination WS25/26

This repository contains the material for the Statistical Programming term paper for Winter Semester 2025/2026.

The project combines:
- exploratory and applied analysis in Python
- Quarto-based report writing
- supporting data files for Sections 1 to 3

## Project Structure

- `Quarto/assignment.qmd`: main Quarto report
- `Quarto/assignment.pdf`: rendered PDF output
- `Aufgabe 1/Aufgabe1.ipynb`: notebook for Section 1
- `Aufgabe 2/Aufgabe2.ipynb`: notebook for Section 2
- `Aufgabe 3/Aufgabe3.ipynb`: notebook for Section 3
- `Daten/`: input data and generated prediction file
- `pyproject.toml`: Python dependencies
- `uv.lock`: locked dependency versions for `uv`

## Environment Setup

This repository uses `uv` and a local virtual environment in `.venv`.

Install dependencies:

```powershell
uv sync
```

Activate the environment manually if needed:

```powershell
.\.venv\Scripts\Activate.ps1
```

## Running the Quarto Document

Render the full report from the repository root with:

```powershell
quarto render Quarto\assignment.qmd
```

This executes the code cells and rebuilds the output document.

## Working in VS Code

For interactive work:
- open `Quarto/assignment.qmd`
- make sure the selected kernel uses `.venv\Scripts\python.exe`
- restart the kernel if execution state looks stale

If Quarto cells keep running forever or the kernel repeatedly restarts, check that the Jupyter kernel points to the local `.venv` interpreter rather than a system or Windows Store Python.

## Data Files

The `Daten/` folder contains the datasets used throughout the assignment, including:
- Berlin Airbnb listings and geo data for the descriptive and regression sections
- train/test data for the classification section
- `predictions.csv` for final model output

## Notes

- The Quarto report and the notebooks overlap in content, but `Quarto/assignment.qmd` is the main integrated submission document.
- The repository currently targets Python `3.13` according to `.python-version`.
