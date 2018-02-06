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

# install caret
RUN install2.r --error \
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

# install caret dependencies
RUN install2.r --error \
    caretEnsemble \
    ada \
    adabag \
    adaptDA \
    arm \
    bartMachine \
    binda \
    bnclassify \
    Boruta \
    brnn \
    bst \
    C50 \
    caTools \
    CHAID \
    class \
    Cubist \
    CVST \
    ddalpha \
    DDR \
    DEoptimR \
    deepboost \
    deepnet \
    dimRED \
    deepboost \
    deepnet \
    e1071 \
    earth \
    elasticnet \
    elmNN \
    enpls \
    evtree \
    extraTrees \
    fastAdaboost \
    fastICA \
    FCNN4R \
    foba \
    foreach \
    frbs \
    gam \
    gbm \
    glmnet \
    gower \
    gpls \
    hda \
    HDclassif \
    HiDimDA \
    inTrees \
    ipred \
    kerndwd \
    kernlab \
    kknn \
    klaR \
    kohonen \
    KRLS \
    lars \
    lava \
    leaps \
    logicFS \
    LogicReg \
    MASS \
    mboost \
    mda \
    mgcv \
    ModelMetrics \
    monomvn \
    neuralnet \
    nnet \
    nnls \
    nodeHarvest \
    numDeriv \
    oblique.tree \
    obliqueRF \
    ordinalNet \
    pamr \
    partDSA \
    party \
    penalized \
    penalizedLDA \
    pls \
    plsRglm \
    plyr \
    prodlim \
    protoclass \
    proxy \
	  pROC \
    qrnn \
    quantregForest \
    randomForest \
    randomGLM \
    ranger \
    Rborist \
    RcppRoll \
    recipes \
    relaxo \
    rFerns \
    robustbase \
    relaxo \
    rFerns \
    robustDA \
    rocc \
    rotationForest \
    rpart \
    rpartScore \
    rPython \
    rqPen \
    rrcov \
    rrcovHD \
    RRF \
    rrlda \
    RSNNS \
    RWeka \
    sda \
    SDDA \
    sdwd \
    sfsmisc \
    snn \
    sparsediscrim \
    sparseLDA \
    spikeslab \
    spls \
    SQUAREM \
    stepPlr \
    superpc \
    vbmp \
    VGAM \
    wsrf \
    xgboost \

# install spatial packages
RUN install2.r --error \
    tmap \
    ggmap \

EXPOSE 8787

CMD ["/init"]
