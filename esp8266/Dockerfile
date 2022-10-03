FROM ghcr.io/burgrp/riot-base

RUN apt install -y gdb-multiarch python3-serial
RUN git clone -c advice.detachedHead=false --depth 1 https://github.com/gschorcht/xtensa-esp8266-elf /esp/xtensa-esp8266-elf

COPY fixpath.inc /bin/
