# Jupyter Notenooks


## Setup

    # install pyenv if needed
    curl https://pyenv.run | bash

    # create a python we'll use with jupyter
    pyenv install 3.10.7
    pyenv virtualenv 3.10.7 notebooks-jupyter
    pyenv local notebooks-jupyter

    # install jupyter
    pip install jupyterlab
    # pip install pandas jupyter notebook ipykernel matplotlib seaborn

    # register environment with jupyter
    python -m ipykernel install --user --name myenv --display-name "Python (notebooks-jupyter)"

    # install some packages to use in our notebooks
    pip install matplotlib scipy


## Run

    jupyter-lab


## Uninstall

    # remove virtualenv
    pyenv uninstall 3.10.7/envs/notebooks-jupyter
