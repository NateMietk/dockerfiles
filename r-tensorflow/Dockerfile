FROM rocker/rstudio

MAINTAINER "Maxwell Joseph" maxwell.b.joseph@colorado.edu

# from the tensorflow dockerfile: 
# https://github.com/tensorflow/tensorflow/blob/master/tensorflow/tools/docker/Dockerfile

# Pick up some TF dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
        build-essential \
        curl \
        libfreetype6-dev \
        libzmq3-dev \
        pkg-config \
        python \
        python-dev \
        rsync \
        software-properties-common \
        unzip \
        libxml2-dev \
        && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN curl -O https://bootstrap.pypa.io/get-pip.py && \
    python get-pip.py && \
    rm get-pip.py

RUN pip --no-cache-dir install \
        ipykernel \
        jupyter \
        matplotlib \
        numpy \
        scipy \
        keras \
        h5py \
        && \
    python -m ipykernel.kernelspec

RUN pip install tensorflow

RUN pip --no-cache-dir install \
  --upgrade tensorflow
  
RUN pip --no-cache-dir install virtualenv

RUN install2.r --error \
    devtools \
    tensorflow \
    keras \
    neuralnet \
    ISLR \
    caTools \
    tidyverse
    
RUN R -e "tensorflow::install_tensorflow(version = "gpu")"

RUN R -e "keras::install_keras(tensorflow = "gpu")"

CMD ["/init"]