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

Do `pip install uv`. Then create and activate a virtual environment:
```
function makenv {
    deactivate || true
    rm -r .venv
    uv venv
    source .venv/bin/activate
    uv sync
}
makenv
```
