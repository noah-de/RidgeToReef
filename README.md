# RidgeToReef

Jupyter notebooks for a binder-based module as part of the the Ridge to Reef program, August 2018

Authors: Kelly Caylor (caylor@ucsb.edu) and Natasha Krell (nkrell@ucsb.edu)

## Getting Started

To get started with the excercise, click here: [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/ecohydro/RidgeToReef/master?filepath=index.ipynb)

## About this Repo

This repository is a set of jupyter notebooks, data, and accompanying configuration files designed to be used with the [binder](mybinder.org) system. Through Binder, these notebooks provide an executable environment, making the code immediately reproducible by anyone, anywhere.

The following information is for authors of the module or others who wish to fork this repo and/or use it as the basis of their own efforts (but please see the Acknowledgements and Disclaimer below). 

**Students or anyone else wishing to simply _access_ the module can stop reading now and just use the [![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/ecohydro/RidgeToReef/master?filepath=index.ipynb) link to start the module in their browser.**


## Installing this Repo locally

While this repositorty is `binder-ready`, meaning it can be run in the cloud using `binder.org`'s awesome service, it is also possible to use the repository in a more traditional way - using `jupyter` on your personal laptop or PC. While a complete description of the steps to install this repo locally is beyond the scope of this module, we are providing the steps necessary, and links to resources where you can get details on each step.

1. **Install `Anaconda`'s most recent distribution of python.** 

The most recent distribution of `Anaconda` can be found [here](https://www.anaconda.com/download). The specific steps for installing `Anaconda` will vary depending on your operating system, but the installers all have easy to follow installation instructions.

2. **Use the `conda` command to create a new python environment named `RidgeToReef`.** 

The `conda` command is installed as part of the Anaconda python distribution and a quick introduction to `conda` is [here](https://conda.io/docs/user-guide/getting-started.html). For most installations, you will need to open a shell terminal and type the following command:

```shell
> conda create -n RidgeToReef python=3.6
``` 

_Note: The next step assumes you already have a working installation of `git` on your machine. If you don't, you will need to [install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). As with installing `Anaconda`, instructions vary based on your OS. But it's all pretty painless._

3. **Clone the `RidgeToReef` github repository to your local machine.**

 This is done by using the `git clone` command:

```shell
> git clone https://github.com/ecohydro/RidgeToReef.git
```

After successfully cloning the repo to your local machine, you should change directory into the RidgeToReef folder,

```shell
> cd RidgeToReef
```

4. **Update the `RidgeToReef` environment.**

The conda command uses a special file called `environment.yml` to resolve any necessary dependencies that are required to run the `jupyter` notebooks contained in this repository. We've placed that file in the `binder` folder, which is a special folder used by the `binder.org` service when setting up the cloud version of this repository. However, that same file can be used to configure your local `python` environment (yay!). We can gather and install the required files using the following command:

```shell
> conda env update --name RidgeToReef --file binder/environment.yml
``` 

_Note: The above command will only work if the `RidgeToReef` environment is not active. Use `conda deactivate` to deactivate your environment._

5. **Activate the `RidgeToReef` conda environment.**

```shell
> conda activate RidgeToReef
``` 

6. **Start the `jupyter` notebook server.**  

At this point, you are all set to run the jupyter notebooks locally in your web browser. You can start the webserver an open the `index.ipynb` notebook using the following command:

```shell
> jupyter notebook index.ipynb
```

This should launch the `index.ipynb` in your local browser. Changes you make to this file (or any other `ipynb` notebook) will be autosaved. Feel free to edit or add any material you want. If you do something cool with this data and/or models, then please submit a pull request to the module. 

Enjoy!

## Additional Details

Our analyses are built on the [Anaconda](https://www.anaconda.com/distribution/) python distribution, using [Python v.3.6](https://www.python.org/downloads/release/python-360/). 

### binder/

Configuration files are stored in the `binder/` folder of this repository. The `environment.yml` file contains required python packages. Note **this file cannot be auto-generated by `conda env export`.** You must instead specify the main requirements (e.g. `numpy`, `pandas`) and their versions. 

### data/

The `data/` folder contains all the necessary data files that are used in this excercise. These data were collected as part of the NSF projects acknowledged below, and **any use of these data outside of this excercise requires permission of the authors** (cf. contact information above).

### assets/

Any images, files, or other resources used in the notebooks are contained in the `assets/` folder. 

# Acknowledgements & Disclaimer

This material is based upon work supported by the National Science Foundation under Grants No. [SES-1534544](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1534544&HistoricalAwards=false) and [SES-1360421](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1360421&HistoricalAwards=false). Any opinions, findings, and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the National Science Foundation.
