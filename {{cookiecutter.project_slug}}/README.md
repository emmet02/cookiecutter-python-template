# {{ cookiecutter.project_name }}

{{ cookiecutter.project_description }}

---

## 🚀 Quickstart

This project is managed with `uv`. You do not need to manually create or activate the virtual environment.

### 1. Setup

Run the following command to have `uv` create a virtual environment (if it doesn't exist) and install all dependencies from `pyproject.toml`.

```bash
uv sync
```

All subsequent commands should be executed via `uv run`, which will automatically use the project's virtual environment.

### 2. Install Pre-commit Hooks

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
