FROM ghcr.io/burgrp/riot-base

RUN apt install -y \
    gcc-arm-none-eabi \
    gcc-multilib \
    libstdc++-arm-none-eabi-newlib \
    picolibc-arm-none-eabi \
    libudev-dev

RUN make -C $RIOTBASE/dist/tools/edbg
