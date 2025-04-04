# c3s-training

Master repository for the notebooks to be included in the C3S JupyterBook

## C3SBook

This repository contains a book of notebooks generated with Jupyter Book. Below are the instructions for working with this project, including how the structure of the notebooks works and how to perform the build and deploy process of the book.

## Notebook and Submodule Structure

The book of notebooks is organized using submodules, which allows for maintaining a modular structure and facilitates managing the different topics and sections of the book. Each submodule is a training book and it's uploaded in GitHub as a repository. The submodule structure is defined in the `_toc.yml` file and stored in `notebooks` directory.

## Building and Deploying the Book

To build and deploy the book of notebooks, follow these steps:

### 1. Rebuild the Book

To rebuild the book, first remove the existing `_build` folder and then run the following command to rebuild the book:

```bash
rm -rf _build
jupyter-book build --all .
```

### 2. Book Deployment

Once the book has been successfully rebuilt, you can deploy it to the `gh-pages` branch using `ghp-import`. Run the following command to copy the `_build/html` folder to the `gh-pages` branch and deploy the book:

```bash
ghp-import -n -p -f _build/html
```

# Run our notebooks

In the `notebooks` folder, you'll find all the Jupyter notebooks.

Additionally, there's a `environment.yml` file, containing the conda channels and a list of python dependencies needed for running our notebooks, as presented in the example below


```bash
name: example-environment
channels:
  - conda-forge
  - defaults
dependencies:
  - numpy == 1.26.4
  - cdsapi == 0.6.1
  - pandas == 2.1.4
  - netCDF4 == 1.6.2
  - dask == 2023.11.0
  - xarray == 2023.6.0 
  - matplotlib == 3.8.0 
  - cartopy == 0.22.0
  - jupyterlab==4.3.4
  - myst-parser==4.0.0
```

The first line of the environment.yml file sets the new environment’s name and you can activate this environment by executing the following commands in your terminal:


```bash
conda env create -f environment.yml
conda activate example-environment
```
To verify that the environment is installed correctly and check the list of environments available you can execute  

```bash
conda env list
```


To run the notebooks on your local machine, please refer to [C3S Book:How to run these tutorials ](https://ecmwf-training.github.io/c3s-training/how-to-run-these-tutorials.html) section for detailed instructions.
