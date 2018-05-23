FROM earthlab/spatialverse-aws

RUN install2.r --error \
    ggmap \
    lwgeom \
    lme4 \
    mblm \
    nabor \
    psycho \
    tmaptools \
    tmap

EXPOSE 8787

CMD ["/init"]
