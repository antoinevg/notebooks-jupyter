# Jupyter Notenooks

## Jupyter Setup

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
    python -m ipykernel install --user --name notebooks-jupyter --display-name "Python (notebooks-jupyter)"

## Python Kernel Setup

    # install some packages to use in our notebooks
    pip install matplotlib scipy

## Rust Kernel Setup

    # TODO: https://pypi.org/project/rustenv/

    rustup component add rust-src
    cargo install evcxr_jupyter
    evcxr_jupyter --install

    # some supporting packages
    pip install plotly

Links:

* https://github.com/google/evcxr/

## Run

    jupyter-lab

## Uninstall

    # remove evcxr_jupyter
    evcxr_jupyter --uninstall
    cargo uninstall evcxr_jupyter

    # remove virtualenv
    pyenv uninstall 3.10.7/envs/notebooks-jupyter

## Useful docs

* [evcxr common usage information](https://github.com/google/evcxr/blob/main/COMMON.md)
* [evcxr notebook](https://github.com/google/evcxr/blob/main/evcxr_jupyter/samples/evcxr_jupyter_tour.ipynb)
* [plotly notebook](https://igiagkiozis.github.io/plotly/content/fundamentals/jupyter_support.html)
* [plotters](https://crates.io/crates/plotchart#trying-with-jupyter-evcxr-kernel-interactively)
* [plotters notebook](https://plotters-rs.github.io/plotters-doc-data/evcxr-jupyter-integration.html)
