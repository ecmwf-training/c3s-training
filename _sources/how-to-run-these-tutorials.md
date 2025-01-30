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
If you would like to run this notebook in your own environment, we suggest you install [Miniforge](https://conda-forge.org/download/), which contains most of the libraries you will need.<br>
In our [github repository](https://github.com/Randbee/C3SBook) you can find every notebook in `notebooks/` folder. Also, there is a `requirements.txt` file, containing the necessary python libraries for running our notebooks.You need to run this command in the same directory as the requirements.txt file.

`pip install -r requirements.txt`

```

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
These tutorials provide practical guides on how to work with atmospheric composition data. They can be run without need for installation, and can be fully adapted to suit your needs!
```
