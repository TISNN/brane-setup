# WSCBS_Assignment4b_brane_Setup

This implementation is the initialization part of Titanic Project ([Machine Learning from Disaster](https://www.kaggle.com/c/titanic/overview)).

## Usage
This is the **first** package in our pipeline of project([Assignment 4b](https://github.com/TISNN/WSCBS_Assignment4b)). This part is used for upload our data to brane's file system. It is built for future pipeline of uploading data, which is not necessary in this project since the data is already provided in *./data*. 

Each package, as a part in the brane pipeline, can be run separately to produce the corresponding results (processed data, ML models, visualization)

## Requirements

- Complete installation of Brane ([manual1](https://wiki.enablingpersonalizedinterventions.nl/user-guide/software-engineers/installation.html), [manual2](https://wiki.enablingpersonalizedinterventions.nl/admins/installation/get-binaries.html))
- Brane Dependencies (also in [manual1](https://wiki.enablingpersonalizedinterventions.nl/user-guide/software-engineers/installation.html), [manual2](https://wiki.enablingpersonalizedinterventions.nl/admins/installation/get-binaries.html))
- Brane IDE [manual](https://github.com/epi-project/brane-ide)

## Setup

### By source code (Git repository)

1. Download the source code by `git clone`
```shell
$ git clone https://github.com/TISNN/brane-setup.git
$ cd brane-setup
```
2. Build brane package by .yml file
```shell
$ brane build container.yml
```
3. Check availablity
```shell
$ brane list
```

### By brane package method

1. import brane package
```shell
$ brane import TISNN/brane-setup
```
2. Check availablity
```shell
$ brane list
```

If you see `init` package with version==2.0.0, it was successfully built.

## Run
This package is only effective when executing on brane-ide.

1. Go to you path to `brane-ide`
2. Once brane-ide is installed, launch the containerized JupyterLab environment:
```shell
$ make start-ide
```
3. When we open the jupyter lab with branescript as the kernel, we can already see a `/data` path on the left side, which is the path to brane's file system. There are no files in it yet, we need to copy our own `train.csv` and `test.csv` to this file system.
```shell
[1] import init;
[2] print(init("init"));
```
4. If seen "init done", it ran successfully.