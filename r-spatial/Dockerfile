FROM earthlab/r-spatial-aws


RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    libcairo2-dev \
    libjq-dev \ 
    libprotobuf-dev \
    libv8-3.14-dev \
    protobuf-compiler

RUN install2.r --error \
    tmap 

EXPOSE 8787

CMD ["/init"]

