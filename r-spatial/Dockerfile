FROM earthlab/r-spatial-aws


RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    libcairo2-dev \
    libcurl4-openssl-dev \
    libjq-dev \
    libprotobuf-dev \
    libv8-3.14-dev \
    libxml2-dev \
    protobuf-compiler \
    texlive-fonts-extra \
    texlive-latex-extra

RUN install2.r --error \
    ggmap \
    && R -e "devtools::install_github("hunzikp/velox")" \
    && R -e "devtools::install_github("mtennekes/tmaptools")" \
    && R -e "devtools::install_github("mtennekes/tmap")" \
    && R -e "devtools::install_github('sjmgarnier/viridis')" \
    && R -e "devtools::install_github("ecohealthalliance/fasterize")"

EXPOSE 8787

CMD ["/init"]
