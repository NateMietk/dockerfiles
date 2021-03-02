# Docker image timestamped 3/1/2021
FROM jupyter/scipy-notebook:29edefbcb06a

MAINTAINER Nate Mietkiewicz <nmietkiewicz@corelogic.org>

USER root

RUN apt-get update && \
    apt-get install -y libfreetype6-dev pkg-config libx11-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
    
USER $NB_USER

RUN conda config --remove channels defaults && \
  conda config --add channels conda-forge && \
  conda install --yes -c conda-forge \
    python=3.8 \
    basemap \
    cartopy \
    gdal \
    geopandas \
    h5py \
    ipyparallel \
    jupyter \     
    jupyterlab \
    ncurses \
    netcdf4 \
    pandas \
    pyhdf \
    pysal \
    xarray && \
    conda clean --all -f -y && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"

RUN ipcluster nbextension enable --user

USER $NB_UID

WORKDIR $HOME
