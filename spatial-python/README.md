# spatial-python

Docker container with [Anaconda](http://continuum.io/downloads) (based on Python 3.8) and a set of commonly used spatial packages.

## How to use

Download and run this image using the following commands:

```
docker run -it -p 8888:8888 nathanmietkiewicz/spatial-python

docker run --user root -v new-longhorn-volume:/home/jovyan -e GRANT_SUDO=yes -it --rm -p 8888:8888 nathanmietkiewicz/spatial-python:latest
```

You can then view the Jupyter Notebook by opening `http://localhost:8888` in your browser.

