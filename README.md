![CI](https://github.com/youruser/project_name/actions/workflows/ci.yml/badge.svg)
# Python-Project-Template

This repository is a **project template** for Python-based scientific or analytical work.  
It provides a standardized structure, development tools, and configuration to quickly start new projects.

Before using it, you must modify the configuration and metadata files according to your specific project.

---

## Required Modifications

Before starting development, update the following files:

- `pyproject.toml`
  - Change `project_name`
  - Update description
  - Update author name and email
  - Adjust dependencies if needed

- `environment.yml`
  - Adjust Python version if necessary
  - Modify project-specific dependencies

- `README.md`
  - Replace this template description with your project description

- `CITATION.cff`
  - Update title
  - Update version
  - Update release date
  - Update repository URL
  - Adjust authors and affiliations

- `src/project_name/`
  - Rename the package folder to match your project name

Failing to update these fields may result in incorrect metadata or citation information.

---

## 📦 Installation

### 1. Modify environment configuration

Edit the following files according to your project needs:

- `environment.yml` → adjust Python version and dependencies  
- `pyproject.toml` → update project name, description, authors, and dependencies  

Then create the environment:

```bash
conda env create -f environment.yml
conda activate project_env
```
---
### 2. Modify project metadata

Before installation, update:

* project_name in pyproject.toml
* the folder name inside src/
* this README.md
* author information and contact email

Then install in editable mode:
```bash
pip install -e .[dev]
```

If you need documentation dependencies:

```bash
pip install -e .[dev,docs]
```
---
### Running Tests
```bash
pytest
```
---
### Linting & Formatting

Check code quality:

```bash
ruff check .
```

Auto-fix issues:

```bash
ruff check --fix .
```

Format code:
```bash
ruff format .
```
---
### Build Documentation (Sphinx)

From the docs/ directory:

```bash
make html
```

The built docs will be available in:

```bash
docs/_build/html/index.html
```
---
### Project Structure

```bash
project_name/
│
├── src/project_name/
├── tests/
├── docs/
├── pyproject.toml
├── environment.yml
└── README.md
```
---
### License

MIT License.
