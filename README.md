# venv2jup
Utility to add virtual environment to jupyter or jupyterhub.


## Usage:

  venv2jup [--help|-h]

Run this from within a virtual environment. Afterwards, refresh the jupyter
hub's server page and the virtual environment will be listed under the
"New" button.  The environment will also have inherited any settings 
to the environment variables encoded in the EXPORTVARS variable.

## Explanation

This automates the following steps:

 1. Deduces the virtual environment name from the VIRTUAL_ENV 
    environment variable.

 2. Install ipykernel in the virtual environment, which allows 
    it to operate as a kernel.

 3. Register the virtual environment as a kernel in 
    ~/.local/share/jupyter/kernels/<NAME>/kernel.json

 4. Adds environment variables to that kernel.json file to 
    reproduce the current environment.

## Installation

Just copy venv2jup to a place in the PATH. 
