FROM earthlab/r-spatial-aws


RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    libcairo2-dev \
    libcurl4-openssl-dev \
    libv8-3.14-dev \
    libxml2-dev

RUN install2.r --error \
    ggmap \
    lwgeom \
    lme4 \
    mblm \
    nabor \
    psycho

EXPOSE 8787

CMD ["/init"]
