# workspace

Python project with Jupyter notebooks.

## Setup

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -e ".[dev]"
nbstripout --install             # strip notebook outputs on commit
```

## Usage

```bash
jupyter lab
```

- `notebooks/` – Jupyter notebooks
- `src/workspace/` – reusable Python code (importable from notebooks)
- `data/` – local data files (git-ignored)
