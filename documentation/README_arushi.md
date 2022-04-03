<div align="center">

# Welcome to the **Ersilia Model Hub**!

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/uk/fundraiser/charity/4145012) [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](code_of_conduct.md) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



[![documentation](https://img.shields.io/badge/-Documentation-purple?logo=read-the-docs&logoColor=white)](https://ersilia.gitbook.io/ersilia-book/) [![PyPI version fury.io](https://badge.fury.io/py/ersilia.svg)](https://pypi.python.org/pypi/ersilia/) [![Python 3.7](https://img.shields.io/badge/python-3.7-blue.svg)](https://www.python.org/downloads/release/python-370/) [![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg?logo=Python&logoColor=white)](https://github.com/psf/black) [![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/ersilia-os/ersilia)

</div>

![logo](https://github.com/ersilia-os/ersilia/blob/master/assets/Ersilia_Plum.png)

### Table of Contents:
1. [Project Description](https://github.com/ersilia-os/ersilia#project-description)
2. [Getting started](https://github.com/ersilia-os/ersilia#getting-started)
3. [Contribute](https://github.com/ersilia-os/ersilia#contribute)
4. [Roadmap](https://github.com/ersilia-os/ersilia#roadmap)
5. [License and citation](https://github.com/ersilia-os/ersilia#license-and-citation)
6. [About us](https://github.com/ersilia-os/ersilia#about-us)

# Project Description
The Ersilia Model Hub is the main project of the [Ersilia Open Source Initiative](https://ersilia.io). The aim is to provide a platform for a user-friendly deployment of AI/ML models, where scientists can browse through the assets, identify those which is relevant to their research and obtain predictions without the need of coding expertise. Currently, most of the tools developed, even when published and fully open-sourced, remain unusable by a large majority of the scientific community who does not have the necessary expertise. This gap becomes even larger in Low and Middle Income Country institutions where access to bioinformatic facilities or data science experts are scarce. With this project, we hope to democratize access to this expertise and support research into neglected and infectious diseases.

The models embedded in the hub include both models published in the literature (with appropriate third party acknowledgment) and models developed by the Ersilia team or contributors. All assets are open source, but please do check the Licenses of each model before using them.

## An overview of the Ersilia Model Hub
![overview](https://user-images.githubusercontent.com/78142604/160505622-a5ef0a35-93eb-4506-a961-8876617e0541.png)

* Read more about the project better at the [Ersilia Book](https://ersilia.gitbook.io/ersilia-book/)
* Available models can be checked at [Ersilia Model Hub](https://airtable.com/shr9sYjL70nnHOUrP/tblZGe2a2XeBxrEHP)

# Getting started

## Libraries and Packages
There are a few third-party pre-requisites and you need to have them installed on your computer before proceeding with the installation of the Ersilia tool. You can dowload the correct version for your system by clicking on the links below.

1. [Python 3.7 and above](https://www.python.org/)
2. [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html) / [Anaconda](https://docs.anaconda.com/anaconda/install/index.html) / [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
3. [Docker](https://www.docker.com/)
4. [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
5. [Git LFS](https://git-lfs.github.com/)


 For a better understanding refer to the [Ersilia Book](https://ersilia.gitbook.io/ersilia-book/quick-start/installation).


## Installation on Linux and MacOSX

1. Open a terminal. The best is to set up a [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) environment.

**Create a conda environment**
```
conda create -n ersilia python=3.7
```

**Activate the environment**
```
conda activate ersilia
```

2. Then, simply install the Ersilia Python package.

**Clone from github**
```
git clone https://github.com/ersilia-os/ersilia.git
```
```
cd ersilia
```
**Install with pip (use -e for developer mode)**
```
pip install -e .
```
3. Quickly check that the CLI works on your system.

**See ersilia CLI options**
```
ersilia --help
```

## Installation on Windows
We currently are not testing Windows installation consistenly. We recommend you to install Ubuntu on your Windows machine. THis can be done very easily with the help of ``WSL``.

**Open a Power Shell with Admin permissions and type**
```
wsl --install
```
Then simply install the [Ubuntu terminal](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6#activetab=pivot:overviewtab) on Windows.


If you have any doubts regarding the installation steps, or if you are confused as to why are we using a specific third party pre-requisite, we recommend you to have a look at the [Ersilia Documentation](https://ersilia.gitbook.io/ersilia-book/).

## How to Browse Models

Once Ersilia is installed, you can **browse models** in the [Ersilia Model Hub](https://airtable.com/shrXfZ8pqro0jjcsG/tblZGe2a2XeBxrEHP/viwd5XJVLslkE11Tg).

Select one model. For example `chemprop-antibiotic`. You can **fetch** your model with the Ersilia CLI:
```
ersilia fetch chemprop-antibiotic
```
Generate a few (5) example molecules, to be used as input. Molecules are typically expressed in SMILES format.
```
ersilia example chemprop-antibiotic -n 5 -f my_molecules.csv
```
Then, **serve** your model:
```
ersilia serve chemprop-antibiotic
```
And run the prediction **API**:
```
ersilia api -i my_molecules.csv -o my_predictions.csv
```
Finally, **close** the service when you are done.
```
ersilia close
```

Please see the [Ersilia Book](https://ersilia.gitbook.io/ersilia-book/) for more examples and detailed explanations.

# Contribute
The Ersilia Model Hub is developed and maintained by a small team of Ersilia employees and volunteers, and any contribution is highly valued! There are several ways in which you can contribute to the project:
- If you are a developer, check the [issues](https://github.com/ersilia-os/ersilia/issues) and help us to improve the tool
- If you have developed a model and would like to include it in the Hub to increase its visibility and usability, please [contact us](https://ersilia.io) or open an [issue](https://github.com/ersilia-os/ersilia/issues). We are currently working on an automated contribution tool to facilitate the process.
- If you are a scientist with a cool dataset, also [contact us](https://ersilia.io) or open an [issue](https://github.com/ersilia-os/ersilia/issues) as we might be interested in developing a model based on the data!
- If there is a third-party model you have identified and would like to see it in the Hub, open an [issue](https://github.com/ersilia-os/ersilia/issues) with the relevant information and we will get back to you as soon as possible.

The Ersilia Open Source Initiative adheres to the [Contributor Covenant](https://ersilia.gitbook.io/ersilia-wiki/code-of-conduct) guidelines.

# Roadmap
We are working to grow the Hub organically and responding to our users needs. Here a detail of the next features to come, stay tuned!
1. Deployment for Windows System (expected: February 2022)
2. Automated third-party model contributions (expected: March 2022)
3. Possibility to run lite models online (expected: May 2022)

# License and citation
This repository is open-sourced under the MIT License.
Please [cite us](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) if you use it.

# About us
The [Ersilia Open Source Initiative](https://ersilia.io) is a Non Profit Organization incorporated with the Charity Commission for England and Wales (number 1192266). Our mission is to reduce the imbalance in biomedical research productivity between countries by supporting research in underfunded settings.

You can support us via [Open Collective](https:/opencollective.com/ersilia).

# Contributors
Thanks to all the contributors for their contributions.


<a href = "https://github.com/ersilia-os/ersilia">
  <img src = "https://contrib.rocks/image?repo=ersilia-os/ersilia"/>
</a>