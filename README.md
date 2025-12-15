# kaggle

## Python & virtual environment

This repository is set up to use pyenv and a local virtual environment.

- Local Python (pyenv): the project uses the Python version in `.python-version` (3.13.9).
- Virtual environment: a venv was created at `.venv` using the pyenv-managed Python.

Quick start (zsh):

```zsh
# ensure pyenv is initialized in your shell (adapt if you use a different shell)
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"

# activate the venv
source .venv/bin/activate

# verify
python -V
pip install --upgrade pip setuptools wheel
```

PyTorch compatibility note

According to PyTorch's official docs, Stable PyTorch requires Python 3.10 or later. This project uses Python 3.13.9 which is supported by recent PyTorch releases. Install torch with the command appropriate for your CUDA/CPU setup; for CPU-only:

```zsh
pip install torch torchvision
```

If you want a different Python version, use `pyenv install <version>` and `pyenv local <version>` in the repository root, then recreate the venv with `python -m venv .venv`.