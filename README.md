# *SHARD: A Resource-aware Partitioning Framework for Distributed Inference on Heterogeneous Devices*

by *Washington R. D. Silva, Luciano S. Fraga, Andrew Williams, Kleber V. Cardoso, and Fábio L. Verdi*

# Purpose

This repository hosts the implementations described in the paper *"SHARD: A Resource-aware Partitioning Framework for Distributed Inference on Heterogeneous Devices"*, which has been submitted for publication in *IEEE Networking Letters*. 

The repository is currently under construction. Source code and supplementary materials will be made available soon.

## Abstract

Emerging augmented reality applications demand substantial computing resources to support object detection within stringent latency constraints. Deploying these applications on heterogeneous edge platforms requires partitioning workloads across available devices. However, assessing feasibility prior to deployment remains challenging. Hence, we present SHARD, a resource-aware framework that converts object detection models into Directed Acyclic Graphs, profiles node performance using analytical modeling, and formulates a constrained optimization problem for platform-agnostic distributed inference. SHARD easily supports different Deep Learning models and different hardware specifications, making it a powerful tool for evaluating inference feasibility on heterogeneous platforms.

## Code implementation and references

> Briefly describe the software/scripts used to produce the results of the
> paper. The following is an example:

All source code used to generate the results and figures in the paper are in
the `code` folder.
The data used in this study is provided in `data` and the sources for the
manuscript text and figures are in `manuscript`.
Results generated by the code are saved in `results`.
See the `README.md` files in each directory for a full description.

## Using the code

You can download a copy of all the files in this repository by cloning the
[git](https://git-scm.com/) repository:

    git clone https://github.com/antonia-had/paper_template.git

or [download a zip archive](https://github.com/antonia-had/paper_template/archive/master.zip).

A copy of the repository is also archived at *insert DOI here*


## Dependencies

> Depending on your project, the script might depend on several other packages
> to run. If using Python, you can use a '.yml' file specifying your dependencies.
> You can create one and place it in the repository so subsequent users take it
> and create a Python environment with all they need to replicate your results.
> This section should then describe how one can set up an environment with the
> dependencies necessary to run your code.

You'll need Python *version number* to run the code.
You can set up an environment with all dependencies using an environment manager
like [Anaconda Python distribution](https://www.anaconda.com/download/) which
provides the `conda` package manager.
Anaconda can be installed in your user directory and does not interfere with
the system Python installation.
The required dependencies are specified in the file `environment.yml`.

Run the following command in the repository folder (where `environment.yml`
is located) to create a separate environment and install all required
dependencies in it:

    conda env create

## Data
> You need to either provide or cite the data used in your analysis.
> Avoid cluttering your repository with a lot of raw data but instead archive and
> mint a DOI for your data.

Hadjimichael, A. (2020). My interesting dataset [Data set]. DataHub. https://doi.org/some-doi-number

## Reproducing the results

> Here you should include all information necessary to reproduce your results.
> Ideally, you'd set up a makefile that automates as much as possible, but make
> sure to provide clear step-by-step instructions for everything.
> The following can be used as example of replicating Python code.

Activate the conda environment:

    source activate ENVIRONMENT_NAME

or, on Windows:

    activate ENVIRONMENT_NAME

To build and test the software, produce all results and figures, follow these steps:

> Add steps here


## License

All source code is made available under a BSD 3-clause license. You can freely
use and modify the code, without warranty, so long as you provide attribution
to the authors.

The manuscript text is not open source. The authors reserve the rights to the
article content, which is currently submitted for publication in the
JOURNAL NAME.
