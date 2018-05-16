FROM earthlab/spatialverse-aws


RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    libcairo2-dev \
    libcurl4-openssl-dev \
    libjq-dev \
    libprotobuf-dev \
    libv8-3.14-dev \
    libxml2-dev \
    protobuf-compiler


RUN install2.r --error \
    ggmap \
    lwgeom \
    lme4 \
    mblm \
    nabor \
    psycho \
    tmaptools \
    tmap \
    ## from GitHub
  && R -e "install_github("hadley/rlang", dependencies = TRUE, force = TRUE)" \
  && R -e "install_github("tidyverse/ggplot2",force=TRUE)"

EXPOSE 8787

CMD ["/init"]
