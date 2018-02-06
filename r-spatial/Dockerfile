FROM earthlab/r-spatial-aws
FROM mangothecat/caret

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
    tmap \
    ggmap \

EXPOSE 8787

CMD ["/init"]
