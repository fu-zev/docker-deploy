# Copyright (c) Zhiwei Fu.
ARG BASE_CONTAINER=continuumio/miniconda3
FROM $BASE_CONTAINER

LABEL maintainer="Z. Fu <z.fu@live.com>"

USER root

# 

# Copy needed ssh private for cloning git repo
RUN cp /

# Clone the docker-deploy repo
RUN cd /git/ && git clone git clone fu-zhiwei@vs-ssh.visualstudio.com:v3/fu-zhiwei/docker-deploy/docker-deploy

# Create new py env "main" from yaml file
RUN conda env -n main -q -y -f=/git/docker-deploy/py_main/main.yaml

# Use main by default
RUN conda activate main

WORKDIR $HOME