# r-spatial

Docker container with R, RStudio, various spatial packages, and the tidyverse, based on the [earthlab/r-spatial-aws](https://github.com/earthlab/dockerfiles/tree/master/r-spatial-aws) image.

## How to use

Download and run this image using the following commands:

```
docker pull nathanmietkiewicz/random_forests
docker run -i -t nathanmietkiewicz/r-spatial /bin/bash
```

To use Rstudio:

```
docker run -d -p 8787:8787 nathanmietkiewicz/random_forests
```

In a web browser, navigate to localhost:8787 (on linux) or on a Mac, substitute the location pointed to by `docker-machine ip default` for `localhost`.
Log in with username: rstudio, password: rstudio.

## Mounting folders

If you want to share a directory between your host machine and the container, use the `-v` flag in your call to `docker run`, as described [here](https://github.com/rocker-org/rocker/wiki/Sharing-files-with-host-machine).
For more information on how to take full advantage of RStudio in this image, see https://github.com/rocker-org/rocker/wiki/Using-the-RStudio-image.
