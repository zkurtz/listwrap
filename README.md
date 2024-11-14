# listwrap

Formatting lists of strings.

Use cases include subtasks of automatic config generation or any other highly structured context such as programmatically constructing human-readable SQL statements.

We're [on pypi](https://pypi.org/project/listwrap/), so `pip install listwrap`.

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

1. Install poetry: `curl -sSL https://install.python-poetry.org | python3 -`
1. Install [pyenv and its virtualenv plugin](https://github.com/pyenv/pyenv-virtualenv).
1. Create a dev ops virtual environment using [makenv](https://gist.github.com/zkurtz/eabd6fef97ee7ef3d3a45bf2cc45c6bf):
```
PYTHON_VERSION=3.12.2
makenv listwrap
```
