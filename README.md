# workspace

Python project with Jupyter notebooks.

## Setup

### Windows
```powershell
python -m venv .venv
.venv\Scripts\activate        # Windows: .venv\Scripts\activate
pip install -e ".[dev]"
nbstripout --install             # strip notebook outputs on commit
```

#### NVIDIA GPU (optional)

On Windows, `pip install torch` installs the CPU-only build. To train on an NVIDIA GPU, reinstall PyTorch with CUDA support:

```bash
pip install torch --index-url https://download.pytorch.org/whl/cu130
```

### Linux 
```bash
python -m venv .venv
source .venv/bin/activate
pip install -e ".[dev]"

## Install the nbstripout git filter
python -m venv ~/.venvs/nbstripout
~/.venvs/nbstripout/bin/pip install nbstripout
~/.venvs/nbstripout/bin/pip nbstripout --install
```

The notebooks detect the GPU automatically and fall back to the CPU if none is available.


## Usage

```bash
jupyter lab
```
## Exercises

| Notebook | Description |
|---|---|
| `notebooks/02_mini_gpt.ipynb` | **Mini-GPT** (German): students choose a dataset (presets, their own `.txt` file, or pasted text), then tokenize it, build and train a small character-level transformer with a live loss chart, generate text, and explore attention and embeddings. The default CPU setting trains in a few minutes. |


- `notebooks/` – Jupyter notebooks
- `src/workspace/` – reusable Python code (importable from notebooks)
- `data/` – local data files (git-ignored)
