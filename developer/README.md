# Developer instructions

## Updating the submodules

This repository does not automatically update the submodules, this is intentional and is to ensure that
the content is updated periodically and with the approval of the owners.

The following commands will update all the submodules to the current HEAD of the "main" branch.

```
# Change to submodule directory
cd submodules

# Update all submodules
./update-submodules 

# If happy with updates, git add, commit and push
git add .
git commit -m"Update submodules"
git push
```

## Build the JupyterBook locally

### Create a JUPYTER-BUILD environment with dependencies installed:

```
. ./developer/create-environment-for-build
```

### Rebuild jupyter book

```
rm -rf _build
jupyter-book build --all .
```

### View local build

```
open _build/html/index.html
```



## Troubleshooting notes

1. Multiple Level 1 Headers (#) in a notebook seems to break the _toc definition of title. It is also bad practice so discourage.
