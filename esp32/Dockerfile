FROM ghcr.io/burgrp/riot-base

RUN apt install -y \
    bzip2

ENV IDF_TOOLS_PATH=/idf
RUN $RIOTBASE/dist/tools/esptools/install.sh all

COPY fixpath.inc /bin/
