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

*Not* inside any virtual environment, do `pip install uv`. Then create and activate a virtual environment:
```
uv venv --python 3.12.2
source .venv/bin/activate
uv sync
```

1. Create a dev ops virtual environment using [makenv](https://gist.github.com/zkurtz/eabd6fef97ee7ef3d3a45bf2cc45c6bf):
```
PYTHON_VERSION=3.12.2
makenv listwrap
```
