# {{ cookiecutter.project_name }}

{{ cookiecutter.project_description }}

---

## 🚀 Quickstart

This project is managed with `uv`.

### 1. Initial Setup

First, create and activate a virtual environment.

```bash
# Create the virtual environment
uv venv

# Activate the environment (macOS/Linux)
source .venv/bin/activate

# Activate the environment (Windows)
.venv\Scripts\activate
```

### 2. Install Dependencies

Sync the project dependencies using `uv`. This will install everything from `pyproject.toml` and `uv.lock`.

```bash
uv pip sync pyproject.toml --all-extras
```

### 3. Install Pre-commit Hooks

This template uses `prek` for fast pre-commit checks.

First, install `prek` using `uv`:
```bash
uv tool install prek
```

Then, install the git hooks:
```bash
prek install
```
Now, `prek` will run automatically on every commit to ensure code quality.

---

## ✅ Running Quality Checks

You can run all checks manually at any time.

### Linting and Formatting

This project uses `ruff` for linting and formatting.

```bash
# Check formatting
uv run ruff format --check .

# Check for linting errors
uv run ruff check .
```

### Type Checking

This project uses `ty` (a new, fast type checker from Astral) for static type analysis.

```bash
uv run ty check .
```

### Dependency Analysis

This project uses `deptry` to check for unused, missing, or transitive dependencies.

```bash
uv run deptry .
```

### Testing

This project uses `pytest` for running tests.

```bash
uv run pytest
```
