# How to run these tutorials

The tutorials are in the form of [Jupyter notebooks](https://jupyter.org/), a powerful tool for interactive computing. Jupyter notebooks allow you to write and execute code, view the results, and add explanatory text all in one document. They are widely used in data science, research, and education due to their versatility and ease of use.

You will not need to install any software to work with Jupyter notebooks, as there are several free cloud-based services available for creating, editing, running, and exporting notebooks. These services provide a hassle-free environment where you can focus on your analysis without worrying about software installation or compatibility issues.

<hr>

## Possible Cloud-based services

:::{dropdown} WEKEO

[WEKEO](https://www.wekeo.eu/) is the EU Copernicus DIAS reference service for environmental data, virtual processing environments, and skilled user support. It is a platform for all audiences. This is our official platform for accessing the notebooks. You can access every notebook by clicking on the WEkEO link, which will redirect you to our official website. From there, you can open the notebook directly in JupyterHub. You need to be [signed up](https://www.wekeo.eu/register) to access the notebooks.

:::

```{warning}
These free cloud-based services are not supported by ECMWF
```

:::{dropdown} Binder

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/)

```{note}
Binder may take some time to load, so please be patient!
```

1. Click on the Binder badge
2. Wait for the Binder environment to load.
3. Once loaded, navigate to the desired notebook and click on it to open and interact with it.
   :::

:::{dropdown} Kaggle

[![Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code)

```{note}
Requires (free) registration with Kaggle. Once in, `switch on the internet` via settings.
```

1. Click on the Kaggle badge
2. If you're not logged in to Kaggle, sign in or create a free account.
3. After signing in, you'll be redirected to the Kaggle notebook interface with the option to open the notebook. Click on it to proceed.

:::

:::{dropdown} Colab

```{note}
Requires Google account, and installation of some libraries, you can add our `requirements.txt` file and install all of them with `pip install -r requirements.txt`
```

[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

1. Click on the Colab badge
2. If prompted, sign in to your Google account.
3. Once signed in, the notebook will open in Google Colab. You can then interact with and run the notebook in the Colab environment.

:::

:::{note}
These cloud-based services represent only a selection of the available options for running notebooks in the cloud. Users can leverage these services to execute Jupyter notebooks without the need to install any software locally. However, it's essential to note that this selection is not exhaustive, and users may explore other cloud-based platforms tailored to their specific needs and preferences.
:::

<hr>

## Run the notebooks locally

```{attention}
In our [github repository](https://github.com/ecmwf-training/c3s-training) you can find every notebook in `submodules/` folder.
```

### Key Concepts

If you are consindering to work with your notebooks locally, it is important that you are aware of some key concepts or information that you'll find in this tutorial or during the preparation and installation process. 

- **Dependencies** are all of the software components required by your notebook in for it to work as intended and avoid runtine errors. They can be libraries, frameworks, or other programs. 

- **Packages** are a way to organize and group together related dependencies. They act like toolboxes, storing and organizing tools making easier to install and manage dependencies.  

- **Conflicting dependecies or dependency hell** are issues that occur when two or more packages that are sharing dependencies in a project, require different versions of the same dependency. Because only a single version of a dependency is 
  permitted in any project's environment.     
 
- **Environments** are directories that contain a specific collection of packages that you have installed. You may have several environments with different versions for the same dependecy. If you change one environment, your other environments 
  are not affected. There is a `base environment`located at the root prefix that constains the system installation parameters. 
  
- **The activation** of an environment makes all its contents available to your terminal or shell.

- **The deactivation** of an environment is the opposite operation of activation, removing from your shell what makes the environment content accessible.
 
- **Pip** is the standard tool for installing or uninstalling Python packages and managing their dependencies. For more information visit [pip documentation](https://pip.pypa.io/en/stable/).

- **Conda** is an open-source, cross-platform package manager and environment management system which can be used to create Python and R development environments on many different platforms. It is particularly beneficial for data scientists, researchers, and developers working with diverse software requirements across different projects. For more information visit [Conda Documentation](https://docs.conda.io/projects/conda/en/latest/index.html)
  
- **Conda channels** are the locations where packages are stored. They serve as the base for hosting and managin packages. Remote channels like conda-forge offer a wide range of community- 
  maintained packages, expanding the available options for software development and experimentation.

- **Conda-forge** is a community channels made up of thousands of contributors, which contains repositories of conda recipes and thus provides conda packages 
  for a wide range of software. The `conda-forge` channel is free for all to use. For more information visit [conda-forge documentation](https://conda-forge.org/docs/).


### Conda installation

If you would like to run the notebooks in your own environment, we suggest you use [Conda](https://docs.conda.io/projects/conda/en/latest/index.html). Using conda provides a streamlined approach to package management, platform compatibility, environment isolation, and access to an extensive package ecosystem. Conda is available on Windows, macOS, or Linux and can be used with any terminal application (or shell). 

We suggest you use the [Miniforge](https://conda-forge.org/download/) installer, which contains most of the libraries you will need. Miniforge is an installer maintained by the conda-forge community that comes preconfigured for use with the conda-forge channel.

Basic installations instructions are available below. More detailed instructions are available in this [github repository](https://github.com/conda-forge/miniforge). 

**Unix-like platforms (Mac OS & Linux)**

Download the installe  and ru n`bash Miniforge3-$(uname)-$(uname -m).shh
*
Wi**o**
ws
Download and execute the Windows inllersta from [Miniforge](https://conda-forge.org/download/)ler
.

```{note}
There are several installers that you could use to install Conda. For more information about that visit [Installing conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html)
```


### Setting a virtual environment

In our notebooks we use packages that don't come as part of the standard dependencies of Python and some of these packages need specific dependecy versions that could be in conflict with other applications or projects in our local environment. The solution to this problem is to crenrtual environment where we are able to set up the versions and conditions to the releant dependencYou can easily activate or deactivate environments, which is how you switch between them. You can also share your environment with someone by giving them a copy of your `environment.yaml` file.ible.
With conda, you can create, export, list, remove, and update environments that have different versions of Python and/or packages installed in them. Switching or moving between environments is called activating the environment. You can also share an environment filWe suggest that you create an environment with commands in the most basic way using the terminal for the following steps:

1. To create an environment called `C3S-Training`.
  `conda create -n C3S-Training`  

2. When conda asks you to proceed, type `y`.

   This creates the `C3S-Training` environment in a /envs/ folder. No packages will be installed in this environment.

You will need to activate your environment each time you're planning to run the tutorial. To activate the `C3S-Training` environment you can use the command line with `conda activate C3S-Training`. As soon your envirnomend is activated, conda prepends the path name `C3S-Training` onto your system command.

To deactivate an environment, type in the command line: `conda deactivate`

  
### Install the ingrequired packale 

In our [github repository](https://github.com/ecmwf-training/c3s-training) you can find a `requirements.txt` file, containing a list of python dependencies needed for running our notebooks.

Using and mantaining a requirement.txt files is a good practice for Python development. It ensures that the necessary librarires and dependecies are well documented and easily reproducible, making it easier for others to work on the code and reducing the likelihood of conflict issues. 

In the figure below you can see an example of a requirement.txt file where there is a list of dependencies with their relevant and required version in a format "dependency_name == version". You can specify the version of a dependency using `==`,`>`,`>=`,`<`, `<=`, and so on. Omitting the version specifier installs the latest version.   

   ![Requirement.txt file example](requirement-file-exampl.p
n
```{note}
Before to install the required packages with the requirements file, remember to activate the relevant environment trough the command line `conda activate C3S-Training`
```
g)

To install all the dependencies included in the requirement file you need to run this command in the same directory of the requiremnent fil `
pip install -r requiremenxtts.
t`.

```{note}
For more information please check [requirement file format documentation](https://pip.pypa.io/en/stable/reference/requirements-file-format/). ```x


### Visualization of Notebooks

To visualize and execute the notebooks, we recommend downloading [JupyterLab](https://jupyter.org/), a versatile web-based interactive development environment. You can interact with our notebooks in this environment locally.

:::{note}
If you prefer a lightweight interface and want to consum less resources, you may consider downloading Jupyter Notebook instead of Jupyter Lab. Jupyter Notebook provides a basic yet efficient environment for running your notebooks without consuming as many resources. It's a great option for users who prioritize simplicity and performance in their workflow. Here's documentation of [Jupyter Notebook](https://docs.jupyter.org/en/latest/start/index.html)
:::

1. **Download JupyterLab**:

   - Visit the [Jupyter installation website](https://jupyter.org/install) in your web browser.
   - Navigate to the `Jupyter Lab` section and follow the instructions to download and install JupyterLab for your operating system (Windows, macOS, or Linux).

   ![Jupyter Lab install screenshot](jupyter-lab-install.png)

2. **Launch JupyterLab**:

   - After installing JupyterLab, open your terminal or command prompt.
   - Type `jupyter lab` and press Enter to launch JupyterLab. This will start a local server and open JupyterLab in your default web browser.

   Check the [JupyterLab documentation](https://jupyterlab.readthedocs.io/en/latest/getting_started/starting.html)!

3. **Access JupyterLab Interface**:

   - Once JupyterLab is launched, you will see the JupyterLab interface in your web browser. It consists of a file browser on the left and a main work area on the right.

   ![Jupyter Lab Interface](jupyter-lab-interface.png)

4. **Open a Notebook**:

   - You can download every notebook by clicking on the download button at the top of the webpage.
     ![Download notebook](download-notebook.png)
   - Navigate to the directory where your notebook is located using the file browser on the left.
   - Click on the notebook file (usually with a `.ipynb` extension) to open it in JupyterLab.
   - The notebook will open in a new tab within the main work area of JupyterLab.

5. **Interact with the Notebook**:
   - You can now interact with the notebook by running code cells, editing text, and executing various commands.
   - To run a code cell, select it and either click the "Run" button in the toolbar or press Shift + Enter.
   - Explore the different features of JupyterLab to customize your workflow and make the most out of your notebook experience.

```{note}
These tutorials provide practical guides on how to work with C3S data. They can be run without need for installation, and can be fully adapted to suit your needs!
```
