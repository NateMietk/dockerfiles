FROM jupyter/scipy-notebook

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
    arcpy \
    basemap \
    cartopy \
    gdal \
    geopandas \
    h5py \
    ipyparallel \
    ncurses \
    netcdf4 \
    pandas \
    pyhdf \
    pysal \
    xarray

RUN ipcluster nbextension enable --user

COPY test.ipynb test.ipynb

RUN jupyter nbconvert --to notebook --execute test.ipynb && \
    rm test*