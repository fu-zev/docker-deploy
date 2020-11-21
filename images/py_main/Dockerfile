# Copyright (c) Zhiwei Fu.
ARG BASE_CONTAINER=continuumio/miniconda3
FROM $BASE_CONTAINER

LABEL maintainer="Z. Fu <z.fu@live.com>"

USER root

# Clone the docker-deploy repo
RUN mkdir -p git && cd git/ && git clone https://github.com/fu-zhiwei/docker-deploy.git && conda env create -q -f ./docker-deploy/images/py_main/main.yaml

WORKDIR $HOME