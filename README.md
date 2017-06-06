# HAR Tutorial

_Wei-Yi Cheng, Ph.D._
_Data Scientist, Roche Innovation Center New York_

This repository contains data and scripts to run an Human Activity Recognition
(HAR) model on a subset of [WISDM actitracker](http://www.cis.fordham.edu/wisdm/dataset.php)
data.

## Setting up working environment

The easiest way to get started is to run the jupyter notebook from
[docker](https://www.docker.com/). If you do not have docker installed in your
environment, you can do so by following the instruction from the
docker website([Windows](https://www.docker.com/docker-windows),
[Mac](https://www.docker.com/docker-mac)).

Once you have docker installed (you can run `docker run hello-world` without
error), you can build the docker image for this tutorial simply by doing

```
cd /path/to/where/you/clone/har-tutorial
cd docker
docker build --tag har .
```

Once the image is built, you can run

```
docker run -it --rm -p 8888:8888 har jupyter-notebook --no-browser --ip=*
```

This command will give you a link to the jupyter notebook with a secure token,
_e.g._ `http://localhost:8888/?token=f67b0b3ddd446900c4f94822af2275c5883d029322efda07`.
Enter this link in your browser, it will then take you to jupyter notebook.

