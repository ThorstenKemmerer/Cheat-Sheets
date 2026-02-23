# uv / uvx Cheat Sheet (Beginner, Common Commands)

> **uv**: fast Python package + project manager (replaces lots of `pip`, `venv`, `pip-tools`, etc. workflows)  
> **uvx**: “run a tool without installing it globally” (similar idea to `pipx run`)

---

## Install / Upgrade uv

### macOS / Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Windows (PowerShell)
```powershell
irm https://astral.sh/uv/install.ps1 | iex
```

### Upgrade
```bash
uv self update
```

### Check version
```bash
uv --version
uvx --version
```

---

## Create & Use a Project

### Create a new project
```bash
uv init my-project
cd my-project
```

### Add dependencies
```bash
uv add requests
uv add "fastapi>=0.110"
```

### Remove dependencies
```bash
uv remove requests
```

### Install/sync dependencies (from lock)
```bash
uv sync
```

### Run a command inside the project environment
```bash
uv run python -V
uv run python script.py
uv run pytest
```

---

## Virtual Environments

### Create a virtual environment
```bash
uv venv
```

### Create a venv in a specific path
```bash
uv venv .venv
```

### Activate the venv (optional)
Most of the time you can just use `uv run ...`, but you *can* activate:

**macOS / Linux**
```bash
source .venv/bin/activate
```

**Windows (PowerShell)**
```powershell
.venv\Scripts\Activate.ps1
```

---

## Python Versions

### Pick a Python version for the project (example)
```bash
uv python install 3.12
uv python pin 3.12
```

### List available/installed Python versions
```bash
uv python list
```

---

## Locking & Reproducible Installs

### Create/update lock file (if your workflow uses it)
```bash
uv lock
```

### Install exactly what’s locked
```bash
uv sync
```

---

## Running One-off Tools with `uvx` (No Global Install)

### Run a tool (downloads/caches as needed)
```bash
uvx ruff --version
uvx black --version
uvx pytest --version
```

### Run a specific version of a tool
```bash
uvx ruff==0.6.0 --version
```

### Typical examples
```bash
uvx ruff check .
uvx black .
uvx pytest -q
uvx mypy .
```

> Tip: `uvx` is great for CI or quick local runs when you don’t want to add the tool to your project dependencies.

---

## Working with Requirements Files (Common Interop)

### Install from requirements.txt
```bash
uv pip install -r requirements.txt
```

### Freeze installed packages to requirements.txt
```bash
uv pip freeze > requirements.txt
```

---

## Useful Diagnostics

### Show help
```bash
uv --help
uvx --help
uv pip --help
```

### Show where Python is coming from (sanity check)
```bash
uv run python -c "import sys; print(sys.executable)"
```

---

## Quick “Which command should I use?”

- **“I want a project with dependencies”** → `uv init`, `uv add`, `uv sync`, `uv run ...`
- **“I want to run a tool once”** → `uvx <tool> ...`
- **“I have requirements.txt”** → `uv pip install -r requirements.txt`
- **“I need a venv”** → `uv venv` (then `uv run ...`)

---