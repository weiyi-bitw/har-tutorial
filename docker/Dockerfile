FROM tensorflow/tensorflow:latest

MAINTAINER Wei-Yi Cheng

RUN apt-get update && apt-get install -y git-core && \
    rm -rf /var/apt/lists/*

RUN pip install keras h5py && \
    rm -rf /root/.cache/pip/*

ENV KERAS_BACKEND="tensorflow"

RUN useradd -ms /bin/bash har
USER har
WORKDIR /home/har

RUN git clone https://github.com/weiyi-bitw/har-tutorial.git && \
    cd har-tutorial && \
    tar -zxvf wisdm_subset.tar.gz

