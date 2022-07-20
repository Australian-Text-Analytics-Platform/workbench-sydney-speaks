# Workbench for Sydney Speaks corpus

Current version: [v0.0.0](https://github.com/Australian-Text-Analytics-Platform/workbench-sydney-speaks/releases/tag/v0.0.0)

A workbench for corpus tools accessing the Sydney Speaks corpus. This workbench is based on the GLAM Workbench - https://github.com/GLAM-Workbench/glam-workbench-template .  For more information see the [Workbench for Sydney Speaks corpus](https://glam-workbench.net/workbench-for-sydney-speaks-corpus/) section of the GLAM Workbench.

## Access and use of the Sydney Speaks corpus

This workbench requires any user to already have access to the Sydney Speaks corpus. Remember to respect the contents and context of the corpus and follow any requirements of any license agreed to when obtaining the access.  

## Accessing Oni

Some of the notebooks in this workshop currently run using a demo version of Oni deployed on Nectar, which requires a particular API token.

To get an API token, go to https://oni-demo.text-commons.org, login via GitHub and generate an API TOKEN.

Edit the *vars.env* file in your *notebooks/* folder with:

    API_KEY=PASTE_YOUR_KEY_HERE

Do not commit this to GitHub as it is your private token.

## Notebook topics

* [LDACA-Sydney-Speaks notebook](notebooks/ldaca-sydney-speaks.ipynb) [![Launch on Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Australian-Text-Analytics-Platform/workbench-sydney-speaks/HEAD?labpath=notebooks%2Fldaca-sydney-speaks.ipynb) – Example notebook to run against LDACA
  
  Remember to remove any notebook output to prevent pushing sensitive information. See https://github.com/Australian-Text-Analytics-Platform/ldaca-sydney-speaks for the original notebook and instructions on how to use it.
  
See the [GLAM Workbench for more details](https://glam-workbench.github.io/workbench-for-sydney-speaks-corpus/).

<!-- START RUN INFO -->
<!-- Anything in these sections will not be visible in the index.ipynb file -->

## Run these notebooks

There are a number of different ways to use these notebooks. Binder is quickest and easiest, but it doesn't save your data. I've listed the options below from easiest to most complicated (requiring more technical knowledge).

### Using Binder

[![Launch on Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Australian-Text-Analytics-Platform/workbench-sydney-speaks/master/?urlpath=lab/tree/index.ipynb)

Click on the button above to launch the notebooks in this repository using the [Binder](https://mybinder.org/) service (it might take a little while to load). This is a free service, but note that sessions will close if you stop using the notebooks, and no data will be saved. Make sure you download any changed notebooks or harvested data that you want to save.

See [Using Binder](https://glam-workbench.net/using-binder/) for more details.

### Using Reclaim Cloud

[![Launch on Reclaim Cloud](https://glam-workbench.github.io/images/launch-on-reclaim-cloud.svg)](https://app.my.reclaim.cloud/?manifest=https://raw.githubusercontent.com/Australian-Text-Analytics-Platform/workbench-sydney-speaks/master/reclaim-manifest.jps)

[Reclaim Cloud](https://reclaim.cloud/) is a paid hosting service, aimed particularly at supported digital scholarship in hte humanities. Unlike Binder, the environments you create on Reclaim Cloud will save your data – even if you switch them off! To run this repository on Reclaim Cloud for the first time:

* Create a [Reclaim Cloud](https://reclaim.cloud/) account and log in.
* Click on the button above to start the installation process.
* A dialogue box will ask you to set a password, this is used to limit access to your Jupyter installation.
* Sit back and wait for the installation to complete!
* Once the installation is finished click on the 'Open in Browser' button of your newly created environment (note that you might need to wait a few minutes before everything is ready).

See [Using Reclaim Cloud](https://glam-workbench.net/using-reclaim-cloud/) for more details.

### Using Docker

You can use Docker to run a pre-built computing environment on your own computer. It will set up everything you need to run the notebooks in this repository. This is free, but requires more technical knowledge – you'll have to install Docker on your computer, and be able to use the command line.

* Install [Docker Desktop](https://docs.docker.com/get-docker/).
* Create a new directory for this repository and open it from the command line.
* From the command line, run the following command:  
  ```
  docker run -p 8888:8888 --name workbench-sydney-speaks -v "$PWD":/home/jovyan/work quay.io/glamworkbench/workbench-sydney-speaks repo2docker-entrypoint jupyter lab --ip 0.0.0.0 --NotebookApp.token='' --LabApp.default_url='/lab/tree/index.ipynb'
  ```
* It will take a while to download and configure the Docker image. Once it's ready you'll see a message saying that Jupyter Notebook is running.
* Point your web browser to `http://127.0.0.1:8888`

See [Using Docker](https://glam-workbench.net/using-docker/) for more details.

### Setting up on your own computer

If you know your way around the command line and are comfortable installing software, you might want to set up your own computer to run these notebooks.

Assuming you have recent versions of Python and Git installed, the steps might be something like:

* Create a virtual environment, eg: `python -m venv workbench-sydney-speaks`
* Open the new directory" `cd workbench-sydney-speaks`
* Activate the environment `source bin/activate`
* Install the necessary Python packages: `pip install -r requirements.in`
* Clone the repository: `git clone https://github.com/Australian-Text-Analytics-Platform/workbench-sydney-speaks.git notebooks`
* Open the new `notebooks` directory: `cd notebooks`
* Run Jupyter: `jupyter lab`

See the GLAM Workbench for [more details](https://glam-workbench.net/getting-started/#using-python-on-your-own-computer).

<!-- END RUN INFO -->

## Cite as

See the GLAM Workbench or [Zenodo](https://doi.org/10.5281/zenodo.3521724) for up-to-date citation details.

----

This repository is part of the [GLAM Workbench](https://glam-workbench.github.io/).  

