# Python GitHub template with Poetry and Pre-Commit hooks

A template for python projects with pre-commit hooks, poetry, mypy and pytest

## Features:
- a standard repository structure
- `.gitignore` - for python, pycharm and vscode files
- `poetry` - for dependency management and virtual environment
- `pytest` setup for success
- `mypy` for type checking
- `pre-commit` hooks:
    - `isort` - to sort `import` statements
    - `ruff` - for linting and static analysis
    - `black` - for source code formatting
    - `docformatter` - for formatting docstrings
    - `mypy` - for typechecking


  
## repository structure
```
/
├── README.md      # edit this file to write your own readme
├── pyproject.toml # edit this file to setup the name and authors of your project
├── .gitignore     # preconfigured ignores for python, pycharm and vscode files
├── src/           # place your source files and packages here
│   ├── your_module.py
│   ├── your_package/
│   │   ├── ... 
│   ├── ...
├── tests/         # place your pytest files here
│   ├── test_your_stuff.py   # example
│   ├── ...
├── .pre-commit-config.yaml  # preconfigured pre-commit hooks
```

## Setup
- first make sure you have poetry installed by running
  ```bash
  poetry --version
  ```
  - > if you don't, visit https://python-poetry.org/docs/#installing-with-the-official-installer

- next , install all tools and dependencies using poetry
  ```bash
  poetry install
  ```
  - > this will also install `pre-commit` for you

- now run `pre-commit` to setup all your tools
  ```bash
  poetry run pre-commit run --all-files
- install your pre-commit hooks into the repository
  ```bash
  poetry run pre-commit install
- edit the `name`/`description`/`version`/`author` fields in `pyproject.toml`
## Howto
- run all hooks
  ```bash
  poetry run pre-commit run --all-files
  ```
- run tests
  ```bash 
  poetry run pytest
  ```