# Tricks in Econometricks

Executable notes on econometric methods, built with Quarto and Python.

## Local development

```bash
uv sync
QUARTO_PYTHON=.venv/bin/python quarto preview
```

Render the production site with:

```bash
QUARTO_PYTHON=.venv/bin/python quarto render
```

The rendered site is written to `_site/`.
