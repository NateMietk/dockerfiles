FROM earthlab/r-spatial-aws

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    libcairo2-dev \
    libcurl4-openssl-dev \
    libv8-3.14-dev \
    libxml2-dev
    
RUN install2.r --error \ 
caret \
ranger \
lwgeom \
tuneRanger \
mlr \
pbapply \
velox \
reaster \
ncdf4 \
sf \
rasterVis \
gridExtra \
data.table \
rvest \
parallel \
foreach \
httr \
purrr \
rgdal \
maptools \
foreign \
zoo \
lubridate \
spatstat

EXPOSE 8787

CMD ["/init"]
