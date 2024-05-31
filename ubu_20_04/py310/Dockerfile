FROM ubuntu:20.04

ENV PYTHON_VERSION 3.10.1
ENV LINUX_VERSION ubuntu:20.04
USER root



RUN apt-get update &&\
    apt-get upgrade -y && \
    #apt-get install -y --no-install-recommends curl gcc g++ gnupg unixodbc-dev openssl git &&\
    apt-get install -y software-properties-common ca-certificates &&\
    apt-get install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libssl-dev libreadline-dev libffi-dev wget libbz2-dev libsqlite3-dev && \
    update-ca-certificates && \
    rm -rf /var/lib/apt/lists/*

RUN mkdir /python && cd /python && \
    wget https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tgz && \
    tar -zxvf Python-$PYTHON_VERSION.tgz && \
    cd Python-$PYTHON_VERSION && \
    ls -lhR && \
    ./configure --enable-optimizations && \
    make install && \
    rm -rf /python

### Stage 1 - add/remove packages ###



### Stage 1 - add/remove packages ###


### Stage 2 --- collapse layers ###
RUN python3 --version 
RUN pip3 install pip --upgrade
### Stage 2 --- collapse layers ####

#CMD ["/bin/bash", "/run.sh"]

# size 865mb