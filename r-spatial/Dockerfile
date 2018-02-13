FROM earthlab/r-spatial-aws


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

    ## install caret
    minqa \
    nloptr \
    RcppEigen \
    profileModel \
    pbkrtest \
    lme4 \
    brglm \
    gtools \
    car \
    BradleyTerry2 \
    caret \
    
    ## install spatial mapping
    tmap \
    ggmap \
    viridis \
    viridisLite \
    
    ## install caret dependencies packages
    caretEnsemble \
    MASS \
    neuralnet \
    randomForest \
    rpart \
    rPython
    
EXPOSE 8787

CMD ["/init"]
