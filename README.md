# workspace

Python project with Jupyter notebooks.

## Setup

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -e ".[dev]"
nbstripout --install             # strip notebook outputs on commit
```

### NVIDIA GPU (optional)

On Windows, `pip install torch` installs the CPU-only build. To train on an NVIDIA GPU, reinstall PyTorch with CUDA support:

```bash
pip install torch --index-url https://download.pytorch.org/whl/cu128
```

The notebooks detect the GPU automatically and fall back to the CPU if none is available.

## Exercises

| Notebook | Description |
|---|---|
| `notebooks/02_mini_gpt.ipynb` | **Mini-GPT** (German): students choose a dataset (presets, their own `.txt` file, or pasted text), then tokenize it, build and train a small character-level transformer with a live loss chart, generate text, and explore attention and embeddings. The default CPU setting trains in a few minutes. |

## Usage

```bash
jupyter lab
```

- `notebooks/` – Jupyter notebooks
- `src/workspace/` – reusable Python code (importable from notebooks)
- `data/` – local data files (git-ignored)
