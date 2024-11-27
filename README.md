# Template repository

This repository is a template for creating a new Python project.
Using this template, has the following benefits:
- We use [`uv`](https://github.com/astral-sh/uv) to manage the Python version, dependencies, and the virtual environment. It is _much_ faster and better than `pip`.
- We set up vscode/cursor in a way that ensures a consistent coding style. In particular:
  - We format and lint the code with `ruff`, which is blazingly fast.
  - We perform type checking with `mypy`.
  - We enforce consistent sorting of imports with `isort`.
  - All of this is done automatically on every save!
  - We perform type checking with `mypy`.

## Initial setup (only once)
In order to use it, you need [`uv`](https://github.com/astral-sh/uv), which you can install globally with:
```sh
pip install uv
# or
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Edit the `pyproject.toml` file to set the project name, author, etc.

To install dependencies, do not use `pip`, but `uv` instead, e.g.:
```sh
uv add python-dotenv openai
```

Now, you can delete everything in the `README.md` file up to here and start coding. The installation instructions below are relevant once the project is created, which you just did!


## Installation

1. Install [`uv`](https://github.com/astral-sh/uv) globally:
    ```bash
    pip install uv
    ```

2. Create and activate a virtual environment with:
    ```bash
    uv sync
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
    ```

3. Set up environment variables:

    Create a `.env` file in the root directory of the project.
    Add the following environment variables to the `.env` file:
    ```
    OPENAI_API_KEY=your_openai_api_key
    ```

4. If you are using vscode/cursor (recommended), install the recommended extensions by searching `@recommended` in the extensions tab. This way, you will have syntax highlighting, linting, type checking, etc. on save!