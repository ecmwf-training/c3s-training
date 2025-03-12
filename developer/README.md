# Developer instructions

# Create a JUPYTER-BUILD environment with dependencies installed:

```
. ./developer/create-environment-for-build
```

## Rebuild jupyter book

```
rm -rf _build
jupyter-book build --all .
```

## View local build

```
open _build/html/index.html
```


## Troubleshooting notes

1. Multiple Level 1 Headers (#) in a notebook seems to break the _toc definition of title. It is also bad practice so discourage.
