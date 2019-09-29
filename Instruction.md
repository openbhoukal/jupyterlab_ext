### 1. Setup a development environment

Set up a new conda environment which includes:
1. The latest version of [JupyterLab](https://github.com/jupyterlab/jupyterlab)
2. [cookiecutter](https://github.com/audreyr/cookiecutter), the tool used to bootstrap the extension
3. [NodeJS](https://nodejs.org/en/), the JavaScript runtime used to compile the extension
4. [git](https://git-scm.com/), the version control system used throughout this tutorial

Creating a new conda environment for the extension leaves the root conda environment
untouched. This is a best practice which isolates your extension from other development
activities on your machine.

A new conda environment can be created with the required dependencies by running:
```bash
conda create -n runall-extension jupyterlab cookiecutter nodejs git -c conda-forge
```

Activate the new conda environment so that all commands operate on that environment.

On Unix/Linux:
```bash
source activate runall-extension
```

On Windows:
```cmd
activate runall-extension

###2. Clone repo

```bash
git clone https://github.com/openbhoukal/jupyterlab_ext/new/demo
```

### 3. Build, install and run the extension

Your new extension project has enough code in it to see it working in JupyterLab.
But first, the initial project dependencies must be installed and the extension
code compiled:

```bash
cd jupyterlab_ext/managementextension/
jlpm install
jlpm run build
jupyter labextension install .
jupyter lab
```






