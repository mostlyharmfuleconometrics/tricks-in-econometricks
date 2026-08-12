# Tricks in Econometricks

Tricks in Econometricks is a shared blog for practical, applied econometric
methods. Contributors can use Python or R to explain estimators, diagnostics,
research designs, and reproducible workflows with executable examples.

The homepage is generated from the Quarto documents under `posts/`. Each post
is a self-contained Quarto document and should state the assumptions behind the
method, show how to apply it, and explain how to interpret the result.

## Set up the project

Install [Quarto](https://quarto.org/docs/get-started/) and clone this
repository. For Python posts, create the project environment with:

```bash
uv sync
```

For R posts, install R and the packages that Quarto uses to execute R code:

```bash
Rscript -e 'install.packages(c("knitr", "rmarkdown"))'
```

Python dependencies belong in `pyproject.toml` and `uv.lock`. Add them with
`uv add <package>`. State any extra R package requirements in the post and
install them with `install.packages()`.

## Write a post

Add a `.qmd` file under `posts/`. Select one execution engine in its YAML
header.

For Python:

```yaml
---
title: "Post title"
jupyter: python3
---
```

For R:

```yaml
---
title: "Post title"
format: html
---
```

Use `{python}` or `{r}` for executable code blocks. The existing posts provide
complete examples for both languages.

## Preview and render

Preview the full blog with:

```bash
QUARTO_PYTHON=.venv/bin/python quarto preview
```

Render the production site with:

```bash
QUARTO_PYTHON=.venv/bin/python quarto render
```

Quarto uses the project Python environment for Python posts and the installed R
environment for R posts. The rendered site is written to `_site/`.

## Contribute

Open a pull request with one focused method or workflow. Before submission,
render the full site and check that the post includes its code, output, and the
information needed to reproduce the example.
