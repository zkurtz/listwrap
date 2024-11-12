# listwrap

Formatting lists of strings.

Use cases include subtasks of automatic config generation or any other highly structured context such as programmatically constructing human-readable SQL statements.

We're [on pypi](https://pypi.org/project/listwrap/), so you can `pip install listwrap` or `poetry add listwrap` etc.

## Examples

```
>>> from listwrap import align
>>> print(align(["a", "b", "c"]))
    "a",
    "b",
    "c",
>>> print(align(["a", "b", "c"], quote=None))
    a,
    b,
    c,
>>> print(align(["a", "b", "c"], indent=1))
 "a",
 "b",
 "c",
>>> print(align(["a", "b", "c"], indent=0, vertical=False))
"a","b","c",
```
Several formatting other options are supported; see the `align` method docstring.

## Development

Install poetry:
```
curl -sSL https://install.python-poetry.org | python3 -
```

Install [pyenv and its virtualenv plugin](https://github.com/pyenv/pyenv-virtualenv). Then:
```
pyenv install 3.12.2
pyenv global 3.12.2
pyenv virtualenv 3.12.2 listwrap
pyenv activate listwrap
```

Install this package and its dependencies in your virtual env:
```
poetry install --with dev
```

Set up git hooks:
```
pre-commit install
```
