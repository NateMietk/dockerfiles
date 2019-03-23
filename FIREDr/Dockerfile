FROM earthlab/r-spatial-aws

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    libcairo2-dev \
    libcurl4-openssl-dev \
    libv8-3.14-dev \
    libxml2-dev

RUN R -e "install.packages('foreach',dependencies=TRUE, repos='http://cran.rstudio.com/')" \
RUN R -e "install.packages('gdalUtils',dependencies=TRUE, repos='http://cran.rstudio.com/')" \
RUN R -e "install.packages('Hmisc',dependencies=TRUE, repos='http://cran.rstudio.com/')" \
RUN R -e "install.packages('lwgeom',dependencies=TRUE, repos='https://github.com/r-spatial/lwgeom')" \
RUN R -e "install.packages('pbapply',dependencies=TRUE, repos='http://cran.rstudio.com/')" \
RUN R -e "install.packages('parallel',dependencies=TRUE, repos='http://cran.rstudio.com/')" \
RUN R -e "install.packages('raster',dependencies=TRUE, repos='http://cran.rstudio.com/')" \
RUN R -e "install.packages('sf',dependencies=TRUE, repos='http://cran.rstudio.com/')" \

getURL

EXPOSE 8787

CMD ["/init"]
