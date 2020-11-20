# Copyright (c) Zhiwei Fu.
ARG BASE_CONTAINER=continuumio/miniconda3
FROM $BASE_CONTAINER

LABEL maintainer="Z. Fu <z.fu@live.com>"

USER root

# Create git folder in pwd if not existing
RUN mkdir -p git && cd git/

# Clone the docker-deploy repo
RUN git clone https://github.com/fu-zhiwei/docker-deploy.git

# Back to original workdir
RUN cd ..

# Create new py env "main" from yaml file
RUN conda env create -q -f=./git/docker-deploy/py_main/main.yaml

# Use main by default
RUN conda activate main